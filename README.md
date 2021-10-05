# JAVA-OOPS-Concepts
My Learnings in CSS corp


// program of encapsulation




class Encapsulate { 

    private String ShravanName;
    private int ShravanRoll;
    private int ShravanAge;
 
   
    public int getAge()
    { return ShravanAge; }
 
    public String getName()
    { return ShravanName; }
 
   
    public int getRoll()
    { return ShravanRoll; }
 
   
    public void setAge(int newAge)
    { ShravanAge = newAge; }
 
   
    public void setName(String newName)
    { ShravanName = newName; }
 
    
    public void setRoll(int newRoll) 
    { ShravanRoll = newRoll; }
    
    
    }
 
    public class Encapsulation {
    public static void main(String[] args)
    {
        Encapsulate obj = new Encapsulate();
 
        
        obj.setName(" SHRAVAN ALEXANDER ");
        obj.setAge(22);
        obj.setRoll(53);
 
       
        System.out.println("Name: " + obj.getName());
        System.out.println("Age:   " + obj.getAge());
        System.out.println("Roll:  " + obj.getRoll());
 
     
    }
}



// OUTPUT 
Name:  SHRAVAN ALEXANDER 
Age:   22
Roll:  53
