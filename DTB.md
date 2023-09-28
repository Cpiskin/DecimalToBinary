# DecimalToBinary 

import java.util.Scanner;

public class DTB {
    public static void main(String args[]) {
      
      Scanner s = new Scanner(System.in);
      System.out.println("Enter a number to convert to binary: ");
      int num = s.nextInt();
      
      int binary = 0;
      int base = 1;
      
      while(num > 0){
          int digit = num % 2;
          binary += digit * base;
         // instead of ==>> using math.pow();
          base *= 10;
          num = num / 2;
      }
      
      System.out.println(binary);
    }
}
