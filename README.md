# basicCode..
//SUM NTH NATURAL NUMBER.
import java.util.Scanner;

public class TestClass {
    static int SumNthNum(int n) {
        //sum of n natural number.
        int sum=n*(n+1)/2;
        return sum;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        System.out.println(SumNthNum(n));
    }
}
//FIND NTH TERM OF ARITHMETIC PROGRESSION
import java.util.Scanner;

public class TestClass {
    static int AP(int n,int a,int d) {
        //ARITHMETIC PROGRESSION
        int AP=a+(n-1)*d;
        return AP;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a = sc.nextInt();
        int d = sc.nextInt();

        System.out.println(AP(n,a,d));
    }
}
//FIND THE NTH TERM OF GEOMETRIC PROGRESSION
import java.util.Scanner;

public class TestClass {
    static int AP(int n,int a,int r) {
        //ARITHMETIC PROGRESSION
        int GP=a*(int)Math.pow(r,(n-1));
        return GP;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int a = sc.nextInt();
        int r = sc.nextInt();

        System.out.println(AP(n,a,r));
    }
}
//FIND LCM.

import java.util.Scanner;

    public class Lcm {
        public static void main(String[] args) {
            Scanner sc = new Scanner(System.in);
           int n = sc.nextInt();
           int m = sc.nextInt();
           int lcm=1;
           for (int i = Math.max(n,m); i <= n*m; i++) {
               if (i%n == 0&& i%m == 0) {
                   lcm=i;
                   break;
               }
           }
           System.out.println(lcm);
           sc.close();

        }

    }
    //COUNT DISTINCT ELEMENTS

    
import java.util.Scanner;

public class Socialnetwork {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        int[] arr = new int[t];
        int count = 0;

        for (int i = 0; i < t; i++) {
            arr[i] = sc.nextInt();
        }
        for (int i = 0; i < t; i++) {
            boolean flag = true;
            for (int j = i - 1; j >= 0; j--) {
                if (arr[i] == arr[j]) {
                    flag = false;
                    break;
                }
            }
            if (flag) {
                count++;
            }
        }
            System.out.println(count);

    }
}
//MAX IN AN ARRAY.

import java.util.Scanner;

public class Socialnetwork {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int t = sc.nextInt();
        int[] arr = new int[t];
         boolean flag = true;
        for (int i = 0; i < t; i++) {
            arr[i] = sc.nextInt();
        }
        for (int i = 1; i <t; i++) {
            if (arr[i - 1] > arr[i]) {
                flag = false;
                break;
            }
        }
        if (flag) {
            System.out.println("YES");
        }else{
            System.out.println("NO");
        }

    }
}
//Panagram Checking in Java

import java.util.Scanner;

public  class TestClass {
   static boolean isPanagram(String a) {
       int n = a.length();
       if (n < 26) return false;
       boolean[] valid = new boolean[26];
       for (int i = 0; i < n; i++) {
           char c = a.charAt(i);

           if (c >= 'a' && c <= 'z') {
               valid[c - 'a'] = true;
           }
           if (c >= 'A' && c <= 'Z') {
               valid[c - 'A'] = true;
           }
       }
       for (int i = 0; i < 26; i++) {
           if (!valid[i]) return false;
       }

    return true;

   }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       String a = sc.nextLine();
        System.out.println(isPanagram(a));
    }
}
//Extracting Digits After the Decimal Point

import java.util.Scanner;

public  class TestClass {
  static String digitChack(String n){
      int position=n.indexOf('.');
      if(position<0){
          return " ";
      }else{
          return n.substring(position+1);
      }
   }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
       String a = sc.nextLine();
      String ans= digitChack(a);
      System.out.println(ans);
    }
}
//missmatuch charcaters

import java.util.Arrays;
import java.util.Scanner;

public class Main {
     static char function(String a, String b) {
         char[] a1=a.toCharArray();
         Arrays.sort(a1);
         char[] a2=b.toCharArray();
         Arrays.sort(a2);
         for(int i=0;i<a1.length;i++){
             if(a1[i]!=a2[i]){
                 return a2[i];
             }
         }
         return a2[a1.length];
     }
    public static void main(String[] args) {
       Scanner sc = new Scanner(System.in);
     String a = sc.nextLine();
     String b = sc.nextLine();
     System.out.println(function(a,b));
}
}
//First Digit of a Number

import java.util.Scanner;

public class CodeforcesQus {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();

        n=Math.abs(n);
        while (n>=10) {
          n/=10;
        }
        System.out.println(n);
    }
}
//Check for Anagram(they are just permutations of each other).

import java.util.Arrays;
import java.util.Scanner;

public class Recorsion {
    static boolean anagram(String a, String b) {
        if(a.length() != b.length()) return false;
        char[] a1=a.toCharArray();
        Arrays.sort(a1);
        a=new String(a1);
        char[] a2=b.toCharArray();
        Arrays.sort(a2);
        b=new String(a2);
        return a.equals(b);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String a = sc.nextLine();
        String b = sc.nextLine();
        System.out.println(anagram(a,b));

    }
}
//Time Complexity: O(N*logN)
//Auxiliary Space: O(1)

//second mathods.

import java.util.Scanner;

public class Recorsion {
    static boolean anagram(String a, String b) {
        int p = 256;
        if(a.length() != b.length()) return false;
        char[] chars = new char[p];
        for(int i = 0; i < a.length(); i++) {
            chars[a.charAt(i)]++;
            chars[b.charAt(i)]--;
        }
        for(int i = 0; i < p; i++) {
            if(chars[i] != 0) return false;
        }
        return true;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String a = sc.nextLine();
        String b = sc.nextLine();
        System.out.println(anagram(a,b));
    }
}
//Time Complexity: O(N)
//Auxiliary Space: O(256)

//convert decimal number to binary number.

import java.util.Scanner;

public class CodeforcesQus {
    public static String toBinary(int n) {
        StringBuilder sb=new StringBuilder();
        while(n>0){
            sb.append(n%2);
            n/=2;
        }
        return sb.reverse().toString();
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        String s = toBinary(n);
        System.out.println(s);
    }
}
//CONVERT BINARY TO DECIMAL.

import java.util.Scanner;

public class CodeforcesQus {
    static void byTOdec(String str){
        int k=1;
        int m=0;
        for(int i=str.length()-1;i>=0;i--){
            m+=(str.charAt(i)-'0')*k;
            k*=2;
        }
        System.out.println(m);
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String str = sc.nextLine();
        byTOdec(str);
    }
}
//Armstrong number .

import java.util.Scanner;

public class Main {
    static int countDigits(int number) {
        int count = 0;
        while (number > 0) {
            number = number / 10;
            count++;
        }
        return count;
    }
    static int Armstrong(int number) {
        int sum = 0;
        int digits=countDigits(number);
        while (number > 0) {
            int digit = number % 10;
            sum +=Math.pow(digit,digits) ;
            number = number / 10;

        }
        return sum;
    }
            public static void main(String[] args) {
               Scanner sc = new Scanner(System.in);
              int n=sc.nextInt();
              int m=Armstrong(n);
              System.out.println(m);
              if(n==m){
                  System.out.println("YES");
              }else{
                  System.out.println("NO");
              }
            }
        }
