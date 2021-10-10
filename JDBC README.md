# JAVA-OOPS-Concepts
My Learnings in CSS corp

JDBC
API's is that gives access virtually of any tabular data source 
from the java programing language

The Java application calls JDBC classes and interfaces to submit SQL statements and retrieve results
he JDBC API is implemented through the JDBC driver

-->There are 4 types of JDBC drivers


    Type-1 driver or JDBC-ODBC bridge driver.
    Type-2 driver or Native-API driver.
    Type-3 driver or Network Protocol driver.
    Type-4 driver or Thin driver.
    
    Type-1
   ->JDBC-ODBC bridge driver uses ODBC driver to connect to the database. 
   ->The JDBC-ODBC bridge driver converts JDBC method calls into the ODBC function calls.
   ->The driver is also called Universal driver because it can be used to connect to any of the databases.
   ->This driver software is built-in with JDK so no need to install separately.
   ->It is a database independent driver.
   
   Type-2
   ->This driver converts JDBC method calls into native calls of the database API.
   ->In order to interact with different database, this driver needs their local API,
     that’s why data transfer is much more secure as compared to type-1 driver.
   
   Type-3
   ->This driver converts JDBC method calls into native calls of the database API. 
   ->In order to interact with different database, this driver needs their local API, 
     that’s why data transfer is much more secure as compared to type-1 driver.
     
   Type-4
   ->Thin driver is also called native protocol driver. This driver interact directly with database.
     It does not require any native database library, that is why it is also known as Thin Driver.
   ->Does not require any native library and Middleware server, so no client-side or server-side installation.
     It is fully written in Java language, hence they are portable drivers.
     
     
     **establish connection with JDBC**
     
     ->Register the driver:
       To develop a basic JDBC application, first of all, you need to register the driver with the[ DriverManager]
       You can register a driver in two ways, 
          ->one is using [ registerDriver() ] method of the DriverManager class
          ->using [forName()] method of the class named Class.

         ---The [ registerDriver() ] method accepts an object of the Driver class, it registers the specified Driver with the DriverManager.
          
          ( Driver myDriver = new com.mysql.jdbc.Driver();
            DriverManager.registerDriver(myDriver);  )

         ---The [ forName() ] method loads the specified class into the memory and thus it automatically gets registered.
           
           ( Class.forName("com.mysql.jdbc.Driver"); )

       ->Get Connection: Get the Connection object using the getConnection() method. 
         
         [ getConnection() ]
         
          This method accepts the database URL (an address that points to your database),
          Username and, password as parameters and, returns a connection object.

           Invoke this method by passing, the URL of the desired database, user name and, password as parameters to it.

         (  String url = "jdbc:mysql://localhost/";
           String user = "root";
           String passwd = "password";
           Connection conn = DriverManager.getConnection(url, root, passwd);  )
     
     
       ---> PROGRAM
     
     
      import java.sql.*;
         public class JDBCExample {
           static final String JDBC_DRIVER = "com.mysql.jdbc.Driver";
           static final String DB_URL = "jdbc:mysql://localhost/";
   
           static final String USER = "root";
           static final String PASS = "password";

           public static void main(String[] args) {
           Connection conn = null;
           try{
           Class.forName("com.mysql.jdbc.Driver");
           System.out.println("Connecting to database...");
           conn = DriverManager.getConnection(DB_URL, USER, PASS);
           System.out.println("Connection established");
           }
           catch(Exception e)
           {
         }
           System.out.println("Goodbye!");
   }
}
