# Ex04-Constructor
## Aim:
 To write a C# program to calculate the salary of an employee by passing the name, designation, noofexperience, basic salary and insurance amount through constructor.
 
 ## Algorithm:
### Step 1:
Create a new Class named employee.
### Step 2:
Create a constructor

### Step 3:
Create two methods one is Salary & other is Display

### Step 4:
Create a main function and get name, designation, experience, basic salary and insurance amount from the User.

### Step 5:
Create a object and pass the input as parameters

### Step 6:
Call the salary method to calculate the salary

### Step 7:
Call the display method to display the details

### Step 8:
End of the Program.

 
 ## Program:
> Name: Subramaniya Pillai B

> Reg.no: 212221230109
 ```
 using System;
namespace Hello
{
    class Employee
    {
        public string name, designation;
        public int noofexperience, basicsalary, insurance;
        float hra, ta, gross_salary;
        public Employee(string name, string designation, int noofexperience, int basicsalary, int insurance)
        {
            this.name = name;
            this.designation = designation;
            this.noofexperience = noofexperience;
            this.basicsalary = basicsalary;
            this.insurance = insurance;
        }
        public void salary()
        {
            hra = (20 / 100) * this.basicsalary;
            ta = (10 / 100) * this.basicsalary;
            gross_salary = hra + ta + this.basicsalary - this.insurance;
        }
        public void display()
        {
            Console.WriteLine("Name of the employee is {0} having {1} of experience, working as {2}", this.name, this.noofexperience, this.designation);
            Console.WriteLine("Receives salary of {0}", gross_salary);
        }
        public static void Main(String[] args)
        {
            Employee emp1 = new Employee("Saravana", "Tester", 2, 40000, 1000);
            Employee emp2 = new Employee("Paul", "Developer", 3, 35000, 1000);
            emp1.salary();
            emp2.salary();
            emp1.display();
            emp2.display();
        }
    }
}
 ```
 ## Output:
 ![Alt text](image.png)
 ## Result:
Hence, a C# program to calculate the salary of an employee by passing the name, designation, years of experience, basic salary and insurance amount through constructor is executed successfully
