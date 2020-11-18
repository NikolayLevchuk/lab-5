# lab-5
Laboratorna 5
Variant 13
Дана квадратна матриця порядку M. Знайти суму елементів її 1)
головної; 2) побічної діагоналей.
*****************************************************************
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp14
{
    class Program
    {


        static void Main(string[] args)
        {
            Console.WriteLine("Вкажiть розмiрнiсть квадратноi матриці");
            string str = Console.ReadLine();
            int N = Convert.ToInt32(str);
            int[,] matrix = new int[N, N];
            int sum1 = 0; int sum2 = 0;

            Random rnd = new Random();
            for (int i = 0; i < N; i++)
            {
                for (int t = 0; t < N; t++)
                {
                    matrix[i, t] = rnd.Next(0, 10);
                    Console.Write(matrix[i, t] + "\t");
                }
                Console.WriteLine();
            }

            for (int i = 0; i < N; i++)
            {
                sum1 += matrix[i, i];
                sum2 += matrix[i, N - i - 1];
            }

            Console.WriteLine();
            Console.WriteLine("Cума головноi матрицi - " + sum1);
            Console.WriteLine("Cума побічноi матрицi - " + sum2);
            Console.ReadKey();
        }
    }
}
