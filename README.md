LAB SHEET1
Q1. Presidency University collects student information during enrolment for the even semester. The program uses the Scanner class to take input (such as name,course,gender, age,fees and fees paid status) from the student and displays the information entered. Help the Presidency University by writing an application in java to perform the same. (Hint: Use Scanner Class to take the Input from the User)
import java.util.Scanner;
public class first
{
  public static void main(String[] ar) 
    {    	Scanner sc= new Scanner(System.in);
    	System.out.println("Enter your name,course, gender,age, fees and fees paid");
    	String name=sc.nextLine();
    	String course=sc.nextLine();
    	char gender=sc.next().charAt(0);
    	int age=sc.nextInt();
    	float fees=sc.nextFloat();
    	boolean feespaid=sc.nextBoolean();
    	System.out.print("Your name is "+name+"gender is "+gender);
    	System.out.println("");
    	System.out.println("Your age is " +age);
    	System.out.print("your fees " +fees+"and feespaid "+ feespaid);
    }  }
Your age is 54
your fees 123900.4 and feespaid true




Q2 . A power distribution company charges its customers based on the number of units consumed. The tariff rates are as follows:
•	For the first 100 units: ₹1.50 per unit
•	For the next 200 units (101-300): ₹2.50 per unit
•	For units above 300: ₹4.00 per unit
import java.util.Scanner;
public class ElectricityBill {
public static void main(String[] args)
	{    Scanner scanner = new Scanner(System.in);
               // read number of units consumed from keyboard
                 System.out.print("Enter the number of units consumed: ");
                    int units = scanner.nextInt();
                   double billAmount = 0.0;
                // Calculate the bill based on the tariff rates
    if (units <= 100) {
        billAmount = units * 1.50;
    } else if (units <= 300) {
        billAmount = (100 * 1.50) + ((units - 100) * 2.50);
    } else {
        billAmount = (100 * 1.50) + (200 * 2.50) + ((units - 300) * 4.00);
    }
  // Add the fixed charge to bill Amount
       System.out.println("Electricity Bill: " + billAmount);
    scanner.close();
}  }





Q3. Write a Java program that calculates the total cost of an order based on the number of items and a per-item cost that varies depending on the type of item.
Purse Rs 500, Laptop Bag Rs 1200 and Head Phone 1000.  If user enter any other number, print invalid order item.
import java.util.Scanner;
public class OrderItem
{
    public static void main(String[] args) {
    Scanner sc = new Scanner(System.in);
    System.out.println("Please enter the quantity of items in your order:");
     int quantity = sc.nextInt();
      System.out.println("Please enter the type of item in your order (1-3):1.Purse 2.Laptop bag 3.Head Phone");
        int itemType = sc.nextInt();
        double itemCost;
        switch (itemType) {
            case 1:
                itemCost = 500.0;
                break;
            case 2:
                itemCost = 1200.0;
                break;
            case 3:
                itemCost = 1000.0;
                break;
            default:
                System.out.println("Invalid item type. Enter the right one");
                  break;
        }
      double totalCost = quantity * itemCost;
       System.out.println("Your total cost is in Rs " + totalCost);
    } }



    
Q4. Write a program to find the factorial value of any number entered by the user. Input the first line contains integer T, total number of test cases. Then follow T lines, each line contains an integer N. Output display the factorial of the given number N.
import java.util.Scanner;
class factorial
{   public static void fact(int n)
    {
        int i,fact=1;
        for(i=1;i<=n;i++)
        {
           fact=fact*i;           }
          System.out.println(fact);     }
    public static void main(String[] args)
   {
    int n,num,i;
    Scanner sc = new Scanner(System.in);
   n=sc.nextInt();
   for(i=0;i<n;i++)
   {
    num=sc.nextInt();
    fact(num);
   } }  }
  Sample input
 2
5 8
Sample output
120
40320



Q5. A university maintains Library applications which keep track of the books or magazines the students read in every month using matrix form. A student visits the university library in the month of June, July, and August. He reads fiction, non-fiction books and magazines, both in paper copies and online. The library application shows how many different types of books and magazines the student read.  Use the information given below for better understanding:  
 
