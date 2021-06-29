using System;
using System.Collections.Generic;

namespace List2
{
    public class Program
    {
        public static void Main()
        {
            // Create Student Objects
            Student stud1 = new Student()
            {
                ID = 101,
                Name = "Erika Tecson",
                Gender = "Female",
                Grade = 89
            };
            Student stud2 = new Student()
            {
                ID = 102,
                Name = "Jhyzel Orcega",
                Gender = "Female",
                Grade = 90
            };
            Student stud3 = new Student()
            {
                ID = 103,
                Name = "Elton John Navarro",
                Gender = "Male",
                Grade = 92
            };
            Student stud4 = new Student ()
            {
                ID = 104,
                Name = "Jerrica Fernandez",
                Gender = "Female",
                Grade = 90
            };
            
            // Create a List of Employees
            List<Student> listStudent = new List<Student>();
            
            listStudent.Add(stud1);
            listStudent.Add(stud2);
            listStudent.Add(stud3);
            listStudent.Add(stud4);
            // The List index is also 0 based.
            Student stud = listStudent[0];

            Console.WriteLine("First Student and her Name, Gender and Grade");
            Console.WriteLine("ID = {0}, Name = {1}, Gender = {2}, Grade = {3}",
                     stud.ID, stud.Name, stud.Gender, stud.Grade);
            Console.WriteLine();
            
            // retrieving the list using for loop
            Console.WriteLine("Other Students and their Names, Gender and Grade");
            for (int i = 0; i < listStudent.Count; i++)
            {
                Student students = listStudent [i];
                Console.WriteLine("ID = {0}, Name = {1}, Gender = {2}, Grade = {3}",
             students.ID, students.Name, students.Gender, students.Grade);
            }
            Console.WriteLine();

           
        }
    }
    public class Student
    {
        public int ID { get; set; }
        public string Name { get; set; }
        public string Gender { get; set; }
        public int Grade { get; set; }
    }
}
