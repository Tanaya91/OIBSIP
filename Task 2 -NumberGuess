package GuessNumber;
import java.util.Random;
import java.util.Scanner;
public class NumberGuess {

		    private static final int MAX_ATTEMPTS = 7;   // Attempts per round
		    private static final int MAX_ROUNDS = 3;     // Total rounds
		    private static final int RANGE_START = 1;
		    private static final int RANGE_END = 100;

		    public static void main(String[] args) {
		        Scanner scanner = new Scanner(System.in);
		        Random random = new Random();

		        int totalScore = 0;

		        System.out.println("Welcome to Guess The Number Game!");
		        System.out.println("You have " + MAX_ROUNDS + " rounds to play.");
		        System.out.println("Try to guess the number between " + RANGE_START + " and " + RANGE_END + ".");
		        System.out.println("You get " + MAX_ATTEMPTS + " attempts per round.\n");

		        for (int round = 1; round <= MAX_ROUNDS; round++) {
		            int numberToGuess = random.nextInt(RANGE_END - RANGE_START + 1) + RANGE_START;
		            int attemptsLeft = MAX_ATTEMPTS;
		            boolean guessedCorrectly = false;

		            System.out.println("Round " + round + " starts!");

		            while (attemptsLeft > 0) {
		                System.out.print("Enter your guess (" + attemptsLeft + " attempts left): ");
		                int guess;

		                // Input validation
		                if(scanner.hasNextInt()) {
		                    guess = scanner.nextInt();
		                    if(guess < RANGE_START || guess > RANGE_END) {
		                        System.out.println("Please enter a number between " + RANGE_START + " and " + RANGE_END + ".");
		                        continue;
		                    }
		                } else {
		                    System.out.println("Invalid input! Please enter an integer.");
		                    scanner.next(); // Clear invalid input
		                    continue;
		                }

		                attemptsLeft--;

		                if (guess == numberToGuess) {
		                    int roundScore = attemptsLeft + 1; // More points for fewer attempts
		                    totalScore += roundScore;
		                    System.out.println("Congratulations! You guessed the number.");
		                    System.out.println("You scored " + roundScore + " points this round.\n");
		                    guessedCorrectly = true;
		                    break;
		                } else if (guess < numberToGuess) {
		                    System.out.println("Try higher!");
		                } else {
		                    System.out.println("Try lower!");
		                }
		            }

		            if (!guessedCorrectly) {
		                System.out.println("Sorry, you've used all your attempts.");
		                System.out.println("The number was: " + numberToGuess + "\n");
		            }
		        }

		        System.out.println("Game Over!");
		        System.out.println("Your total score: " + totalScore + " points.");

		        scanner.close();
		    }
		

	}


