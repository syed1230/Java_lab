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

