# Interface
package Interface;
import java.util.Scanner;
interface Calculator {
double add(double a, double b);
double subtract(double a, double b);
double multiply(double a, double b);
double divide(double a, double b);
{
class SimpleCalculator implements Calculator {
@Override
public double add(double a, double b) {
return a + b;
}
@Override
public double subtract(double a, double b) {
return a - b;
}
@Override
public double multiply(double a, double b) {
return a * b;
}
@Override
public double divide(double a, double b) {
if (b == 0) {
System.out.println("Error: Division by zero is not allowed!");
return Double.NaN; // Return;Not a Numbert; if division by zero
}
return a / b;
}
}
public class Interface {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
Calculator calculator = new SimpleCalculator();
System.out.println("welcome to the simple calculator!");
System.out.print("Enter the first number:");
double num1 = scanner.nextDouble();
System.out.print("Enter the second number:");
double num2 = scanner.nextDouble();
System.out.println("\nResults:");
System.out.println("Addition:" + calculator.add(num1, num2));
System.out.println("Subtraction:"  + calculator.subtract(num1, num2));
System.out.println("Multiplication:"  + calculator.multiply(num1, num2));
System.out.println("Division:" + calculator.divide(num1, num2));
scanner.close();
}
    }

OUTPUT:
welcome to the simple calculator!
Enter the first number:2
Enter the second number:4

Results:
Addition:6.0
Subtraction:-2.0
Multiplication:8.0
Division:0.5
