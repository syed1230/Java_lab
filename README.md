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
//10/02/2025
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
