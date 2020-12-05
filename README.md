# Guess_number_in_Java
//Creating A Guess Number game with Object and classes 
import java.util.Random ;

import java.util.Scanner ;

class Game {

	int number ;

	int input_Number ;

	int guessCount =  0 ;

	public int number() {

		Random rand = new Random() ;

		number = rand.nextInt(50);

		return number ;

	}

	public int input_Number() {

		Scanner scan = new Scanner(System.in) ;

		System.out.print("Guess the Number :");

		input_Number = scan.nextInt() ;

		return input_Number ;

	}

	public boolean isCorrectNumber() {

//		input_Number++ ;

		guessCount++ ;

		if (input_Number == number) {

			System.out.format("😆Correct Guess number \nYou Guess in " + guessCount++ +" Times \n");

		}

		if (input_Number < number) {

			System.out.println("☹️to Low .. ");

		} else if (input_Number > number) {

			System.out.println("☹️to High  ");

		}

		return false ;

	}

}

public class Main {

	public static void main(String[] args) {

		System.out.println("______ Guess Number ______");

		Game guess = new Game() ;

		guess.number() ;

		boolean b = false;

		while (b != true) {

			guess.input_Number() ;

			guess.isCorrectNumber() ;

		}

	}

}
