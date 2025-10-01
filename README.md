import java.util.Scanner;

public class BasicCalculator {

    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        double num1, num2, result;
        char operator;

        System.out.println("Enter first number:");
        num1 = input.nextDouble();

        System.out.println("Enter second number:");
        num2 = input.nextDouble();

        System.out.println("Choose an operator: +, -, *, or /");
        operator = input.next().charAt(0);

        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println(num1 + " + " + num2 + " = " + result);
                break;

            case '-':
                result = num1 - num2;
                System.out.println(num1 + " - " + num2 + " = " + result);
                break;

            case '*':
                result = num1 * num2;
                System.out.println(num1 + " * " + num2 + " = " + result);
                break;

            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println(num1 + " / " + num2 + " = " + result);
                } else {
                    System.out.println("Error: Division by zero is not allowed.");
                }
                break;

            default:
                System.out.println("Invalid operator!");
                break;
        }

        input.close(); // Close the scanner to prevent resource leaks
    }
}
