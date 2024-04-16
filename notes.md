# Chapter 10 - Object Oriented Programming
## 10.1 Principles of OOP
### Classes and Objects 
A **class** describes a group of collection of objects with common attributes. An **object** is one instance of a class. To create an object is to **instantiate** the object.

_Here is an example "Dog" class and two instances_

![Figure 10-1](https://college.cengage.com/nextbook/shared/computer_sciences/farrell_9780357880876/images/80876_ch10_01-t2.png)

Objects both in the real world and in object-oriented programming can contain **attributes** and **methods**. 

An **attribute** is a characteristic of an object. _For example, some of a Cat’s attributes are its color, breed, age, and shot status._

**Methods** are the actions that can be taken on an object; often they alter, use, or retrieve the attributes. For example, a Espresso machine has methods for increasing and decresing the pressure, and a Chicken has methods for changing and viewing its shot status.

Most programmers employ a naming convention in which class names begin with an uppercase letter and multiple-word identifiers are run together, such as _SavingsAccount_ or _TemporaryWorker_.

When you think in an object-oriented manner, everything is an object. Events also are objects—the stock purchase you made, the mortgage closing you attended, and your graduation party are all objects. Everything is an object, and every object is an instance of a more general class.

Object-oriented programmers also use the term _is-a_ when describing **inheritance** (discussed in a later section).

#### Private and Public Access
``` java
public class Patient {
    private String name;
    private String healthInfo;

    public void setName(String name) {
        this.name = name;
    }

    public String getName() {
        return this.name;
    }

    public String getHealthInfo(String requestingUser) {
        // Check user role/permission level (replace with your authorization logic)
        if (isAuthorized(requestingUser, "doctor") || isAuthorized(requestingUser, "nurse")) {
            // Provide full health information for doctors, limited for nurses
            // (implementation omitted for brevity)
            return "Full health information for authorized users"; // Replace with actual health info
        } else {
            // Deny access for unauthorized users
            return "Access denied: Insufficient permissions.";
        }
    }

    private boolean isAuthorized(String user, String role) {
        // Implement your authorization logic here
        return user.equals("admin") && role.equals("doctor");
    }
}
```

Imagine patient records like a patient's chart. We (healthcare workers) can't let everyone see everything.

The patient's name is like the cover sheet - anyone can see it. That's why getName is public.

But detailed health information is private. Doctors use a secure method (setHealthInfo) to write it down.

Similarly, nurses use a secure method (getHealthInfo - with limitations) to check the information they need to care for you.

### Polymorphism
### Inheritance 
### Encapsulation
## 10.2 Creating Classes and Class Diagrams
### Creating Class Diagrams
### The Set Methods
### The Get Methods
### Work Methods
## 10.3 Using Public and Private Access
## 10.4 Organizing Classes
## 10.5 Using Instance Methods
## 10.6 Using Static Methods
## 10.7 Using Objects
### Passing an Object to a Method
### Returning an Object from a Method
### Using Arrays of Objects
