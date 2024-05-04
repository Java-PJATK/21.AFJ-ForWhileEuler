# AFJ-ForWhileEuler
Listing 21 AFJ-ForWhileEuler/ForWhileEuler Page 42

Cont. from 

In the next example, we use while- and for-loops to calculate Euler’s totient function φ(n) — this is the number of positive integers up to a given integer n that are relatively prime to n (for example, φ(10) = 4, as there are 4 natural numbers that are smaller than 10 and relatively prime to it: 1, 3, 7, and 9.

## Listing 21 AFJ-ForWhileEuler/ForWhileEuler.java

```java
import java.util.Scanner;
/*
 * Finding and printing values of Euler's totient
 * function, i.e., number of positive integers up
 * to a given integer n that are relatively prime to n.
 */

public class ForWhileEuler {
    public static void main(String[] args) {
        Scanner scan = new Scanner(System.in);

        while (true) {
            System.out.print(
                "\nEnter a natural number (0 to exit) -> ");
            int n = scan.nextInt();

            if (n == 0) break;

            int count = 0;
            for (int p = 1; p <= n; ++p) {
                int a = n, b = p;
                  // Euclid's algorithm for GCD
                while (a != b) {
                    if (a > b) a -= b;
                    else       b -= a;
                }
                if (a == 1) ++count;
            }
            System.out.print("\u03c6(" + n + ") = " + count);
        }
    }
}
```

The program prints, for example:

```
$ Enter a natural number (0 to exit) -> 54
φ(54) = 18
$ Enter a natural number (0 to exit) -> 10
φ(10) = 4
$ Enter a natural number (0 to exit) -> 111222
φ(111222) = 35856
$ Enter a natural number (0 to exit) -> 0
$
```

Next Section 6. Static functions Listing 22 CYS-PassArr/PassArr.java
