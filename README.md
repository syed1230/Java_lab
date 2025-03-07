# Java_lab
java practice codes
<br>
import java.util.Scanner;
class exam{
public static void main(String[] args){
Scanner input=new Scanner(System.in);
<br>
int n=10;
for(int i=1;i<=n;i++){
System.out.println("value of i is :"+i);
}<br>
for(int i=1;i<=n; i=i+2){
System.out.println("value of i is :"+i);
}<br>
int m=1;
for (int i=10;i>=n;i--){
System.out.println("i value is:"+i);
}<br>
int sum=0;
for(int i=1;i<=n;i++){
sum=sum+i;
System.out.println("sum is :"+sum);
}<br>
for(int i=0;i<=n;i=i+2){
System.out.println("even numbers is:"+i);
}
}
}
<!--10/02/2025-->
import java.util.Scanner;
class exam{
public static void main(String[] args){
Scanner input=new Scanner(System.in);
System.out.println("fibinocci series");
System.out.println("enter a number:");
int n =input.nextInt();
int f1=0,f2=1;<br>
System.out.println(" "+f1);
System.out.println(" "+f2);
for ( int i=1;i<=n;i++){
int f3=f1+f2;
System.out.println(" "+f3);
f1=f2;
f2=f3;
}<br>
int fact=1;
for(int i=1;i<=n;i++){
fact=fact*i;
}
System.out.println("factorial of given number:"+fact);<br>
for ( int i=1;i<=n;i++){
if (i%2==0){
System.out.println("it is a composite number:"+i);
}
else{
System.out.println("it is a prime number:"+i);
}
}

}
}
<!--week3-->
class car{
//creating the attributes requires for the classs
String car_name,car_color,car_brand,fule_type;
int maleage;
//constructor
car(String car_name,String car_color,String car_brand,String fule_type,int maleage){
this.car_name=car_name;
this.car_color=car_color;
this.car_brand=car_brand;
this.fule_type=fule_type;
this.maleage=maleage;
}

//creating the methods forte class

public void start(){
System.out.println("this is start statement: "+car_name+"  "+car_color);
}

public void stop(){
System.out.println("this is start statement: "+car_brand+"  "+fule_type);
}

public void services(){
System.out.println("this is start statement: "+maleage);
}

public static void main(String[] args){
//creating the object for the class
car car1=new car("maruthi","navy blue","KIA","petrol", 1234);
car1.start();
car car2=new car("maruthi","navy blue","KIA","petrol", 1234);
car2.stop();
car car3=new car("maruthi","navy blue","KIA","petrol", 1234);
car3.services();

System.out.println("\n THANK YOU FOR APPLYING THIS");
}
}
<!--bank code-->

import java.util.Scanner;

class BankAccount {
 // Class-level variable to store balance
    private float existing;
    private Scanner input; // Single Scanner instance for input
    public  String name;
    // Constructor
    public BankAccount() {
        input = new Scanner(System.in);
        System.out.println("Enter the account holder name :");
        this.name=input.next();
        System.out.print("Enter existing amount in bank account: ");
        this.existing = input.nextFloat();
    }
    // Deposit method
    public void deposit() {
        System.out.print("Enter amount to be deposited: ");
        float deposit = input.nextFloat();
        existing += deposit;
        System.out.println("Existing amount now is: " + existing);
    }
    // Withdrawal method
    public void withdrawal() {
        System.out.print("Enter amount to be withdrawn: ");
        float withdrawal = input.nextFloat();
        if (existing < withdrawal) {
            System.out.println("Not sufficient balance.");
        } else {
            existing -= withdrawal;
            System.out.println("Remaining balance: " + existing);
        }
    }
    // Main method
    public static void main(String[] args) {
        BankAccount customer1 = new BankAccount();
        customer1.deposit();
        customer1.withdrawal();
        System.out.println("thank you " + customer1.name + " for using our bank");

}
}
<!--03/03/2025-->
class book{
//creating the variables

public String title_of_book;
public String author;
public int year_publication;

//creating a constructor 
book(String title_of_book,String author,int year_publication){
this.title_of_book=title_of_book;
this.author=author;
this.year_publication=year_publication;
}
//creating the method to print DETAILS
public void details(){
System.out.println("the title of the book is: "+title_of_book+"\nThe author of te book is: "+author+"\nthe year of publication is:"+year_publication+"\n");
}
//creating the main class and objects for the method
public static void main(String[] args){
book one=new book("THE GREAT INDIAN RIVERS","DR.SHIVARAM",1989);
one.details();
book two=new book("ANGLES IN TIBET","S.SLUMP",2001);
two.details();
System.out.println("\nThese are the details of the two books which are famously treading nowadays\n THANK YOU ");
}

}
class myclass{
//creating the variables

static int count=0;
final double pi=3.1415;
//creating a constructor 
myclass(){
count++;
}
//method to print the values
public void values(){
System.out.println(+count);
System.out.println(+pi);
}
//object and the main function
public static void main(String[] args){
myclass one=new myclass();
one.values();
myclass two=new myclass();
two.values();
myclass three=new myclass();
three.values();
myclass four=new myclass();
four.values();
}

}
<!--code for single inheritences-->
import java.util.Scanner;

