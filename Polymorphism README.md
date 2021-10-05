# JAVA-OOPS-Concepts
My Learnings in CSS corp


class Animal {
  public void animalSound() {
    System.out.println("The animal makes a sound");
  }
}

class LION extends Animal {
  public void animalSound() {
    System.out.println("The LION : ror ");
  }
}

class Dog extends Animal {
  public void animalSound() {
    System.out.println("The dog : bow wow");
  }
}

public class Main {
  public static void main(String[] args) {
    Animal myAnimal = new Animal();
    Animal myLION = new LION();
    Animal myDog = new Dog();
        
    myAnimal.animalSound();
    myLION.animalSound();
    myDog.animalSound();
  }
}


// OUTPUT
The animal makes a sound
The LION : ror 
The dog : bow wow
