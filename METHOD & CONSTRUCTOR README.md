# JAVA-OOPS-Concepts
My Learnings in CSS corp

1)METHODS

A method is block of code that contains a series of 
statements A program that executed  by calling the method 
and specifying any required method arguments

The Main method is entry point in every java 
application and it is called by the JVM when the 
program is started.

CREATE METHOD

public int funcName(int a, int b) { // body }
public        = Access specifier
int           = return type
funcName      = function name
int a, int b  = list of parameters



public class Addition   
{  
public static void main(String[] args)   
{  
int a = 19;  
int b = 5;  
 
int c = add(a, b);   
System.out.println("The sum of a and b is= " + c);  
}  

public static int add(int n1, int n2)   
{  
int s;  
s=n1+n2;  
return s; 
}  
} 

OUTPUT
The sum of a and b is= 24

2)CONSTRUCTOR

A constructor initializes an object when it is created.
It has the same name as its class and is syntactically similar to a method.
However, constructors have no explicit return type.

DEFAULT CONSTRUCTOR

Hence, the Java compiler automatically creates the default constructor.
The default constructor initializes any uninitialized instance variables 
with default values.


 
