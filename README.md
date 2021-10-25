namespace _8_Magic_Sum
{
    using System;
    using System.Linq;
 
    public class Program
    {
        public static void Main()
        {
            int[] numbers = Console.ReadLine()
                .Split()
                .Select(int.Parse)
                .ToArray();
 
            int targetSumNumber = int.Parse(Console.ReadLine());
 
            for (int i = 0; i < numbers.Length-1; i++)
            {
                for (int j = i+1; j < numbers.Length; j++)
                {
                    if (numbers[i] + numbers[j] == targetSumNumber)
                    {
                        Console.WriteLine(numbers[i] + " " + numbers[j]);
                    }
                }
            }
        }
    }
}
