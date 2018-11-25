/* # Week3_CST105_ProgrammingExercise3_Erica_Walters-
 * Guessing Game
 */
/* The following program is the original work of Erica Walters. 
 * The purpose of this program is to create a guessing game, asking for user input to guess integers between 1 and 1000.
 * The program uses a randomly generated number from the program, a scanner to keep track of the number of guesses,
 * and a boolean variable to determine if the game should look when the guess is incorrenct and when to end whe the guess is correct.
 * The program will display: "You WIN! It took you 'X' guesses."
 */

/** Program: Guessing Game
 * File: GuessingGame.java
 * Author: Erica Walters
 * Date: November 25, 2018 
 */
import java.util.Random;
import java.util.Scanner;
public class GuessingGame {
    public static void main(String[] args) {
        Random rand = new Random ();
        int numberToGuess = rand.nextInt(10000);
        int numberOfTries = 0;
        Scanner input = new Scanner(System.in);
        int guess;
        boolean win = false;
        
        while (win == false) {
                
        System.out.println("Enter a guess between 1 and 10000: ");
        guess = input.nextInt();
        numberOfTries++;
        
        if (guess == numberToGuess) {
            win = true;
        }
        else if (guess < numberToGuess) {
            System.out.println("Higher");
        }
        else if (guess > numberToGuess) {
            System.out.println("Lower");
        }
        }
        System.out.println("You WIN."); System.out.println("It took you " + numberOfTries + " guesses.");
    }
}
