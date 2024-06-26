# PRACTICE EXERCISE : Static Members
A company has 2 departments and it is growing, so more departments are needed.

The program you are given takes the number of departments to be opened as input, then takes their names and creates Department objects, passing their names as the constructor.

Complete the Department class to have 1 static member **depCount** with an initial value of 2 for the number of departments and the constructor that will count it and output corresponding message (see sample output).

**Sample Input**
2
Finance
Marketing

**Sample Output**
Department opened: Finance
Department opened: Marketing
Number of departments: 4

**Explanation**
The first input represents the number of departments to be opened, followed by their names.
As a result, the program outputs the corresponding messages (the 1st and the 2nd outputs) and the total number of departments: 2 (initial) + 2 (opened) = 4.

> You need to **increment the static number** of departments inside the constructor.

```cs
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading;
using System.Threading.Tasks;

namespace SoloLearn
{
    class Program
    {
        static void Main(string[] args)
        {
            int numOfDeps = Convert.ToInt32(Console.ReadLine());

            int count = 0;
            while (count < numOfDeps)
            {
                string depName = Console.ReadLine();
                Department dep = new Department(depName);
                count++;
            }

            Console.WriteLine("Number of departments: " + Department.depCount);
        }
    }
    class Department
    {
        
        public string depName;

        //declare static depCount member with value of 2

        //complete the constructor
        public Department(string name)
        {
            Console.WriteLine("Department opened: " + name);
            this.depName = name;
        }
    }
}
```