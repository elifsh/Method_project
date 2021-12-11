# Method_project
Fırat University Method Projects

### Kendisine parametre olarak gelen 2 tamsayının a üss b sini hesaplayıp geri döndüren methodu yazınız.

```java
import java.util.Scanner;

public class Main {
    
    public static int aussub(int a, int b) {
        int c=1;
        while (b!=0) {
            c = c*a;
            b--;
        }
        return c;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        System.out.println("Taban sayiyi giriniz");
        int a = sc.nextInt();
        System.out.println("Us olan sayiyi giriniz");
        int b = sc.nextInt();
        sc.close();

        int c = aussub(a, b);
        System.out.println("a ussu b sayisi:" + c);
    }
}

```

### Kendisine parametre olarak gelen n tamsayısı kadar adınızı ekrana yazan methodu yazınız.
```java
public class Main {
    
    public static void n_print(int n) {
        for (int i = 0; i < n; i++) {
            System.out.println("Elif");
        }
    }
    public static void main(String[] args) {
        n_print(8);
    }
}
```
### Kendisine parametre olarak gelen pozitif tamsayısının kaç basamaklı olduğunu geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static int basamak_sayisi(int sayi){
        int i = 0, basamak = 0;
        while (sayi != 0) {
            basamak += sayi%10;
            sayi /= 10;

            if (basamak!=0) {
                i++;
            } else {
                System.out.println("Sayi 1 basamaklidir.");
                break;
            }
        } if (i>0) {
            System.out.println("Sayi "+i+" Basamaklidir.");
        } else {
            System.out.println("Sayi 1 Basamaklidir.");
        }
        return i;
    }
    public static void main(String[] args) {
        Scanner sc =  new Scanner(System.in);
        System.out.println("Lutfen pozitif bir tamsayi giriniz:");
        int a = sc.nextInt();
        sc.close();
        basamak_sayisi(a);
    }
}
```
### n.fibonacci sayısını geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static int fibonacci(int n){
        int f = 0, f1 = 1, f2;
        if (n == 0) {
            return f;
        } for (int i = 2; i <= n; i++) {
            f2 = f + f1;
            f  = f1;
            f1 = f2;
        }
        return f1;   
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Sayi giriniz:");
        int n = sc.nextInt();
        sc.close();
        System.out.println(fibonacci(n));
        
    }
}

```
### Kendisine parametre olarak gelen pozitif tam sayının faktöriyelini alan methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static int factorial(int n){
        int f = 1;
        for (int i = n; i > 0; i--) {
            f*=i;
        }
        return f;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Sayi giriniz:");
        int n = sc.nextInt();
        sc.close();
        System.out.println(factorial(n));
    }
}
```
### Kendisine parametre olarak gelen tamsayıya kadar olan tüm tamsayıları toplayan methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static int sayiya_kadar_topla(int n){
        int top = 0;
        for (int i = n; i >= 0; i--) {
            top += i;
        }
        return top;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Sayi giriniz:");
        int n = sc.nextInt();
        sc.close();
        System.out.println(sayiya_kadar_topla(n));
    }
}
```
