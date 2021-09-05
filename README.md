# Java-Project

// Default package imported from template
package com.company;
// The java.util.scanner package allows for user input
import java.util.Scanner;

// Main class created
public class Main {
    //Main function (method) created
    public static void main(String[] args) {

        // This activates user input
        Scanner input = new Scanner(System.in);

        // The following variables are used later and need to be initialized
        float sum = 0;
        float average;
        int number = 0;
        // Note that counter is set to "-1" because the value "999"is used to terminate the program, and it should not be included in the counter
        int counter = -1;

        // The message below will be displayed upon opening the program
        System.out.println("THIS PROGRAM WILL CALCULATE YOUR CURRENT GPA FOR YOUR CLASSES. TYPE 999 TO INDICATE END OF DATA.");

        // Note to self: do-while loops iterate until the condition met at the end is true
        do {
            // The user will be asked for a number input with the message below
            System.out.print("Please enter your numeric grade for your class: ");
            // Adds the inputted number to sum value
            sum = sum + number;
            // Sets number value as the user input via Scanner library
            number = input.nextInt();
            // Increments counter by 1 per loop
            counter++;
            // The do while loop will end once "999" is inputted
        } while(number != 999);

        // Average value is set to the sum divided by the counter
        average = sum/counter;
        // This will display the GPA. Note that "%f" is a placeholder for the average
        System.out.printf("Your GPA is: %f, ", average);

// Additional Messages:

        // If average is greater than 90, the following message will be displayed
        if (average >= 90) {
            System.out.println("That's a high GPA, great job");
        }

        // If average is less than 90, the following message will be displayed
        else {
            System.out.println("That's not looking so great, study");
        }
    }
}
