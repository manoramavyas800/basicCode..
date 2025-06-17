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
