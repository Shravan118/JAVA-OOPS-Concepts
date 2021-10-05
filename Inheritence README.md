# JAVA-OOPS-Concepts
My Learnings in CSS corp


class Shravan{
String designation = "Intern";
String companyName = "CSS Corp";
void does(){
System.out.println("Training");
}
}
public class HadoopShravan extends Shravan{
String mainSubject = "Spark";
public static void main(String args[]){
HadoopShravan obj = new HadoopShravan();
System.out.println(obj.companyName);
System.out.println(obj.designation);
System.out.println(obj.mainSubject);
obj.does();
}
}

// OUTPUT

CSS Corp
Intern
Spark
Training
