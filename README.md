# Java_lab
java practice codes
import java.util.Scanner;
class exam{
public static void main(String[] args){
Scanner input=new Scanner(System.in);
int n=10;
for(int i=1;i<=n;i++){
System.out.println("value of i is :"+i);
}
System.out.println("next program");
for(int i=1;i<=n; i=i+2){
System.out.println("value of i is :"+i);
}
int m=1;
for (int i=10;i>=n;i--){
System.out.println("i value is:"+i);
}
int sum=0;
for(int i=1;i<=n;i++){
sum=sum+i;
System.out.println("sum is :"+sum);
}
for(int i=0;i<=n;i=i+2){
System.out.println("even numbers is:"+i);
}
}
}
