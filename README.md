# Calculator-

    import java.util.Scanner;               
     public class Main {
      public static void main(String[] args){
        Scanner scanner = new Scanner(System.in);
        double result = 0;
        boolean validOperation = true ;

        System.out.print("Enter The First Number :");
        double num1 = scanner.nextDouble();

        System.out.print("Enter an operator ( + , - , * , / , ^ )");
        char operator = scanner.next().charAt(0);

        System.out.print("Enter the second Number :");
        double num2 = scanner.nextDouble();

        switch (operator){
            case '+' -> result = num1 + num2 ;
            case '-' -> result = num1 - num2 ;
            case '*' -> result = num1 * num2 ;
            case '/' -> {
                if (num2 == 0){
                        System.out.println("The Numerator CAN'T be 0");
                    validOperation = false;
                }
                else {
                    System.out.println( num1 / num2 );
                }
            }
            case '^' -> result = Math.pow(num1 , num2) ;
            default -> {
                System.out.println("Please Choose The Operators That are Given .");
                System.out.println("Invalid Operator ");
                validOperation = false ;
            }
        }

        if (validOperation){
        System.out.printf("The result is : %.2f" , result ) ;
        }


        scanner.close();
    }
    }
