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
