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
