from abc import*
class DBinterface(ABC):
    @abstractmethod
    def connect(self):pass

    @abstractmethod
    def disconnect(self):pass

class Oracle(DBinterface):
    def connect(self):
        print("connecting to Oracle database")
    def disconnect(self):
        print("disconeccting to Oracle Database")

class Sybase(DBinterface):
    def connect(self):
        print("connecting to sybase database")
    def disconnect(self):
        print("disconeccting to sybase Database")

dbname=input("enter database name:")
classname=globals()[dbname]
x=classname()
x.connect()
x.disconnect()



Note:The inbuilt function globals()[str] converts the string 'str' into a class name and returns the 
classname
