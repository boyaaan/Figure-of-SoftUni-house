# -5.-Sword
using System;

class Program
{
    static void Main()
    {
        int n = int.Parse(Console.ReadLine());

        int wight = (2 * n) + 1;
        int sharp = n - 1;

        Console.WriteLine(@"{0}/^\{0}", new string('#', sharp));


        int spaces = (wight - (sharp * 2) + 2) / 2;
        spaces++;

        for (int i = 0; i < n / 2; i++)
        {
            sharp--;
            Console.WriteLine(@"{0}.{1}.{0}", new string('#', sharp), new string(' ', spaces));

            spaces += 2;

        }
        spaces -= 2;

        Console.WriteLine(@"{0}|{1}S{1}|{0}", new string('#', sharp), new string(' ', n / 2));
        Console.WriteLine(@"{0}|{1}O{1}|{0}", new string('#', sharp), new string(' ', n / 2));
        Console.WriteLine(@"{0}|{1}F{1}|{0}", new string('#', sharp), new string(' ', n / 2));
        Console.WriteLine(@"{0}|{1}T{1}|{0}", new string('#', sharp), new string(' ', n / 2));

        if (n == 4 || n == 5 || n == 6)
        {
            for (int i = 0; i < n / 2 - 1; i++)
            {

                Console.WriteLine(@"{0}|{1}|{0}", new string('#', sharp), new string(' ',spaces));

            }
        }
        else
        {
            for (int i = 0; i < n / 2; i++)
            {

                Console.WriteLine(@"{0}|{1}|{0}", new string('#', sharp), new string(' ', spaces));

            }
        }

        Console.WriteLine(@"{0}|{1}U{1}|{0}", new string('#', sharp), new string(' ', n / 2));
        Console.WriteLine(@"{0}|{1}N{1}|{0}", new string('#', sharp), new string(' ', n / 2));
        Console.WriteLine(@"{0}|{1}I{1}|{0}", new string('#', sharp), new string(' ', n / 2));

        Console.WriteLine(@"@{0}@", new string('=', wight - 2));

        if (n == 4 || n == 5 )
        {
            for (int i = 0; i < n / 2; i++)
            {

                Console.WriteLine(@"{0}|{1}|{0}", new string('#', n -1), new string(' ', n / 2 -1));

            }
            Console.WriteLine(@"{0}\{1}/{0}", new string('#', n - 1), new string('.', 1));

        }
        else
        {
            for (int i = 0; i < n / 2; i++)
            {

                Console.WriteLine(@"{0}|{1}|{0}", new string('#', n - 2), new string(' ', 3));

            }
            Console.WriteLine(@"{0}\{1}/{0}", new string('#', n - 2), new string('.', 3));

        }

    }
}

