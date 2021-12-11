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
### Kendisine parametre olarak gelen iki tamsayıdan büyük olanı geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static int print_enb(int a, int b){
        int enb = 0;
        if (a>b) {
            enb = a;
        } else if(b>a) {
            enb = b;
        } else {
            enb = a;
        }
        return enb;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.print("Sayi Giriniz: ");
        int a = sc.nextInt();
        System.out.print("Sayi Giriniz: ");
        int b = sc.nextInt();
        sc.close();
        System.out.println("Buyuk Sayi: " + print_enb(a, b));
    }
}
```
### Kendisine parametre olarak gelen Stringteki küçük karakterlerin sayısını geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String numbers_of_lowercase_char(String str){
        int sayac = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i)>=97 && str.charAt(i)<=122) {
                sayac++;
            }
        }
        String num = Integer.toString(sayac);
        return num;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println("Kucuk Karakterlerin Sayisi: " + numbers_of_lowercase_char(str));
    }
}
```
### Kendisine parametre olarak gelen Stringi ters çevirip geri döndüren methodu yazınız.
```java

```
### Kendisine parametre olarak gelen Stringteki küçük karakterleri büyük yapan sonucu geri döndüren methodu yazınız.
```java

```
