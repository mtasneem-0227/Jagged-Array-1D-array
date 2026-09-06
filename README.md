# Jagged-Array-1D-array
Lab task 2
using System;

class Employee
{
    public int EmployeeID;
    public string Name;

    public Employee(int id, string name)
    {
        EmployeeID = id;
        Name = name;
        Console.WriteLine("Employee Constructor Called");
    }
}

class PermanentEmployee : Employee
{
    public double BasicSalary;
    public double Bonus;

    public PermanentEmployee(int id, string name, double basicSalary, double bonus)
        : base(id, name)
    {
        BasicSalary = basicSalary;
        Bonus = bonus;

        Console.WriteLine("PermanentEmployee Constructor Called");
    }

    public void Display()
    {
        Console.WriteLine("Employee ID: " + EmployeeID);
        Console.WriteLine("Name: " + Name);
        Console.WriteLine("Basic Salary: " + BasicSalary);
        Console.WriteLine("Bonus: " + Bonus);
        Console.WriteLine("Total Salary: " + (BasicSalary + Bonus));
    }
}

class Program
{
    static void Main()
    {
        PermanentEmployee emp = new PermanentEmployee(101, "Karim", 50000, 10000);

        emp.Display();
    }
}
