
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Grand_Theft_Examo
{
    class Grand_Theft_Examo
    {
        static void Main(string[] args)
        {
            byte escape_attempts = byte.Parse(Console.ReadLine());
            long sum_slaps = 0;
            long sum_escaped = 0;
            long sum_beers = 0;
            for (byte i = 0; i < escape_attempts; i++)
            {
                int thieves = int.Parse(Console.ReadLine());
                int beers = int.Parse(Console.ReadLine());
            
                if (thieves > 5)
                {
                    sum_slaps += 5;
                    sum_escaped += thieves - 5;  
                }
                else
                {
                    sum_slaps += thieves;
                }
                    
                sum_beers += beers;
            }
            long packs = sum_beers / 6;
            long bottles = sum_beers % 6;
            Console.WriteLine($"{sum_slaps} thieves slapped.");
            Console.WriteLine($"{sum_escaped} thieves escaped.");
            Console.WriteLine($"{packs} packs, {bottles} bottles.");

        }
    }
}