import java.util.Scanner;
class AddTwoMatrix
{
   public static void main(String args[])
   {
      int m, n, i, j;
      Scanner in = new Scanner(System.in);
      m=3;
      n=2;
      int first[][] = new int[m][n];
      int second[][] = new int[m][n];
      int sum[][] = new int[m][n];

      System.out.println("Enter the books which the student read in the month of June and it's matrix form is");
      for (i = 0; i < m; i++)
         for (j = 0; j < n; j++)
            first[i][j] = in.nextInt();

     System.out.println("Enter the books which the student read in the month of July and it's matrix form is");
        for (i = 0; i < m; i++)
          for (j = 0; j < n; j++)
             second[i][j] = in.nextInt();
   //Sum of matrices is: 
      for (i = 0; i < m; i++)
          for (j = 0; j < n; j++)
         sum[i][j] = first[i][j] + second[i][j];  
 
 System.out.println("Total number of different types of books and magazines he read is");
      for (i = 0; i < m; i++) 
      {
          for (j = 0; j < n; j++)
            System.out.print(sum[i][j]+"\t");
            System.out.println();
      }
       System.out.println("Total paper fiction books the student has read  " +sum[0][0]);
      System.out.println("Total online fiction books the student has read " +sum[0][1]);
      System.out.println("Total paper non-fiction books the student has read "+sum[1][0]);
      System.out.println("Total online non- fiction books the student has read " +sum[1][1]);
      System.out.println("Total papers the student has read " +sum[2][0]);
      System.out.println("Total  online magzines the student has read " +sum[2][1]);        
}  }




 
Q6) Presidency university stores the faculty details such as facid, facname, gender,course and date of joining.  Write a java application to store all the details using a constructor, parameterized constructor, and method to display the data.
import java.util.Scanner;
class faculty
{  int facid;
   String facname;
   String course;
   char gender;
   String doj;
   faculty()
   {
     facid=1001;
     facname="komal";
     course="java";
     gender ='f';
     doj="15/01/2025";    
   }
   faculty(int id, String name,String cour,char gen,String joining)
   {
     facid=id;
     facname=name;
     course=cour;
     gender =gen;
     doj=joining;
   }
   void display()
   {
     System.out.println(" Your id and name is  "+ facid +" "+facname);
     System.out.println(" Your are teaching "+course);
     System.out.println(" Your gender and date of joining "+gender + " "+doj);
   }
}
class FacList
{
  public static void main(String[] ar)
  {
  faculty obj= new faculty();
  obj.display();
  getData();
  }
  static void getData()
  {
    Scanner sc= new Scanner(System.in);
    int id; 
    String n,c,joiningdate;
    char g;
    System.out.println("Enter name,course,joingdate, gender and id");
    n=sc.nextLine();
    c=sc.nextLine();
    joiningdate=sc.nextLine();
    g= sc.next().charAt(0);
    id=sc.nextInt();
    faculty obj2=new faculty(id,n,c,g,joiningdate);
    obj2.display();
  }
} }}	




 
Q7) Presidency university stores the faculty details such as facid, facname, gender,course and date of joining.  Write a java application to store the faculty details using object Array.
import java.util.Scanner;
class faculty
{  int facid;
   String facname;
   String course;
   char gender;
   String doj;
   void getData()
   {
    Scanner sc= new Scanner(System.in);
    System.out.println("Enter name,course,joingdate, gender and id");
    facname=sc.nextLine();
    course=sc.nextLine();
    doj=sc.nextLine();
    gender= sc.next().charAt(0);
    facid=sc.nextInt();
    }
    void display()
   {
     System.out.println(" Your id and name is  "+ facid +" "+facname);
     System.out.println(" Your are teaching "+course);
     System.out.println(" Your gender and date of joining "+gender + " "+doj);
   }
}
class FacList2
{
  public static void main(String[] ar)
  { int i=0;
    Scanner sc1= new Scanner(System.in);
    System.out.println("How many faculty details do you want");
    int n=sc1.nextInt();
    faculty[] obj= new faculty[n];
    while(i<n)
    {
      obj[i]=new faculty();
      obj[i].getData();
      obj[i].display();
      i++;    }
  } }




  
 
Q8. An engineer wants to calculate the area of different shapes for the painting.  Write a java application to do the same with the help of overloading.
public class Overload 
{
	public void area(int a)
	{
		int result=a*a;
		System.out.println("Area of rectangle is"+result);
	}
	public void area(int a, int b)
	{
		int result=a*b;
		System.out.println("Area of square is"+result);
	}
	public void area(int b, float h)
	{
		float result=(0.5f)*b*h;
		System.out.println("Area of rectangle is"+result);
	}
	public static void main(String[] a)
	{
		Overload obj=new Overload();
		obj.area(10);
		obj.area(10,20);
		obj.area(10,12.3f); 	} 	}

     Output
