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
<!--multilevel inheritence-->
class Amma {  // Superclass
    String clg_1 ;
    String clg_2 ;
    String clg_3;

    
}
class Enginer extends Amma {  // Subclass
    public void cse_amar() {
        System.out.println("You have selected the "+clg_1+" branch.");
System.out.println("you have studied enginering for the following years:\n");
for (int i=2024;i<2029;i++){
System.out.println(+i);
}
    }
    public void cse_coeim() {
        System.out.println("*****\n\nYou have selected the "+clg_2+" branch.");
System.out.println("studied enginering and became haker\n\n");
for (int i=4;i>=1;i--){
for (int j=0;j<4;j++){
System.out.print(" ");
}
for (int k=0;k<i;k++){
System.out.print("hacker ");
}
System.out.println();
}
    }
}
class Administer extends Enginer{
Administer(String clg_1,String clg_2,String clg_3) {
       this.clg_1=clg_1;
this.clg_2=clg_2;
this.clg_3=clg_3;
    }
    public void cse_fad() {
        System.out.println("\n\n\nYou have selected the "+clg_3+" branch.");
System.out.println("you have became a :");
for(int i=4;i>=1;i--){
System.out.println("Doctor!!");
}
    }
}
 class inherit {
    public static void main(String[] args) {
        Administer eng = new Administer("amritapuri","coeimbator","faridab");  // Create an object of Enginer
        eng.cse_amar();  // Call method for Amaravati branch
        eng.cse_coeim();  // Call method for Chennai branch
        eng.cse_fad();  // Call method for Bengaluru branch
    }
}
<!--10/03/2025-->
import java.util.Scanner;
//PARENT CLKASS 
class Calci{
    float a;
    float b;
    static String ad="+";
     static String su="-";
     static String mu="*";
     float x;
     float y;
    Calci(){
        System.out.println("welcome to the calculator");
    }
}
class Simple extends Calci {
Simple(float a,float b){
    this.a=a;
    this.b=b;
}
 //ADDITION METHOD
    public  float add(float a, float b){
        float c;
        c=a+b;
        System.out.println("\n\nADDITION: "+c);
        return c;
    }
    //SUBTRACTION METHOD
    public float sub(float a , float b){
        float d;
        if(a>b){
            d=a-b;
        }
        else{
            d=b-a;
        }
        System.out.println("\n\nSUBSTRACTION: "+d);
        return d;
    }
//MULTIPICATION METHOD 
    public float  multi(float a,float b){
        float e;
        e=a*b;
        System.out.println("\n\n MULTIPICATION: "+e);
        return e;
    }
}
//MAIN FUNCTION 
class book extends Calci {
    public static void main(String[] args){
        Scanner input=new Scanner(System.in);
        System.out.println("enter types: [+] or[-]or[*]");
        String type=input.nextLine();
        Simple two=new Simple(4,5);
        if (type.equals(ad)){
        two.add(4,5);
        }
        else if(type.equals(su)){
        two.sub(4,5);
        }
        else if (type.equals(mu)){
        two.multi(4,5);
        }
    }
}
<!--10/03/2025-->
<!--calculator programm-->
import java.util.Scanner; 
class Calculator {
    // Base class for the calculator
Calculator(){
System.out.println("\nthis is the calculator program\n");
System.out.println("------------------------------------");
}

}

class Simple extends Calculator {
    public int add(int a, int b) {
        return a + b;
    }
    public int subtract(int a, int b) {
        return a - b;
    }
    public int multiply(int a, int b) {
        return a * b;
    }
}

class Super extends Simple {
    public int square(int a) {
        return a * a;
    }
    public int cube(int a) {
        return a * a * a;
    }
    public double squareRoot(int a) {
        return Math.sqrt(a);
    }
}
class Advanced extends Super { 
    public double divide(int a, int b) {
        if (b != 0) {
            return (double) a / b;
        } else {
            return 0; // Division by zero is not allowed.
        }
    }
    public int modulus(int a, int b) {
        return a % b;
    }
}
public class inherit {
    public static void main(String[] args) {
	Scanner input=new Scanner(System.in);
	System.out.println("enter a value:");
	int a=input.nextInt();
	System.out.println("enter b value: ");
	int b=input.nextInt();
        Simple simpleCalc = new Simple();
        System.out.println("Addition: " + simpleCalc.add(a, b));
        System.out.println("Subtraction: " + simpleCalc.subtract(a, b));
        System.out.println("Multiplication: " + simpleCalc.multiply(a, b));
        Advanced advancedCalc = new Advanced();
        System.out.println("Division: " + advancedCalc.divide(a, b));
        System.out.println("Modulus: " + advancedCalc.modulus(a, b));
        Super superCalc = new Super();
        System.out.println("Square: " + superCalc.square(a));
        System.out.println("Cube: " + superCalc.cube(b));
        System.out.println("Square Root: " + superCalc.squareRoot(b));
    }
}
<!--vehicle company-->
class Vehicle{
    String brand;
    int speed;
    Vehicle(String brand,int speed){
        this.brand=brand;
        this.speed=speed;
    }
    void Details(){
        System.out.println("Brand:"+brand);
        System.out.println("\nSpeed:"+speed);
	System.out.println("------------------------------");
    }
}//End of super class

class CARS extends Vehicle{
    int doors;
    int capacity;
    public CARS(String brand,int speed,int doors,int capacity){
        super(brand, speed);
        this.doors=doors;
        this.capacity=capacity;
    }
    void cardetails(){
        System.out.println("\nNumber of doors:"+doors);
        System.out.println("\nCapacity:"+capacity);
	System.out.println("----------------");    
}

}//End of car sub-class

class Bikes extends Vehicle{
    Boolean gears;
    Bikes(String brand,int speed,Boolean gears){
        super(brand, speed);
        this.gears=gears;
    }
    void bikedetails(){
        if (gears==true) {
        System.out.println("This bike has gears.");
	}
        else{
        System.out.println("This bike does not have gear system.");
}    
}

}//End of bike sub-class

class Trucks extends Vehicle{
    int tons;
    Trucks(String brand,int speed,int tons){
        super(brand, speed);
        this.tons=tons;
    }
    void truckdetails(){
        System.out.println("The capacity of truck is: "+tons);
    }

}//End of truck sub-class
class inherit{
    public static void main(String[] args){
        CARS c=new CARS("Tayota",120,5,2);
        c.cardetails();
        c.Details();
        Bikes b=new Bikes("KTM",80,true);
        b.bikedetails();
        b.Details();
        Trucks t=new Trucks("TATA",150,1);
        t.truckdetails();
        t.Details();
	System.out.println("THANK YOU FOR COMING TO OUR COMPANY :) ~ ^ !");
    }
}
