# OperationsBeteenNumbers

import  java.util.Scanner;

public class P41_OperationsBeteenNumbers {

    public static void main(String[] args) {
        Scanner console = new Scanner(System.in);
        int n1 = Integer.parseInt(console.nextLine());
        int n2 = Integer.parseInt(console.nextLine());
        String operator = console.nextLine();
        double result = 0;
        String evenOdd = "";

        if (operator.equalsIgnoreCase("+") || operator.equalsIgnoreCase("-") || operator.equalsIgnoreCase("*")) {
            if (operator.equalsIgnoreCase("+")) {
                result = n1 + n2;
                if (result % 2 == 0) {
                    evenOdd = "even";
                } else {
                    evenOdd = "odd";
                }
            } else if (operator.equalsIgnoreCase("-")) {
                result = n1 - n2;
                if (result % 2 == 0) {
                    evenOdd = "even";
                } else {
                    evenOdd = "odd";
                }
            } else if (operator.equalsIgnoreCase("*")) {
                result = n1 * n2;
                if (result % 2 == 0) {
                    evenOdd = "even";
                } else {
                    evenOdd = "odd";
                }
            }
            System.out.printf("%d %s %d = %.0f - %s", n1, operator, n2, result, evenOdd);
        } else if (operator.equalsIgnoreCase("/")) {
            if (n2 == 0) {
                System.out.printf("Cannot divide %d by zero", n1);
            } else {
                result = n1 * 1.00 / n2;
                System.out.printf("%d %s %d = %.2f", n1, operator, n2, result);
            }
        } else if (operator.equalsIgnoreCase("%")) {
            if (n2 == 0) {
                System.out.printf("Cannot divide %d by zero", n1);
            } else {
                result = n1 * 1.00 % n2;
                System.out.printf("%d %s %d = %.0f", n1, operator, n2, result);
            }
        }
    }

}
