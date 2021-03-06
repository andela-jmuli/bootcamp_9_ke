### Object Oriented Programming  

##### The general Definition  
Object oriented programming refers to a programming methodology based on objects, instead of just fuctions and procedures. The objects are organized into classes, which allow individual objects to be grouped together.  

An object refers to a specific type or **instance** of a class. Each object has a structure similar to other objects in the class, but can be assigned individual characteristics.  

An example is a class Vehicle which describes the minimum things a vehicle is. A vehicle generally describes a car or truck just to be minimal... In this case both instances do have differences e.g. size, purpose etc. Back to the Vehicle where a couple of more attributes includes movement, a driver and wheels. With this, it's clear that the class is Vehicle, instances are car and truck. Thus inheritance occurs where each instance consists of the class's attributes and of course both instances are totally different.  

Polymorphism in this example is descibed where both instances basically do the same thing but each doing it slightly different but with the same goal or attribute defined.  

Object oriented programming makes it easier for programmers to structure and organize programs. Because individual objects can be modified without affecting other aspects of the program, it is also easier to update and change programs writter in object-oriented languages.  


#### Object Oriented programming in Python  

Classes can be thought of as blueprints for creating objects. When one defines a Customer class using the **class** keyword, A customer hasn't really been created but a manual on how customer objects should be constructed.  

```
class Customer(object):
	"""
	A customer of Richy bak with a checking account. Customers have the following properties
	Attributes:  
	name: string representing customer name  
	balance: A float tracking the current balance of the customer's account
	"""

	# constructor
	def __init__(self, name, balance=0.0)
		self.name = name
		self.balance = balance


	def withdrawal(self, amount)
	# returns balance after withdrawing an amount
		if amount > self.balance:
			raise RuntimeError('Amount greater than available balance.')
			self.balance -= amount
			return self.balance


	def deposit(self, amount):
		# returns balance remaining after a deposit of 'amount'
		self.balance += amount
		return self.balance
```

The Customer class doesn't really create a new customer. To do so, we call the class's init method with the proper argument number. Thus:  
```
 joseph = Customer('Joseph Muli', 5000.0)
```


###### Instance Attributes and Methods  

A function defined in a class is called a "method". Methods have access to all the data contained on the instace of the object. They can access and modify anything previously set on self. Because they use self, they require an instance of the class in order to be used thus referred to as instance methods.  


###### Static Methods  

Class attributes are attributes that are set at the class-level, as opposed to the instance-level. Normal attributes are introduced in the init method, but some attributes of a class hold for all instances in all cases.

```
class Car(object):
	wheels = 4

	def __init__(self, make, model):
		self.make = make
		self.model = model


"""
object instantiation
"""
speedster = Car('Pagani', 'Zonda')
print speedster.wheels
"""
returns 4
"""

```

Static Methods don't have access to **self**. Just like class attributes, they are methods that work without requiring an instance to be present. Thus static methods have no self parameter and take the decorator @staticmethod when defined. An example: 

packages and modules nb..... 

```
class Car(object):
	
	@staticmethod
	def make_car_sound():
		print 'Vrooooooooooooooom!'

```