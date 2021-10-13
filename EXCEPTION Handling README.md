# JAVA-OOPS-Concepts
My Learnings in CSS corp


1)EXCEPTION

An exception is an event  which occurs during the 
execution of a program that disrupts the flow of the program's instructions.

An exception can occur when
= A user has entered invalid data.
= A file that needs to be opened cannot be found
= A network connection has been lost in the middle of 
  communications 
= The JVM has run out of memory.

TYPES OF EXCEPTION

Checked Exception

Checked exceptions are those exceptions that are checked by the java compiler
itself at compilation time and are not under runtime exception class hierarchy.
Checked exceptions must be handled either by using try and catch block or by using throws

LIST OF CHECKED EXCEPTION
= ClassNotFoundException
= InterruptedException
= InstantiationException
= IOException
= SQLException
= IllegalAccessException
= FileNotFoundException, etc

2)Unchecked Exception

Unchecked exceptions in Java are those exceptions that are checked by JVM,
not by java compiler. They occur during the runtime of a program.

LIST OF UNCHECKED EXCEPTION

= ArithmeticException
= ClassCastException
= NullPointerException
= ArrayIndexOutOfBoundsException
= NegativeArraySizeException
= ArrayStoreException
= IllegalThreadStateException
= SecurityException, etc.


3)Error
Error is irrecoverable Some example of errors are OutOfMemoryError, VirtualMachineError, AssertionError etc


->TRY CATCH FINALLY

TRY

The first step in constructing an exception handler 
is to enclose the code that might throw an 
exception within a try block

try 
{ code }


CATCH

To associate an exception handler with a try block, 
a catch block is to be mentioned after it

try
{ } 
catch (ExceptionType name)
{ }

THROWABLE CLASS

The argument type,ExceptionType, declares the 
type of exception that the handler can handle and 
must be the name of a class that inherits from 
theThrowabl

FINALLY BLOCK

The finally block always executes when 
the try block exits.
Finally block is executed even if an unexpected 
exception occurs


->Advantage of Exception Handling

The core advantage of exception handling is to maintain the normal flow of the application.
An exception normally disrupts the normal flow of the application,that is why we need to handle
exceptions. 

statement 1;  
statement 2;  
statement 3; //exception occurs 
statement 4;  
statement 5;  
statement 6;  

There are 6 statements in a Java program and an exception occurs at statement 3
the rest of the code will not be executed, statements 4 to 6 will not be executed.

when we perform exception handling the rest of the statements will be executed,
that is why we use exception handling in Java.

->>Java Exception Keywords

Keyword	Description

i) try	

The "try" keyword is used to specify a block where we should place an exception code,
It means we can't use try block alone. The try block must be followed by either catch or finally.

ii) catch

The "catch" block is used to handle the exception , It must be preceded by try block which means 
we can't use catch block alone It can be followed by finally block later.

iii) finally	

The "finally" block is used to execute the necessary code of the program It is executed whether
an exception is handled or not.

iv) throw	

The "throw" keyword is used to throw an exception.

v) throws

The "throws" keyword is used to declare exceptions  It specifies that there may occur an exception 
in the method. It doesn't throw an exception. It is always used with method signature.


-->EXAMPLE OF exception<--

public class Exception
{  
  public static void main(String args[])
  {  
   try{  
      int data=100/0;  //raise exception
   }catch
   (ArithmeticException e) // If we divide any number by zero, there occurs an ArithmeticException.
   
   {System.out.println(e);}  
     
  }  
}  

output--
java.lang.ArithmeticException: / by zero

--->>example 2<----
Multipul catch block

public class exception 
{  
    public static void main(String[] args)
    {  
     try{    
        int a[]=new int[5];    
         a[5]=30/0;    
     }    
      catch
      (ArithmeticException e)  
     {  
         System.out.println("Arithmetic Exception ");  
     }    
      catch
      (ArrayIndexOutOfBoundsException e)  
     {  
         System.out.println("ArrayIndexOutOfBounds Exception ");  
     }    
       catch
       (Exception e)  
     {  
          System.out.println("Parent Exception ");  
     }             
    }
   }
   
   output---
   
   Arithmetic Exception 

