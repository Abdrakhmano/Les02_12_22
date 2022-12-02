### Task №1 (6kyu)

Digital root is the recursive sum of all the digits in a number.

Given n, take the sum of the digits of n. If that value has more than one digit, continue reducing in this way until a single-digit number is produced. The input will be a non-negative integer.

~~~ Java
Examples
16  -->  1 + 6 = 7
942  -->  9 + 4 + 2 = 15  -->  1 + 5 = 6
132189  -->  1 + 3 + 2 + 1 + 8 + 9 = 24  -->  2 + 4 = 6
493193  -->  4 + 9 + 3 + 1 + 9 + 3 = 29  -->  2 + 9 = 11  -->  1 + 1 = 2
~~~

[Task_link](https://www.codewars.com/kata/541c8630095125aba6000c00/train/java)


#### Solution

~~~ Java
public class DRoot {
    public static int digital_root(int n) {
        int result = 0;
        while (n > 0 || result > 9) {
            if (n == 0) {
                n = result;
                result = 0;
            }
            result += n % 10;
            n /= 10;
        }
        return result;
    }
}
~~~

#### Fav Solution

~~~ Java
public class DRoot {
  public static int digital_root(int n) {
    return (n != 0 && n%9 == 0) ? 9 : n % 9;
  }
}
~~~

### Task №2 (7kyu)

Find the total sum of internal angles (in degrees) in an n-sided simple polygon. N will be greater than 2.

[Task_link](https://www.codewars.com/kata/5a03b3f6a1c9040084001765)


#### Solution

~~~ Java
public class AngleSum {
    public static int sumOfAngles(int n) {
        return (n - 2) * 180;
    }
}

~~~

#### Fav Solution

~~~ Java
public class AngleSum {
  public static int sumOfAngles(int n) {
    return 180 * (n-2);
  }
}
~~~

