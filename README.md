using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace SoftUni_Logo
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int side = (12 * n - 6) / 2;
            int middle = 1;

            for (int i = 0; i < n * 2; i++)
            {
                Console.WriteLine("{0}{1}{0}", new string('.', side), new string('#', middle));
                side -= 3;
                middle += 6;
            }

            int left = 2;
            int right = 3;
            int downMiddle = 12 * n - 11;

            for (int i = 0; i < n - 1; i++)
            {
                Console.WriteLine("|{0}{1}{2}", new string('.', left), new string('#', downMiddle), new string('.', right));
                left += 3;
                right += 3;
                downMiddle -= 6;
            }
            for (int i = 0; i < n - 2; i++)
            {
                Console.WriteLine("|{0}{1}{2}", new string('.', left - 3), new string('#', downMiddle + 6), new string('.', right - 3));
            }
            Console.WriteLine("@{0}{1}{2}", new string('.', left - 3), new string('#', downMiddle + 6), new string('.', right - 3));

        }
    }
}
