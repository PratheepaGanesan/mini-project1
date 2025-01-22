Number Guessing Game in Java

Description

This is a simple Number Guessing Game built using Java. The player has five attempts to guess the correct number between 1 and 100. The game gives feedback on whether the guessed number is too high or too low.

Features

Generates a random number between 1 and 100.

The player has 5 attempts to guess the number.

Provides feedback on whether the guess is too high or too low.


Code
import java.util.Scanner;
import java.util.Random;

public class game{
    public static void main(String args[]) {
        Scanner scan = new Scanner(System.in);
        Random random = new Random();
        int randomnumber = random.nextInt(100)+1;
        int attempts=5;
        System.out.println("welcome to the number guessing game");
        System.out.println("I have a number between 1 t0 100");
        System.out.println("You have five attempts");

        for(int i=1;i<=attempts;i=i+1)
        {
            System.out.println("Attempts"+i+"enter your guess:");
            int userguess=scan.nextInt();

            if (userguess==randomnumber)
            {
                System.out.println("congratulations! you guessed the correct number:"+randomnumber);
                scan.close();
                return;
            
            }
            else if(userguess>randomnumber)
            {
                System.out.println("Try a smaller number");
            }
                else
                {
                    System.out.println("try a large number");

                }
            }

            System.out.println("Sorry, you used all attempts! the correct number is:"+randomnumber);
             scan.close();
            }
}
