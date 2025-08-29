---
{"dg-publish":true,"permalink":"/jyothis-electronics-lab/","tags":["gardenEntry"]}
---

# JYOTHIS ELECTRONICS LAB



Test Contents

*This will be entirely focused on object oriented python.*

>[!info]- What is Object Oriented Programming?
>In treats real-world entities as objects and groups related data and functionality together. In traditional programming languages like [[03 Coding/01 C/C\|03 Coding/01 C/C]] the data and functions are seperate and treated differently but in OOP they are grouped together as objects. 

>[!info]- Why Object Oriented Programming?
>In my personal opinion when dealing with real world entities or *things* in general oop makes so much sense. Consider the following 
>You have these functions  
>```c
>int get_age();
>string get_name();
>void get_date_of_birth();
>void print_details();
>```
>In functional programming languages like **C** you will pass a reference to a struct , which will be like follows
>```c
>struct Person {
>	int age;
>	string name;
>	string place_of_birth;
>	date date_of_birth;
>};
>```
>In **C** you will do like 
>```c
>get_name(&person1)
>get_age(&person1)
>get_date_of_birth(&person1)
>print_details(&person1)
>```
>And in oop we do something like following, trust me dealing with pointers is hard for starters
>```python
>person.get_name()
>person.get_age()
>person.get_date_of_birth()
>person.print_details()
>```
>Using functional language with something to group together data like `struct` is great but some like to group functions too like c++ structs which allows to pack functions too. . and i do like the features comes with Object Oriented Programming like **inheritance**, **polymorphism** etc. Which makes sense and updating the codebase much easier. You can always change the logic of the function without changing the interface. It is possible in functional programming languages too but it is not as easy as in OOP.


**Class**: Is a blueprint for creating objects
**Object**: Is an instance of a class

## Class  and Objects
*A class consists of set of attributes and methods.* 
So if you did a little bit of python before you might have already seen classes and objects , you might not realize but when you use basic things like `x = 5` in that `x` is an object of class `int`. To test the theory do the following

```python
print(type(1)) # class 'int'
print(type("Hello")) # class 'str'
print(type(1.5)) # class 'float'
```
{ #341f6e}


>[!success]- **Output**
>```
><class 'int'>
><class 'str'>
><class 'float'>
>```


**Now how can we create new classes?** Look at the following
```python
class Person:
	def print_age(self,age):
		print(f"Age is {age}")  # Method
```
This defines a class named `Person` with a method `print_age`. But in python most of the time when your creatiing a class you will also define an `__init__` method which is called the **initializer**. It is used to initialize the attributes of the class. so the following example is more appropriate. 
