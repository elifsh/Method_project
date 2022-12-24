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
        } for (int i = 1; i <= n; i++) {
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
import java.util.Scanner;
public class Main {
    public static  String reverse_String(String str){
        String temp = " " ;
        char[] ch = str.toCharArray();
        for (int i = ch.length-1; i >= 0; i--) {
            temp += ch[i];
        }
        return temp;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println("Ters Cevirilmis Kelime: " + reverse_String(str));
    }
}
```
### Kendisine parametre olarak gelen Stringteki küçük karakterleri büyük yapan sonucu geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String to_uppercase(String str){
        String temp = "";
        for (int i = 0; i < str.length(); i++) {
            char ch = str.charAt(i);
            ch = (char)(ch-32); 
            temp += ch;
        } 
        return temp;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println(to_uppercase(str));
    }
}
```
### Kendisine parametre olarak gelen Stringteki küçük karakterleri büyük, büyük karakterleri küçük yapıp sonucu geri döndüren methodu yazınız. 
```java
import java.util.Scanner;
public class Main {
    public static  String uppercase_lowercase(String str){
        String temp = "";
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i)>=65 && str.charAt(i)<=90) {
                char ch = str.charAt(i);
                ch = (char)(ch+32); 
                temp += ch;
            }
            else if (str.charAt(i)>=97 && str.charAt(i)<=122) {
                char ch = str.charAt(i);
                ch = (char)(ch-32); 
                temp += ch;
            }
        } 
        return temp;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println(uppercase_lowercase(str));
    }
}
```
### Kendisine parametre olarak gelen Stringteki "aa" Stringlerinden kaç tane olduğunu geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String aa_control(String str){
        int sayac = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i)=='a' && str.charAt(i+1)=='a') {
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
        System.out.println(aa_control(str));
    }
}
``` 
### Kendisine parametre olarak gelen iki Stringten büyük olanı geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String enb_str(String str, String str1){
        int enb_str = 0 ;
        String enbStr = "";
        char [] ch = str.toCharArray();
        char [] ch1 = str1.toCharArray();
        int str_size = 0, str1_size = 0;
        for (int i = 0; i < ch.length; i++) {
            str_size += ch[i];
        } for (int i = 0; i < ch1.length; i++) {
            str1_size += ch1[i]; 
        } if (str_size>str1_size) {
            enb_str = str_size;
            enbStr += str;
        } else if (str_size < str1_size) {
            enb_str = str1_size;
            enbStr += str;
        } else {
            System.out.println("Iki String Esit Buyuklukte: " + str + "==" + str1);
        }
        String temp = "En buyuk olan : " + enbStr+ " |" + " Buyuklugu: " + enb_str;
        return temp;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        System.out.println("Kelime giriniz: ");
        String str1 = sc.nextLine();
        sc.close();
        System.out.println(enb_str(str,str1));
    }
}
```
### Kendisine parametre olarak gelen Stringteki kelime sayısını geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String word_num(String str) {
        char temp = ' ';
        int sayac = 0;
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == temp) {
                sayac++;
            }
        }
        String empty = "Kelime Sayisi: " + (sayac+1);
        return empty;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("String giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println(word_num(str));
    }
}
```
### Kendisine parametre olarak gelen Stringte 'a' karakterinin olup olmadığını geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String a_control(String str) {
        boolean b = true;
        String a = "";
        for (int i = 0; i < str.length(); i++) {
            if (str.charAt(i) == 'a') {
                b = true;
            } else {
                b = false;
            }
        } if (b == true) {
            a = "'a' karakteri var | " + str;
        } else {
            a = "'a' karakteri yok | " + str;
        }
        return a;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println(a_control(str));
    }
}
```
### Kendisine parametre olarak gelen Stringin palindrom olup olmadığını geri döndüren methodu yazınız.
```java
import java.util.Scanner;
public class Main {
    public static  String str_palindrome(String str) {
        String temp = "" ;
        String p = "";
        char[] ch = str.toCharArray();
        for (int i = ch.length-1; i >= 0; i--) {
            temp += ch[i];
        } if (str.equalsIgnoreCase(temp)) {
            p = "String Palindromdur. | " + str + " == " + temp;
        } else {
            p = "String Palindrom Degildir. | " + str + " != " + temp;
        }
        return p;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Kelime giriniz: ");
        String str = sc.nextLine();
        sc.close();
        System.out.println(str_palindrome(str));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisinin toplamını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int array_sum(int [] arr) {
        int sum = 0;
        for (int i = 0; i < arr.length; i++) {
            sum += arr[i];
        }
        return sum;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println("Dizi elemanlari toplami: " + array_sum(arr));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisindeki en küçük elemanın indisini geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int array_sum(int [] arr) {
        int enk = arr[0], enk_d = 0;
        for (int i = 1; i < arr.length; i++) {
            if (enk>arr[i]) {
                enk = arr[i];
                enk_d = i;
            }
        }
        return enk_d;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println("Tamsayi dizisindeki en kucuk  sayinin indisi: "+ array_sum(arr));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisinin sıralı olup olmadığını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int array_sort_control(int [] arr) {
        boolean b = true;
        int enk = arr[0];
        for (int i = 1; i < arr.length-1; i++) {
            if (enk >= arr[i]) {
                b = false;
                break;
            } else {
                b = true;
            }
            enk = arr[i];
        } if (b == true) {
            System.out.println("Tamsayi dizisi Siralidir..");
            return 1;
        } else {
            System.out.println("Tamsayi dizisi Sirali degildir..");
            return 0;
        }
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println(array_sort_control(arr));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisinin her elemanını 1 arttırıp geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int[] array_plus_one(int [] arr) {
        for (int i = 0; i < arr.length; i++) {
            arr[i]+=1;
        }
        return arr;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println(Arrays.toString(array_plus_one(arr)));
    }
}
```
### Kendisine parametre olarak gelen String dizisindeki en uzun Stringin olduğu indisi geri döndüren methodu yazınız.
```java
import java.util.Arrays;
public class Main {
    public static  int string_lengths(String [] str) {
        int enb = str[0].length();
        int enb_d = 0; 
        for (int i = 0; i < str.length; i++) {
            if (enb < str[i].length()) {
                enb = str[i].length();
                enb_d = i;
            }
        }
        return enb_d;
    }
    public static void main(String[] args) {
        String [] str = {"Ali","Ayse","el","ele"};
        System.out.println(Arrays.toString(str));
        System.out.println("Uzunlugu en fazla olan elemanin indisi: " + string_lengths(str));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisindeki en büyük ikinci sayıyı geri dönrüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int  print_enb2(int [] arr) {
        Arrays.sort(arr);
        int enb2 = arr[arr.length-2];
        return enb2;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println(print_enb2(arr));
    }
}
```
### Kendisine parametre olarak gelen tamsayı dizisindeki en büyük ve en küçük sayıyı geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  String  print_enb_enk(int [] arr) {
        Arrays.sort(arr);
        int enb = arr[arr.length-1];
        int enk = arr[0];
        String temp = "Dizideki En buyuk sayi: " + enb + " | Dizideki En kucuk sayi: " + enk;
        return temp;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] arr = new int[10];
        for (int i = 0; i < arr.length; i++) {
            arr[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(arr));
        System.out.println(print_enb_enk(arr));
    }
}
```
### Vize ve final notlarının bulunduğu iki diziyi parametre olarak alıp öğrencilerin ortalamasını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  String  score_average(int [] Vize, int [] Final) {
        int [] ort = new int[10];
        for (int i = 0; i < ort.length; i++) {
            ort[i]=(Vize[i]+Final[i])/2;
        }
        String temp = Arrays.toString(ort);
        return temp;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] Vize = new int[10];
        int [] Final = new int[10];

        for (int i = 0; i < Vize.length; i++) {
            Vize[i] = r.nextInt(100)+1;
        }
        for (int i = 0; i < Final.length; i++) {
            Final[i] = r.nextInt(100)+1;
        }
        System.out.println("Vize Notlari:     " + Arrays.toString(Vize));
        System.out.println("Final Notlari:    " + Arrays.toString(Final));
        System.out.println("Not Ortalamalari: " + score_average(Vize,Final));
    }
}
```
### Kendisine parametre olarak gelen iki boyutlu tamsayı dizisindeki en büyük sayıyı geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class methods_projects {
    public static  int  print2d_enb(int [][] arr) {
        int enb = arr[0][0];
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                if (enb < arr[i][j]) {
                    enb = arr[i][j];
                }
            }
        }
        return enb;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [][] arr = new int[10][10];
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                arr[i][j] = r.nextInt(100)+1;
            }
        } for (int[] i : arr) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("Dizideki en buyuk eleman: " + print2d_enb(arr));
    }
}
```
### Bir önceki sorudaki en büyük elemanın indisini döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  String  print2d_enb(int [][] arr) {
        int enb = arr[0][0];
        String enb_d = " ";
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                if (enb < arr[i][j]) {
                    enb = arr[i][j];
                    enb_d = "En büyük elemanin indisleri: "+"|i = "+ i +" ,"+" j = " + j + "|"; 
                }
            }
        }
        return enb_d;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [][] arr = new int[10][10];
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                arr[i][j] = r.nextInt(100)+1;
            }
        } for (int[] i : arr) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("Dizideki en buyuk eleman: " + print2d_enb(arr));
    }
}
```
### İki önceki sorudaki her bir satırın toplamını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static String  print_row_sum(int [][] arr) {
        int top = 0;
        for (int i = 0; i < arr.length; i++) {
            top = 0;
            for (int j = 0; j < arr[0].length; j++) {
                top += arr[i][j];
            }
            System.out.println((i+1)+". satirin toplami: "+ top);  
        }
        return "";
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [][] arr = new int[10][10];
        for (int i = 0; i < arr.length; i++) {
            for (int j = 0; j < arr.length; j++) {
                arr[i][j] = r.nextInt(100)+1;
            }
        } for (int[] i : arr) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println(print_row_sum(arr));
    }
}
```
### Kendisine parametre olarak gelen iki boyutlu String dizisindeki en uzun Stringi geri döndüren methodu yazınız.
```java
import java.util.Arrays;
public class Main {
    public static  String string_2d_lengths(String [][] str) {
        int enb = str[0][0].length();
        String enb_d = ""; 
        for (int i = 0; i < str.length; i++) {
            for (int j = 0; j < str.length; j++) {
                if (enb < str[i][j].length()) {
                    enb = str[i][j].length();
                    enb_d = str[i][j];
                }
            }
        }
        return enb_d;
    }
    public static void main(String[] args) {
        String [][] str = {{"Ali","Ayse","el","ele"},{"elay","elay","ey","yey"},{"umbirirrella","ayy","ayy","jdk"}};
        for (String [] i : str) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("Uzunlugu en fazla olan eleman: " + string_2d_lengths(str));
    }
}
```
### Kendisine parametre olarak gelen 3x3'lük A ve B matrislerinin toplamını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int[][] matris_sum(int [][] A, int [][] B) {
        int[][] sum = new int[3][3];
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A.length; j++) {
                sum[i][j] = A[i][j] + B[i][j];
            }
        }
        return sum;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [][] A = new int[3][3];
        int [][] B = new int[3][3]; 
        
        for (int i = 0; i < A.length; i++) {
            for (int j = 0; j < A.length; j++) {
                A[i][j] = r.nextInt(10)+1;
                B[i][j] = r.nextInt(10)+1;
            }
        }
        System.out.println("A matrisi: ");
        for (int [] i : A) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("B matrisi: ");
        for (int [] i : B) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("Matrisler Toplami: ");
        for (int [] i : matris_sum(A, B)) {
            System.out.println(Arrays.toString(i));
        }
    }
}
```
### Kendisine parametre olarak gelen 10 elemanlı tamsayı dizisini 1 sağa döndüren ve diziyi ana methoda geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int[] shifted_array(int [] A) {
        int A_temp = A[A.length-1];
        for (int i = A.length-2; i >= 0; i--) {
            A[i+1] = A[i];
        }
        A[0] = A_temp;
        return A;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int []A = new int[10];
        for (int i = 0; i < A.length; i++) {
            A[i] = r.nextInt(10)+1;
        }
        System.out.println(Arrays.toString(A));
        System.out.println(Arrays.toString(shifted_array(A)));
    }
}
```
### 10 elemanlı 2 tamsayı dizisinin toplamını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int[] sum_array(int [] A, int [] B) {
        int [] sum = new int[10];
        for (int i = 0; i < sum.length; i++) {
            sum[i] = A[i] + B[i];
        }
        return sum;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] A = new int[10];
        int [] B = new int[10];
        for (int i = 0; i < A.length; i++) {
            A[i] = r.nextInt(10)+1;
            B[i] = r.nextInt(10)+1;
        }
        System.out.println("A dizisi: " + Arrays.toString(A));
        System.out.println("B dizisi: " + Arrays.toString(B));
        System.out.println("Diziler toplami: " + Arrays.toString(sum_array(A,B)));
    }
}
```
### Kendisine parametre olarak gelen sayının asal olup olmadığını geri döndüren methodu yazınız.
```java
import java.util.Random;
public class Main {
    public static  boolean prime_number(int n) {
        int sayac = 0;
        boolean b = true;
        for (int i = 2; i < Math.sqrt(n); i++) {
            if (n%i == 0) {
                sayac++;
            }
        } if (sayac == 0) {
            b = true;
        } else {
            b = false;
        }
        return b;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int n = r.nextInt(1000)+1;
        System.out.println(n +" sayisi asal mi? " + prime_number(n));
    }
}
```
### Kendisine parametre olarak gelen 10 elemanlı tamsayı dizisindeki tek olanların ortalamasını geri döndüren methodu yazınız.
```java
import java.util.Arrays;
import java.util.Random;
public class Main {
    public static  int sum_of_odd_number(int [] A) {
        int sum_odd = 0;
        for (int i = 0; i < A.length; i++) {
            if (A[i]%2!=0) {
                sum_odd += A[i];
            }
        }
        return sum_odd;
    }
    public static void main(String[] args) {
        Random r = new Random();
        int [] A = new int[10];
        for (int i = 0; i < A.length; i++) {
            A[i] = r.nextInt(100)+1;
        }
        System.out.println(Arrays.toString(A));
        System.out.println("Dizi icindeki tek elemanlarin toplami: " + (sum_of_odd_number(A)));
    }
}
```
### Kendisine parametre olarak gelen iki boyutlu String dizisi içindeki en uzun karaktere sahip olan Stringi ve yerini(satır,sütun) geri döndüren methodu yazınız.
```java
import java.util.Arrays;
public class Main {
    public static  String string_2d_lengths(String [][] str) {
        int enb = str[0][0].length();
        String enb_d = ""; 
        for (int i = 0; i < str.length; i++) {
            for (int j = 0; j < str.length; j++) {
                if (enb < str[i][j].length()) {
                    enb = str[i][j].length();
                    enb_d = str[i][j] + "\nEn uzun Stringin bulundugu yer: " + "|i = " + i + " ," + " j = " + j + "|";  ;
                }
            }
        }
        return enb_d;
    }
    public static void main(String[] args) {
        String [][] str = {{"Ali","Ayse","el","ele"},{"elay","elay","ey","yey"},{"umbirirrella","ayy","ayy","jdk"}};
        for (String [] i : str) {
            System.out.println(Arrays.toString(i));
        }
        System.out.println("Uzunlugu en fazla olan eleman: " + string_2d_lengths(str));
    }
}
```
