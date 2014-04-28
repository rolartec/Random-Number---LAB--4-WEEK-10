Random-Number---LAB--4-WEEK-10
==============================

RANDOM NUMBER LAB#4 WEEK 10 BY REINA OLARTE


//  BY  REINA OLARTE

// GUESS A NUMBER  LAB #4 WEEK 10

// CHOOSE A NUMBER BETWEEN LOW-HIGH NUMBER

import java.util.Scanner;// imports the scanner class

public class GuessANumber
{
	public static void main( String[]args)
	{
		//Create the Scanner to input the number
		Scanner input = new Scanner(System.in);

		//instantiate random number



		// variables
		int UserNumber;
		int computerNumber;
		int lownumber;
		int highnumber;
		boolean SIGA = true;
		boolean SValues = true;
		String SINO;

		while(SIGA)
		{

			System.out.println("HI !!! LETS GO TO PLAY The Guessing game\nPlease enter a low digit:");
			lownumber = input.nextInt();
			//GuessedNumber.setLowNumber(lownumber);
			System.out.println("Please enter a high digit:");
			highnumber = input.nextInt();
			//GuessedNumber.setHighNumber(highnumber);
			RandomNumber GuessedNumber = new RandomNumber(lownumber, highnumber);
				while(SValues)
						{

						computerNumber = GuessedNumber.GetANumber();	

						System.out.printf("\nPlease Enter a Number between %d and %d As your guess:", lownumber, highnumber);
						UserNumber = input.nextInt();

						if (computerNumber == UserNumber)
						{
							System.out.println("You Guessed the right number");
							System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
						}

						else
							{
								if (computerNumber < UserNumber)
								{
									System.out.println("You Guessed to High");
									System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);
								}
								else
								{	System.out.println("You Guessed to Low");
								System.out.printf("Your number %d, Random number %d" , UserNumber, computerNumber);					
								}//end else	
							}//end else
						System.out.printf("\n\nWould you like to continue guessing between %d and %d?\nType yes or no",GuessedNumber.getLowNumber(), GuessedNumber.getHighNumber());
						SINO = input.next();
						if (SINO.toUpperCase().startsWith("Y"))
						{
							SValues = true;
						}
						else
						{
							SValues = false;
						}
						}//end loop same value

		System.out.println("\nDo you want to continue?\nPress Y for yess N for no");
		SINO = input.next();

		if (SINO.toUpperCase().startsWith("Y"))
		{
			SIGA = true;
			SValues = true;
		}
		else
		{
			SIGA = false;
		}


		}//end loop
	}//End main

}//End class
