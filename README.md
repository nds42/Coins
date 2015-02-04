# Coins
This program displays the quantity of each coin to add up to the inputted amount in cents.
/*
 * Nate Stein
 * 12/6/14
 * Block 2 B
 * Chapter 9
 * Exercise: 14a
 * Takes an amount in cents and outputs the number of each coin.
 */

import java.util.Scanner;

public class Coins {
	private int cents;
	private int quarters;
	private int dimes;
	private int nickels;
	private int pennies;
	
	public Coins(int c)
	{
		cents = c;
		quarters = cents / 25;
		cents -= quarters * 25;
		dimes = cents / 10;
		cents -= dimes * 10;
		nickels = cents / 5;
		cents -= nickels * 5;
		pennies = cents;
		cents -= pennies;
	}
	public int getQuarters()
	{
		return quarters;
	}
	public int getDimes()
	{
		return dimes;
	}
	public int getNickels()
	{
		return nickels;
	}
	public int getPennies()
	{
		return pennies;
	}
	public static void main(String[] args) {
		Scanner kb = new Scanner(System.in);
		System.out.print("Enter amount in cents: ");
		int cents = kb.nextInt();
		Coins c = new Coins(cents);
		System.out.println(c.getQuarters() + " quarter(s)");
		System.out.println(c.getDimes() + " dime(s)");
		System.out.println(c.getNickels() + " nickel(s)");
		System.out.println(c.getPennies() + " pennie(s)");
	}

}
OUTPUT:
Enter amount in cents: 67
2 quarter(s)
1 dime(s)
1 nickel(s)
2 pennie(s)
