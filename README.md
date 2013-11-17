Final-Project
=============
Houses the methods that I have created for our Point of Sale System
________________________________________________________________________

import java.util.ArrayList;
import java.util.Scanner;

/*
 * code by Talha Siddique @ tsiddique@gwmail.gwu.edu. 
 * Please contact and explain to me what option C is about. I don't understand what the "child UI is" Thanks
 */
public class salesUserInterface {

	
	public static void userInterface() {
		Scanner scan = new Scanner (System.in);
		ArrayList<String> salesList; //array list for sales
		salesList = new ArrayList<String>(); //name of array list
		String sale; //storing the sale as a string.
		int option; //the options available to the user. 
		
		System.out.println("Welcome! Please select from the following options:");
		System.out.print("1)New Sale 2)Delete Sale 3)Search Sales 4)Show All Sales 5)Exit");
		do {
			option = scan.nextInt(); //scans for user's entered input for options
			
			if(option ==1 ) {
				System.out.println("Plese enter the sale");
				sale = scan.next();
				salesList.add(sale);
				System.out.println("Please enter another choice");
			}
			if(option == 2) {
				System.out.println("Please enter the sale to be deleted");
				sale = scan.next();
				salesList.remove(sale);
				System.out.println("Please enter another choice");	
			}
			if (option == 3) { 
				System.out.println("What sale are you looking for");
				sale = scan.next();
				/*
				 * At this point I was having some trouble trying to do a search for specific sales. I was thinking of printing
				 * I couldn't find a method in the array list that would let me take a user input and compare that with what is in
				 * the array list. I'm not sure if the method used for arrays, iterating until we find the user input, would work here. 
				 * Any tips would help. 
				 */		
			}
			if (option ==4) {
				System.out.println("Here is the list of sales: ");
				System.out.println(salesList);
			}
			
			if (option ==5) {
				System.out.println("Thank you for using the system");
				break;
			}
			
		
	}
		while(true);
		
		
	}
	
	public static void main(String[]args){
	
	}
}