class CLanguage {
    String one = "c";
    int package1 = 210000;
    public void info_1() {
        System.out.println("the company " + one + " gives a package of: " + package1 + " for c language");
    }
}

class JavaLanguage extends CLanguage {
    String two = "java";
    int package2 = 10000000;
    public void info_2() {
        System.out.println("the company " + two + " gives a package of: " + package2 + " for java");
    }
}

class OOPs extends JavaLanguage {
    public static void main(String[] args) {
        String king = "oops";
        int package3 = 1000000000;
        JavaLanguage I = new JavaLanguage();
        CLanguage cLang = new CLanguage(); // Create instance of CLanguage
        System.out.println("enter java/c/oops");
        Scanner input = new Scanner(System.in);
        System.out.println("enter your course language:");
        String learn = input.nextLine(); // Changed to nextLine()
        if (learn.equals(cLang.one)) { // Accessing instance variable through the instance
            I.info_1();
            System.out.println("\nyou have chosen the c language\nAll the best"); // Fixed typo
        } else if (learn.equals(I.two)) { // Accessing instance variable through the instance
            I.info_2();
            System.out.println("\nyou have chosen the java language\nAll the best"); // Fixed typo
        } else if (learn.equals(king)) { // Changed to equals()
            System.out.println("the king is " + king + " with high package of: " + package3);
        }
    }
}
<!--single inheritence-->
class Amma {  // Superclass
    String clg_1 = "amaravati";
    String clg_2 = "chennai";
    String clg_3 = "bengaluru";

    
}
class Enginer extends Amma {  // Subclass
Enginer(String clg_1,String clg_2,String clg_3) {
       this.clg_1=clg_1;
this.clg_2=clg_2;
this.clg_3=clg_3;
    }
    public void cse_amar() {
        System.out.println("You have selected the "+clg_1+" branch.");
for (int i=1;i<2;i++){
System.out.println("increase your career our collage\n***\n\n");
}
    }
    public void cse_chennai() {
        System.out.println("You have selected the "+clg_2+" branch.");
for (double i=8.5;i<=11 ;i++){
System.out.println("your cgpa has incrades in our collage:"+i);
}
    }
    public void cse_bengaluru() {
        System.out.println("***\n\nYou have selected the "+clg_3+" branch.");
for(int i=1;i<4;i++){
System.out.println("According to your cgpa ur fee-slab is: slab-"+i);
}
    }
}
 class inherit {
    public static void main(String[] args) {
        Enginer eng = new Enginer("amaravati","chennai","bengaluru");  // Create an object of Enginer
        eng.cse_amar();  // Call method for Amaravati branch
        eng.cse_chennai();  // Call method for Chennai branch
        eng.cse_bengaluru();  // Call method for Bengaluru branch
    }
}
