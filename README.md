# assignment2-Beeram

# Sai Kaushik Berram

## Paris

The **French** capital is one of the most **romantic** place in the Europe. With its abundance of **history**, there is so much to study and view in this city. There are so many different styles of **architecture**. It’s all so unique to Paris, and really makes the city so **unique** and **beautiful**. My favorite buildings include the **Cathédrale de Notre-Dame** and **the Hôtel Carnavalet**.

---

# Travel Destination
1. Maryville to Paris 
    1. Maryville to Kansas city (MCI)
    2. Kansas city (MCI) to Chicago (ORD)
    3. Chicago (ORD) to Paris (TYS)

- Clothes
- Shoes
- perfumes
- Watch

**[AboutMe](AboutMe.md)**

---
## Tables

This table shows the data related to my favourite food items. Which I would recommend others

|FOOD|LOCATION|AMOUNT|
|---|---|---|
|Biryani|Paradise|$20
|Pizza|Pizza Hut|$8|
|Chilli Chicken|Bhawarchi|$7.69
|Ice Cream|Cream Stone|$7

---

## Quotes

>If you set your goals ridiculously high and it's a failure, you will fail above everyone else's success. 
-*James Cameron*

>Life is what happens when you're busy making other plans. 
-*John Lennon*

---

## Code Fencing 

 int gcd (int a, int b) {  
     while (b) {  
         a %= b;  
         swap(a, b);  
     }  
     return a;  
 }  


> Stein’s algorithm or binary GCD algorithm is an algorithm that computes the greatest common divisor of two non-negative integers. Stein’s algorithm replaces division with arithmetic shifts, comparisons, and subtraction.

[Stein's algorithm](https://www.geeksforgeeks.org/steins-algorithm-for-finding-gcd/)

// Iterative Java program to
// implement Stein's Algorithm
import java.io.*;
 
class GFG {
 
 // Function to implement Stein's
    // Algorithm
    static int gcd(int a, int b)
    {
        // GCD(0, b) == b; GCD(a, 0) == a,
        // GCD(0, 0) == 0
        if (a == 0)
            return b;
        if (b == 0)
            return a;
 
        // Finding K, where K is the greatest
        // power of 2 that divides both a and b
        int k;
        for (k = 0; ((a | b) & 1) == 0; ++k)
        {
            a >>= 1;
            b >>= 1;
        }
 
        // Dividing a by 2 until a becomes odd
        while ((a & 1) == 0)
            a >>= 1;
 
        // From here on, 'a' is always odd.
        do
        {
            // If b is even, remove
            // all factor of 2 in b
            while ((b & 1) == 0)
                b >>= 1;
 
            // Now a and b are both odd. Swap
            // if necessary so a <= b, then set
            // b = b - a (which is even)
            if (a > b)
            {
                // Swap u and v.
                int temp = a;
                a = b;
                b = temp;
            }
 
            b = (b - a);
        } while (b != 0);
 
        // restore common factors of 2
        return a << k;
    }
 
    // Driver code
    public static void main(String args[])
    {
        int a = 34, b = 17;
 
        System.out.println("Gcd of given "
                           + "numbers is " + gcd(a, b));
    }
 }


[Code Source](https://www.geeksforgeeks.org/steins-algorithm-for-finding-gcd/)


