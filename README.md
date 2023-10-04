# NUMBER-GUESSING-GAME
 Laptop with Browser Icon The fun and easy project “Guess the Number” is a short Java project that allows the user to guess the number generated by the computer.










import java.util.Random;
import java.util.Scanner;

public class GuessTheNumber {
    public static void main(String[] args) {
        Random random = new Random();
        int minRange = 1;
        int maxRange = 100;
        int randomNumber = random.nextInt(maxRange - minRange + 1) + minRange;

        Scanner scanner = new Scanner(System.in);
        int attempts = 0;
        int userGuess;

        while (true) {
            System.out.println("Guess the number between " + minRange + " and " + maxRange + ": ");
            userGuess = scanner.nextInt();
            attempts++;

            if (userGuess == randomNumber) {
                System.out.println("Congratulations! You guessed the number in " + attempts + " attempts.");
                break;
            } else if (userGuess < randomNumber) {
                System.out.println("Try a higher number.");
            } else {
                System.out.println("Try a lower number.");
            }
        }
    }
}
