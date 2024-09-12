import java.util.Scanner;

public class FactorialRecursive {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        System.out.print("Enter a number: ");
        int number = scanner.nextInt();
        
        if (number < 0) {
            System.out.println("Factorial is not defined for negative numbers.");
        } else {
            long factorial = factorial(number);
            System.out.println("Factorial of " + number + " is: " + factorial);
        }
        
        scanner.close();
    }

    // Recursive method to calculate factorial
    public static long factorial(int n) {
        if (n == 0) {
            return 1;
        } else {
            return n * factorial(n - 1);
        }
    }
}
