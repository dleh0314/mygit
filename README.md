import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] callList = new int[n];

        for (int i = 0; i < n; i++) {
            callList[i] = sc.nextInt();
        }

        int a = 0;
        int b = 0;

        for (int callTime : callList) {
            a += (callTime / 30 + 1) * 10;
            b += (callTime / 60 + 1) * 15;
        }

        if (a < b) {
            System.out.println("Y " + a);
        } else if (a > b) {
            System.out.println("M " + b);
        } else {
            System.out.println("Y M " + a);
        }

        sc.close();
    }
}
