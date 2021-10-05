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

3)TRY CATCH FINALLY

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


