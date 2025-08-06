# ConsoleCalculator
Calculator project for internship task

Console Calculator:
- Simple Java calculator for basic arithmetic operations
- Takes two numbers and an operator as input
- Handles division by zero error

How to Run:
1. Compile: javac ConsoleCalculator.java
2. Run: java ConsoleCalculator

Features:
- Addition
- Subtraction
- Multiplication
- Division


code:

package JavaT;
import java.util.Scanner;
public class ConsoleCalculator {

	public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        // Step 1: Take first number
        System.out.print("Enter first number: ");
        double num1 = sc.nextDouble();

        // Step 2: Take operator
        System.out.print("Enter operator (+, -, *, /): ");
        char operator = sc.next().charAt(0);

        // Step 3: Take second number
        System.out.print("Enter second number: ");
        double num2 = sc.nextDouble();

        double result;

        // Step 4: Perform operation
        switch (operator) {
            case '+':
                result = num1 + num2;
                System.out.println("Result: " + result);
                break;
            case '-':
                result = num1 - num2;
                System.out.println("Result: " + result);
                break;
            case '*':
                result = num1 * num2;
                System.out.println("Result: " + result);
                break;
            case '/':
                if (num2 != 0) {
                    result = num1 / num2;
                    System.out.println("Result: " + result);
                } else {
                    System.out.println("Error: Cannot divide by zero!");
                }
                break;
            default:
                System.out.println("Invalid operator!");
        }

	}
}
