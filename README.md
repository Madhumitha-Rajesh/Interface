# Interface

Coding-

package constructor;
import java.util.Scanner;
//define calculator interface
interface Calculator{
    double add(double a,double b);
    double subtract(double a,double b);
    double multiply(double a,double b);
    double divide(double a,double b);
}
class SimpleCalculator implements Calculator{
    @Override
    public double add(double a,double b){
        return a+b;
    }
    @Override
    public double subtract(double a,double b){
        return a-b;
    }
    @Override
    public double multiply(double a,double b){
        return a*b;
    }
    @Override
    public double divide(double a,double b){
        if(b==0){
            System.out.println("Error:Division by 0 is not allowed!");
            return Double.NaN;
        }
        return a/b;
    }
}
public class CalculatorProgram{
    public static void main(String[] args) {
        Scanner scanner=new Scanner(System.in);
        Calculator calculator=new SimpleCalculator();
        System.out.print("Enter the first number");
        double num1=scanner.nextDouble();
        System.out.print("Enter the second number:");
        double num2=scanner.nextDouble();
        System.out.println("RESULTS\n");
        System.out.println("Addition:"+calculator.add(num1,num2));
        System.out.println("Subtraction:"+calculator.subtract(num1,num2));
        System.out.println("Multiplication:"+calculator.multiply(num2, num2));
        System.out.println("Division:"+calculator.divide(num2, num2));
        scanner.close();
    }
    
}


Output-

Addition of two integers:31
Addition of three integers:510
Addition of two doubles:30.299999999999997