Area of rectangle is  100
Area of square is  200
Area of rectangle is 61.5
Q9. Create a Class class called Rectangle and store length, width using constructor. Calculate the area using that. Create tabletop using rectangle class and calculate the cost of painting that table top.
import java.util.Scanner;
class Rectangle
{
protected double length, width;
protected double calcarea;
public Rectangle()
{
length = 0;
width = 0;
}
public void Area()
{
calcarea = length * width;
System.out.println(" Area is "+ calcarea);
}
}

class tabletop extends Rectangle
{
double cost;
public tabletop()
{
cost = 0;
}
public tabletop(double length, double width)
{
this.length = length;
this.width = width;
}
public void calcost()
{
Area ();
cost = 1000;
double totalcost = calcarea * cost;
System.out.println("Total cost is " + totalcost);
}
}
class Inheritance1
{
 public static void main(String[] ar)
{
 Scanner sc = new Scanner(System.in);
System.out.println(" Enter length and Width");
double l = sc.nextDouble();
double w = sc.nextDouble();
tabletop obj = new tabletop(l, w);
obj.calcost();
}
}






 
Q10. A company has two types of employees. 1. Salaried and 2.Daily wage. Salaried employees have their position and basic salary. Daily waged employees have basic and number of days worked. Accounts department wants to calculate the salary for both the type of employees and want to display all details about the employee. Write a code to implement this concept with the import java.util.Scanner;
class Emp
{
  int emp_id;
  String emp_name;
  protected Emp(int id, String name)
{
   this.emp_id = id;
   emp_name = name;
}
public void Print()
{
  System.out.println("Emp ID: " + emp_id);
   System.out.println("Emp Name: " + emp_name);
}
}
class salaried extends Emp
{
int basic;
String position;
 salaried(int id,String name,int basicsalary, String posi)
{
 super(id, name);
basic = basicsalary;
position = posi;
}
public void calculate()
{
float total =basic + (basic *0.3f) + (basic* 0.5f);
System.out.println(" Total salary is " + total);
}
public  void Print()
{
super. Print();
System.out.println(" Your position is" + position);
calculate();
}
}
class dailywage extends Emp
{
int basic;
int noofdays;
 dailywage(int id, String name, int basicsalary, int days) 
{
 super(id,name);
 basic = basicsalary;
 noofdays = days;
}
public void calculate()
{
float total = basic * noofdays;
System.out.println(" Total salary is " + total);
}
public  void Print()
{
super.Print();
System.out.println(" You have worked " + noofdays + "days");
calculate();
}
}
class Empdetails
{
public static void main(String[] a)
{
salaried obj1 = new salaried(1001, "Akshitha", 40000, "Manager");
obj1.Print();
dailywage obj2 = new dailywage(1002, "Raman", 15000, 25);
obj2.Print();
}
}
 
Q11. Write a program to create interface A in this interface we have two method meth1 and meth2. Implements this interface in another class named MyClass.
import java.util.Scanner;
interface A
{
 void add(int a,int b);
 void meth1();
}
interface B
{
  void sub(int a, int b);
}
class MyClass implements A,B
{
    int static Counter=0;
 static
{
   Counter++;
    System.out.println(“ Value of counter is”+ Counter);
   }
   public void add(int a,int b)
   {
      int result=a+b;
      System.out.println(" Result is "+ result);
   }
   public void meth1()
   {
     float area=3.14f*5.0f *5.0f;
     System.out.println("Area of circle " + area);
   }
   public void sub(int a,int b)
   {
      int result=a-b;
      System.out.println(" Result of subtraction  is "+ result);
   }
   public static void main(String[] ar)
   {
     MyClass obj= new MyClass();
     obj.meth1();
     obj.add(10,20);
     obj.sub(30,10);
    MyClass obj1= new MyClass();
     obj1.add(45,80);
      } }
 
Q12. Write a code to understand the concept of package.
         Inter1.java
       package myfirst1;
public interface inter1
{
   void add(int a,int b);
   default void disp()
   {
	   System.out.println("displaying data");
   }
   static void disp2()
   {
	   System.out.println("displaying data from static");
   }
}
Second.java
package myfirst1;
public class second implements inter1
{
	public static void main(String[] args) 
	{	second obj= new second();
		obj.add(100,20);
		obj.disp();
		inter1.disp2();

	}
	public void add(int a, int b)
	{
		int sum=a+b;
		System.out.println("sum is "+sum);
		
	}
	public void disp()
	   {
		   inter1.super.disp();
		   System.out.println("displaying data from second main ");
	   }   }
               sum is 120
    displaying data
    displaying data from second main 
    displaying data from static

