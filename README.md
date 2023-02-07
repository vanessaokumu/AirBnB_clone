PROJECT DESCRIPTION
Write a command interpreter to manage your AirBnB objects.

DESCRIPTION OF COMMAND INTERPRETER
It’s exactly the same but limited to a specific use-case. In our case, we want 
to be able to manage the objects of our project:

Create a new object (ex: a new User or a new Place)
Retrieve an object from a file, a database etc…
Do operations on objects (count, compute stats, etc…)
Update attributes of an object
Destroy an object

HOW TO START IT
Clone the repository
cd into the directory

HOW TO USE IT
put in place a parent class (called BaseModel) to take care of the initialization, serialization and deserialization of your future instances

create a simple flow of serialization/deserialization: Instance <-> Dictionary <-> JSON string <-> file

create all classes used for AirBnB (User, State, City, Place…) that inherit from BaseModel

create the first abstracted storage engine of the project: File storage.

create all unittests to validate all our classes and storage engine

EXAMPLE

guillaume@ubuntu:~/AirBnB$ ./console.py

(hbnb) all MyModel

** class doesn't exist **

(hbnb) show BaseModel

** instance id missing **

(hbnb) show BaseModel My_First_Model

** no instance found **

(hbnb) create BaseModel

49faff9a-6318-451f-87b6-910505c55907

(hbnb) all BaseModel

["[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}"]

(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907

[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'id': '49faff9a-6318-451f-87b6-910505c55907', 'updated_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903300)}

(hbnb) destroy

** class name missing **

(hbnb) update BaseModel 49faff9a-6318-451f-87b6-910505c55907 first_name "Betty"

(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907

[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}

(hbnb) create BaseModel

2dd6ef5c-467c-4f82-9521-a772ea7d84e9

(hbnb) all BaseModel

["[BaseModel] (2dd6ef5c-467c-4f82-9521-a772ea7d84e9) {'id': '2dd6ef5c-467c-4f82-9521-a772ea7d84e9', 'created_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639717), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 23, 639724)}", "[BaseModel] (49faff9a-6318-451f-87b6-910505c55907) {'first_name': 'Betty', 'id': '49faff9a-6318-451f-87b6-910505c55907', 'created_at': datetime.datetime(2017, 10, 2, 3, 10, 25, 903293), 'updated_at': datetime.datetime(2017, 10, 2, 3, 11, 3, 49401)}"]

(hbnb) destroy BaseModel 49faff9a-6318-451f-87b6-910505c55907

(hbnb) show BaseModel 49faff9a-6318-451f-87b6-910505c55907

** no instance found **

(hbnb) 
