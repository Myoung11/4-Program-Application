// Matthew Young
// Final Program Project

/* Summary: This program will run 4 different programs. The user can choose 
            which program they want to run. They can choose from a sales receipt, 
            creating a contact card, balancing a checkbook, and converting time. 
            */


#include <iostream>
#include <iomanip>
#include <cmath>
#include <vector>
#include <string>
#include <fstream>

using namespace std; 


int mainMenu (int desOperation) { // Beginning of int mainMenu(int desOperation) function 

    cout << "       -------------------------------------------" << endl; // Input border
    cout << "       -------------------------------------------" << endl; // Input border 
    cout << "       -------          MAIN MENU          -------" << endl; // Input border and title
    cout << "       -------------------------------------------" << endl; // Input border
    cout << "       -------------------------------------------" << endl; // Input border
    cout << endl;                                                         // Creates a space
    cout << " Number                   Operation         " << endl;       // Input border and title
    cout << "***************************************************************************" << endl; // Input border
    cout << " 1  ..................... Calculate Sales Tax on Multiple Sales Items" << endl;       // Shows description of program
    cout << " 2  ..................... Create a Customer Contact Card" << endl;                    // Shows description of program
    cout << " 3  ..................... Balance a Checkbook" << endl;                               // Shows description of program
    cout << " 4  ..................... Time Conversion Utility" << endl;                           // Shows description of program
    cout << " 5  ..................... Exit" << endl;                                              // Shows description of program
    cout << "***************************************************************************" << endl; // Input border
    
    int invalid = 0;
	bool error = false;
    
    cout << endl;                                                                   // Creates a space
    
    do{ // Do loop for error checking 
    cout << "Enter the desired operation: ";                                        // Asks user to entered number of program they want
    cin >> desOperation;                                                            // User inputed answer
    while (desOperation > 5) {                                                      // While loop for invalid entry
        cout << "Invalid Entry! Please enter a valid response: ";                   // Tells user entry was invalid
        cin >> desOperation;                                                        // User inputed answer
    }
    
    error = cin.fail();                                                             // Sets bool error equal to a failed cin input
		
		if (error)                                                                  // If statement for invalid input (Error Checking)
			cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
	
	cout << endl;                                                                   // Creates a Space 

    int numOp;                                                                      // Variable for which program to run
    numOp = desOperation;                                                           // Sets numOp = to selection from int mainMenu(int desOperation)
    return numOp;                                                                   // Gives selection back
 
} // End of int mainMenu(desOperation) function 
    

int main () { // Beginning of Main Function

char mMenu; // Variable for returning to main menu
string firstname; // Variable for user's name
int numOp;        // Variable for program selection

    cout << "-------------------------------------------" << endl; // Input border
    cout << "-------------------------------------------" << endl; // Input border
    cout << "----------     HELLO WELCOME     ----------" << endl; // Input border and title
    cout << "----------     TO THE PROGRAM    ----------" << endl; // Input border and title
    cout << "-------------------------------------------" << endl; // Input border
    cout << "-------------------------------------------" << endl; // Input border
    cout << "Enter your first name: ";                             // Asks user to input their name
    cin >> firstname;                                              // User inputed name
    cout << endl;                                                  // Creates space
    cout << "-------------------------------------------" << endl; // Input border
    cout << "-------------------------------------------" << endl; // Input border
    cout << "----------          HELLO        ----------" << endl; // Input border and title
    cout << "----------           " << firstname << "         ----------" << endl; // Input border and user's name
    cout << "-------------------------------------------" << endl; // Input border
    cout << "-------------------------------------------" << endl; // Input border
    cout << "Press Y to continue: ";                    // Asks user if they want to continue to program
    cin >> mMenu;                                                  // User inputed answer
    cout << endl;                                                  // Creates space

while (mMenu == 'Y' || mMenu == 'y' || mMenu == 'n' || mMenu == 'N' || mMenu != 'N' || mMenu != 'n' || mMenu != 'Y' || mMenu != 'y') { // While loop to start program

    while (mMenu == 'y' || mMenu == 'Y') { // While loop for when user wants to continue
        
        numOp = mainMenu(numOp); // sets numOp = to selection from other function
    
        if (numOp == 1) { // If statement for program 1
    int invalid = 0;
	bool error = false;
    
    cout << endl;                                                                   // Creates a space
	
	cout << endl;                                                                   // Creates a Space 
    double numItems;          // Variable for number of items
    double valItem;           // Variable for price of items 
    double salesTax;          // Variable for amount of sales tax
    double totSales = 0;      // Variable for total of all prices  
    double totTax;            // Variable for total sales tax
    double grandTot;          // Variable for grand total 
    char runProg;             // Variable for if the user wants to run the program again
    char contProg;            // Variable for the user to enter the program
   vector<double> salesItems; // Vector to hold each individual sales item and price 
   vector<string> salesNames; // Vector to hold each sales item name 
   string salesName;          // Variable for the name of the sales item
   int numVals;               // Variable for number of sales items, included in vectors
   int i;                     // Variable for loops
   
   cout << "*******************************************************************" << endl; // Input border
   cout << "*********                                                **********" << endl; // Input border
   cout << "**********     WELCOME TO THE SALES RECEIPT PROGRAM!     **********" << endl; // Input border and title
   cout << "********** THIS PROGRAM WILL COMPUTE A RECEIPT THAT WILL **********" << endl; // Input border and title
   cout << "**********  DISPLAY THE NAME AND PRICE OF A SALES ITEM,  **********" << endl; // Input border and title
   cout << "**********  THE TOTAL SALES PRICE, THE TOTAL SALES TAX,  **********" << endl; // Input border and title
   cout << "**********  AND THE GRAND TOTAL PRICE OF THE PURCHASE    **********" << endl; // Input border and title
   cout << "**********                                               **********" << endl; // Input border
   cout << "*******************************************************************" << endl; // Input border
   cout << "Press Y to continue: ";                                  // Tells User to press Y to continue to the program
   cin >> contProg;                                                  // User inputed answer
   cout << endl;                                                     // Creates a space
   if (contProg == 'Y' || contProg == 'y') {                         // If statement for when the user presses y to continue to the program
   cout << "Enter in the number of sales items to be calculated: ";  // Asks the user how many sales items they have
   cin >> numVals;                                                   // User inputed number of sales items 
   
   salesItems.resize(numVals);                                       // Resizes the vector the number that the user inputed for numVals
   salesNames.resize(numVals);                                       // Resizes the vector the number that the user inputed for numVals
   cout << endl;                                                     // Creates a space 
   
   for (i = 0; i < salesItems.size(); ++i) {                               // For loop for user to enter the name and price of sales items
       cout << "Enter in the name of sales item number " << i + 1 << ": "; // Asks the user to enter in the name of the sales item
       cin >> salesNames.at(i);                                            // User inputed sales name
       cout << "Enter in the price of the " << salesNames.at(i)  << " : $";// Asks user the value of each sales item
       cin >> salesItems.at(i);                                            // User inputed sales price
   }
   
   totSales = 0;                                                     // Sets totSales equal to zero for 'for' loop
   for (i = 0; i < salesItems.size(); ++i) {                         // For loop to find total of all prices
      totSales = totSales + salesItems.at(i);                        // Equation for totSales
   }
      cout << endl;                                                    // Creates a space
    
    cout << "Enter in the sales tax percentage" << endl;             // Ask user for sales tax percentage
    cout << "(Enter 10 for 10%): ";                                  // Tells user format for input
    cin >> salesTax;                                                 // User inputed sales tax percentage
    cout << endl;                                                    // Creates a space
    
    salesTax = salesTax / 100;                                       // Equation to turn user inputed sales tax into decimal 
    totTax = salesTax * totSales;                                    // Equation to find dollar amount of sales tax. 
    grandTot = totTax + totSales;                                    // Equation to find grand total of sales tax and prices
    
    cout << "*********************************************" << endl; // Inputs top border
    cout << "*********************************************" << endl; // Inputs top border
    cout << "********  S A L E S  R E C E I P T  *********" << endl; // Inputs title for all output 
    cout << "*********************************************" << endl; // Inputs part of top border
    cout << "**              **        **               **" << endl; // Inputs border 
    cout << "**  Item Names  **        **   Price       **" << endl; // Inputs Column titles
    cout << "*********************************************" << endl; // Inputs border
    for (i = 0; i < salesItems.size(); ++i) {                        // For loop using vector to hold each sales item number and price
      cout << "**  " << salesNames.at(i);                            // Outputs part of border and each sales item name
      
      if (salesNames.at(i).size() == 4) {                            // If statement for the length of the sales names to align the amounts and borders
          cout << right << setw(salesNames.size() + 21) << "$      ";// Aligns and outputs the sales name and dollar sign
          cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
        }
      
      if (salesNames.at(i).size() == 5) {                            // If statement for the length of the sales names to align the amounts and borders
          cout << right << setw(salesNames.size() + 19) << "$     "; // Aligns and outputs the sales name and dollar sign
          cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
          }
      
      if (salesNames.at(i).size() == 6) {                            // If statement for the length of the sales names to align the amounts and borders
          cout << right << setw(salesNames.size() + 16) << "$   ";   // Aligns and outputs the sales name and dollar sign
          cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
        }
          
      if (salesNames.at(i).size() > 6) {                             // If statement for the length of the sales names to align the amounts and borders
          cout << right << setw(salesNames.size() + 12) << "$   ";   // Aligns and outputs the sales name and dollar sign
          cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
          }
          
      if (salesNames.at(i).size() < 4) {                             // If statement for the length of the sales names to align the amounts and borders
          cout << right << setw(salesNames.size() + 21) << "$    ";  // Aligns and outputs the sales name and dollar sign
          cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
          }
          
      cout << endl;                                                  // Creates a space
   }
    
    cout << "*********************************************" << endl;         // Inputs border
    cout << "**  Sales Total" << setw(14) << "$   ";                         // Inputs title for total sales output and aligns dollar sign 
    cout << fixed << setprecision(2) << totSales << setw(9) << endl; // Sets amount to two decimals and aligns output for total sales
    cout << "**  Sales Tax" << setw(17) << "$    ";                          // Inputs title for sales tax ouput and aligns dollar sign
    cout << fixed << setprecision(2) << totTax << setw(9) << endl;   // Sets amount to two decimals and aligns output for sales tax
    cout << "**                        ----------" << endl;         // Inputs divider bewtween total sales, sales tax and grand total 
    cout << "**  Grand Total" << setw(14) << "$   ";                         // Inputs title for grand total output and aligns dollar sign
    cout << fixed << setprecision(2) << grandTot << setw(9) << endl; // Sets amount to two decimals and aligns output for grand total 
    cout << "**                                         **" << endl;         // Inputs border
    cout << "*********************************************" << endl;         // Inputs border
    cout << "*********************************************" << endl;         // Inputs border
    
   
   
    cout << endl;                                                             // Creates a space
    cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
    cin >> runProg;                                                           // User inputed answer
}
    while (runProg == 'Y' || runProg == 'y') {   // While loop for when the user wants to run the program again
        
        double numItems;          // Variable for number of items
        double valItem;           // Variable for price of items 
        double salesTax;          // Variable for amount of sales tax
        double totSales = 0;      // Variable for total of all prices  
        double totTax;            // Variable for total sales tax
        double grandTot;          // Variable for grand total 
        char runProg;             // Variable for if the user wants to run the program again
        vector<double> salesItems; // Vector to hold each individual sales item and price 
        vector<string> salesNames; // Vector to hold each sales item name 
        string salesName;          // Variable for 
        int numVals;               // Variable for number of sales items, included in vectors
        int i;                     // Variable for loops
    
    do{ // Do loop for error checking
        cout << "Enter in the number of sales items to be calculated: ";  // Asks the user how many sales items they have
        cin >> numVals;                                                   // User inputed number of sales items 
   
        salesItems.resize(numVals);                                       // Resizes the vector the number that the user inputed for numVals
        salesNames.resize(numVals);                                       // Resizes the vector the number that the user inputed for numVals
   
        cout << endl;                                                     // Creates a space 
   
        for (i = 0; i < salesItems.size(); ++i) {                               // For loop for user to enter the name and price of sales items
            cout << "Enter in the name of sales item number " << i + 1 << ": "; // Asks the user to enter in the name of the sales item
            cin >> salesNames.at(i);                                            // User inputed sales name
            cout << "Enter in the price of the " << salesNames.at(i)  << " : $";// Asks user the value of each sales item
            cin >> salesItems.at(i);                                            // User inputed sales price
        }
   
        totSales = 0;                                                     // Sets totSales equal to zero for 'for' loop
        for (i = 0; i < salesItems.size(); ++i) {                         // For loop to find total of all prices
            totSales = totSales + salesItems.at(i);                        // Equation for totSales
        }
      

            cout << endl;                                                    // Creates a space
    
            cout << "Enter in the sales tax percentage" << endl;             // Ask user for sales tax percentage
            cout << "(Enter 10 for 10%): ";                                  // Tells user format for input
            cin >> salesTax;                                                 // User inputed sales tax percentage
    
            cout << endl;                                                    // Creates a space
    
            salesTax = salesTax / 100;                                       // Equation to turn user inputed sales tax into decimal 
            totTax = salesTax * totSales;                                    // Equation to find dollar amount of sales tax. 
            grandTot = totTax + totSales;                                    // Equation to find grand total of sales tax and prices
    
            cout << "*********************************************" << endl; // Inputs top border
            cout << "*********************************************" << endl; // Inputs top border
            cout << "********  S A L E S  R E C E I P T  *********" << endl; //Inputs title for all output 
            cout << "*********************************************" << endl; // Inputs part of top border
            cout << "**              **        **               **" << endl; // Inputs border 
            cout << "**  Item Names  **        **   Price       **" << endl; // Inputs Column titles
            cout << "*********************************************" << endl; // Inputs border
            for (i = 0; i < salesItems.size(); ++i) {                        // For loop using vector to hold each sales item number and price
                cout << "**  " << salesNames.at(i);                            // Outputs part of border and each sales item name
      
            if (salesNames.at(i).size() == 4) {                            // If statement for the length of the sales names to align the amounts and borders
                cout << right << setw(salesNames.size() + 21) << "$      ";// Aligns and outputs the sales name and dollar sign
                cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
            }
      
            if (salesNames.at(i).size() == 5) {                            // If statement for the length of the sales names to align the amounts and borders
                cout << right << setw(salesNames.size() + 19) << "$     "; // Aligns and outputs the sales name and dollar sign
                cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
            }
      
            if (salesNames.at(i).size() == 6) {                            // If statement for the length of the sales names to align the amounts and borders
                cout << right << setw(salesNames.size() + 16) << "$   ";   // Aligns and outputs the sales name and dollar sign
                cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
            }
          
            if (salesNames.at(i).size() > 6) {                             // If statement for the length of the sales names to align the amounts and borders
                cout << right << setw(salesNames.size() + 12) << "$   ";   // Aligns and outputs the sales name and dollar sign
                cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
            }
          
            if (salesNames.at(i).size() < 4) {                             // If statement for the length of the sales names to align the amounts and borders
                cout << right << setw(salesNames.size() + 21) << "$    ";  // Aligns and outputs the sales name and dollar sign
                cout << fixed << setprecision(2) << salesItems.at(i);      // Aligns, sets to two decimals, and outputs the sales price
            }
          
        cout << endl;                                                  // Creates a space
        }
    
        cout << "*********************************************" << endl;         // Inputs border
        cout << "**  Sales Total" << setw(14) << "$   ";                         // Inputs title for total sales output and aligns dollar sign 
        cout << fixed << setprecision(2) << totSales << setw(9) << endl; // Sets amount to two decimals and aligns output for total sales
        cout << "**  Sales Tax" << setw(17) << "$    ";                          // Inputs title for sales tax ouput and aligns dollar sign
        cout << fixed << setprecision(2) << totTax << setw(9) << endl;   // Sets amount to two decimals and aligns output for sales tax
        cout << "**                        ----------"       << endl;         // Inputs divider bewtween total sales, sales tax and grand total 
        cout << "**  Grand Total" << setw(14) << "$   ";                         // Inputs title for grand total output and aligns dollar sign
        cout << fixed << setprecision(2) << grandTot << setw(9) << endl; // Sets amount to two decimals and aligns output for grand total 
        cout << "**                                         **" << endl;         // Inputs border
        cout << "*********************************************" << endl;         // Inputs border
        cout << "*********************************************" << endl;         // Inputs border
                
    error = cin.fail();                                                             // Sets bool error equal to a failed cin input
		
		if (error)                                                                  // If statement for invalid input (Error Checking)
			cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
	
	cout << endl;                                                                   // Creates a Space
        
        cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
        cin >> runProg;                                                           // User inputed answer
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for 2+ times running through the program when user wants to end the program 
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // !!** Lines 342-350 inputs border/title **!!
            cout << "-------------------------------------------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------          THANK-YOU          -------" << endl;
            cout << "-------          FOR USING          -------" << endl; 
            cout << "-------         OUR PROGRAM!        -------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------------------------------------------" << endl; 
            cout << "-------------------------------------------" << endl; 
                    break;      // Stops while loop
                
            }

        }
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for original function when user wants to end the program
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
                                              
            }

	
	cout << endl;                                                                   // Creates a Space 
            
            cout << "Press Y to go back to the main menu: "; // Asks user if they want to return to the main menu
            
        }
    
        else if (numOp == 2) { // Else if statement for program 2
    int invalid = 0;
	bool error = false;
char runProg;      // Variable for if the user wants to run the program again
char firstIn;      // Variable for the user's first inital
char lastIn;       // Variable for the user's last inital
string lastName;   // Variable for the user's last name
string userName;   // Variable for the user's first name
string streetName; // Variable for the user's address
string cityName;   // Variable for the user's city
string stateName;  // Variable for the user's state
string zipCode;    // Variable for the user's zip code
string phoneNumber; //Variable for the user's phone number 

cout << "Enter customer's full name: ";   // Asks the user to enter in their full name 
    cin >> firstIn >> userName >> lastIn; // User inputed name
    getline (cin, lastName);              // Gets the whole line of user input for their name and sets it to the variable

cout << "Enter Street Address (Ex: 123 Main Street): "; // Asks the user to enter in their address
   getline(cin, streetName);                            // Gets the whole line of user input for their address and sets it to the variable
    
cout << "Enter City: ";                                 // Asks the user to enter their city
    getline(cin, cityName);                             // Gets the whole line of user input for their city and sets it to the variable
    
cout << "Enter State: ";                                // Asks the user to enter their state
    getline(cin, stateName);                            // Gets the whole line of user input for their state and sets it to the variable
    
cout << "Enter Zip Code: ";                             // Asks the user to enter their zip code
    getline(cin, zipCode);                              // Gets the whole line of user input for their zipcode and sets it to the varible
    
cout << "Enter Phone Number: ";                         // Asks the user to enter their phone number
    getline(cin, phoneNumber);                          // Gets the whole line of user input for their phone number and sets it to the varible
    cout << endl;                                       // Creates a space
    
cout << "****************************************" << endl; // Inputs border
cout << "****************    " << firstIn << lastIn << "    **************" << endl; // Inputs border and user's initals 
cout << "****************************************" << endl; // Inputs border
cout << "***           CONTACT CARD           ***" << endl; // Inputs border and output title
cout << "****************************************" << endl; // Inputs border
cout << "***                                  ***" << endl; // Inputs border
cout << "*** " << firstIn << userName << " " << lastIn << lastName << endl; // Outputs the user's name
cout << "*** " << streetName << endl;                                       // Outputs the user's address
cout << "*** " << cityName << ", " << stateName << " " << zipCode << endl;  // Outputs the user's city, state, and zip code
cout << "*** " << phoneNumber << endl;                                      // Outputs the user's phone number
cout << "***                                   ***" << endl; // Inputs border
cout << "*****************************************" << endl; // Inputs border

cout << endl;                                                     // Creates space
cout << "Would you like to create another contact card? (Y/N)? "; // Asks user if they want to create another contact card
cin >> runProg;                                                   // User inputed answer
    
    
    while (runProg == 'Y' || runProg == 'y') {   // While loop for when the user wants to run the program again
    cout << endl; // Creates a space

char runProg;      // Variable for if the user wants to run the program again
char firstIn;      // Variable for the user's first inital
char lastIn;       // Variable for the user's last inital
string lastName;   // Variable for the user's last name
string userName;   // Variable for the user's first name
string streetName; // Variable for the user's address
string cityName;   // Variable for the user's city
string stateName;  // Variable for the user's state
string zipCode;    // Variable for the user's zip code
string phoneNumber; //Variable for the user's phone number 
do{ // Do loop for error checking
cout << "Enter customer's full name: ";   // Asks the user to enter in their full name 
    cin >> firstIn >> userName >> lastIn; // User inputed name
    getline (cin, lastName);              // Gets the whole line of user input for their name and sets it to the variable

cout << "Enter Street Address (Ex: 123 Main Street): "; // Asks the user to enter in their address
   getline(cin, streetName);                            // Gets the whole line of user input for their address and sets it to the variable
    
cout << "Enter City: ";                                 // Asks the user to enter their city
    getline(cin, cityName);                             // Gets the whole line of user input for their city and sets it to the variable
    
cout << "Enter State: ";                                // Asks the user to enter their state
    getline(cin, stateName);                            // Gets the whole line of user input for their state and sets it to the variable
    
cout << "Enter Zip Code: ";                             // Asks the user to enter their zip code
    getline(cin, zipCode);                              // Gets the whole line of user input for their zipcode and sets it to the varible
    
cout << "Enter Phone Number: ";                         // Asks the user to enter their phone number
    getline(cin, phoneNumber);                          // Gets the whole line of user input for their phone number and sets it to the varible
    cout << endl;                                       // Creates a space
    
cout << "****************************************" << endl; // Inputs border
cout << "****************    " << firstIn << lastIn << "    **************" << endl; // Inputs border and user's initals 
cout << "****************************************" << endl; // Inputs border
cout << "***           CONTACT CARD           ***" << endl; // Inputs border and output title
cout << "****************************************" << endl; // Inputs border
cout << "***                                  ***" << endl; // Inputs border
cout << "*** " << firstIn << userName << " " << lastIn << lastName << endl; // Outputs the user's name
cout << "*** " << streetName << endl;                                       // Outputs the user's address
cout << "*** " << cityName << ", " << stateName << " " << zipCode << endl;  // Outputs the user's city, state, and zip code
cout << "*** " << phoneNumber << endl;                                      // Outputs the user's phone number
cout << "***                                   ***" << endl; // Inputs border
cout << "*****************************************" << endl; // Inputs border
    
            cout << endl;                                                             // Inputs space
            cout << "Would you like to create another contact card? (Y/N): ";         // Asks user if they want to run the program again
            cin >> runProg;                                                           // User inputed answer
            
        if (error)                                                                  // If statement for invalid input (Error Checking)
		cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
        cout << endl;                                                               // Creates a space
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for 2+ times running through the program when user wants to end the program 
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
                break;                               // Stops while loop
            }
            
            if (runProg != 'N' && runProg != 'n' && runProg != 'Y' && runProg != 'y') { // If statement for invalid input (Error checking)
                break;                              // Stops while loop
            }
        
    }
        
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for original function when user wants to end the program
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Lines 511-519 inputs border/title
            cout << "-------------------------------------------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------          THANK-YOU          -------" << endl; 
            cout << "-------          FOR USING          -------" << endl; 
            cout << "-------         OUR PROGRAM!        -------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------------------------------------------" << endl; 
            cout << "-------------------------------------------" << endl; 
                                                      
            }
            
            cout << "Press Y to go back to the main menu: "; // Asks user if they want to return to the main menu  
        }
        
        else if (numOp == 3) {// Else if statement for program 3
    
    int invalid = 0;
	bool error = false;
    double begBal;            // Variable for original beginning balance
    vector <double> newBal;   // Vector for balance in between transactions
    double totTrans = 0;      // Variable for final balance
    char userAns;             // Variable for if the user wants to copy output to a file
    char runProg;             // Variable for if the user wants to run the program again
   vector<double> numTrans;   // Vector for dollar amount of each transaction
   vector<string> transNames; // Vector for if transaction is a deposit or withdrawal
   int numVals;               // Variable for number of transactions
   int i;                     // Variable for loops
   
   do{ // Do loop for error checking
   cout << "What is your beginning balance: "; // Asks user their beginning balance
   cin >> totTrans;                            // User inputed balance
   
   begBal = totTrans;                          // Sets begBal equal to user inputed totTrans
   
   cout << "Enter in the number of transactions: "; // Asks user to enter in the number of transactions
   cin >> numVals;                                  // User inputed number of transactions             
   
   numTrans.resize(numVals);      // Resizes the vector to the number that the user inputed for numVals
   transNames.resize(numVals);    // Resizes the vector to the number that the user inputed for numVals  
   newBal.resize(numVals);        // Resizes the vector to the number that the user inputed for numVals
   
   cout << endl;                  // Creates a space  
   
   for (i = 0; i < numTrans.size(); ++i) {  // For loop for asking user if each transaction is D/W and the amount of it                         
       cout << "Is transaction " << i + 1 << " a deposit(D) or withdrawal(W): "; // Asks user if D/W 
       cin >> transNames.at(i);                                                  // User inputed D/W
       cout << "Enter in the amount of the " << transNames.at(i)  << " : $";     // Asks user amount of transaction
       cin >> numTrans.at(i);                                                    // User inputed amount of transactino
   }
   
   for (i = 0; i < numTrans.size(); ++i) { // For loop for checking input
       if (transNames.at(i) != "D" && transNames.at(i) != "d" && transNames.at(i) != "W" && transNames.at(i) != "w") { // If statement for invalid input (Error Checking)
       cout << endl;                                              // Creates a space
       cout << "----------------------------------------" << endl;// Input border
       cout << " INVALID ENTRY! D OR W WAS NOT ENTERED!" << endl; // Tells user input was invalid
       cout << " PROGRAM DID NOT RUN CORRECTLY!        " << endl; // Tells user the program did not run correctly
       cout << "----------------------------------------" << endl; // Input border
       }
   }
                                                        
   for (i = 0; i < numTrans.size(); ++i) { // For loop for calculating balances                       
      
      if (transNames.at(i) == "w" || transNames.at(i) == "W") { // If statement for if transaction is a withdrawal
      totTrans = totTrans - numTrans.at(i);                     // Equation for totTrans to calculate balance. Takes transaction amount away from original balance
      newBal.at(i) = totTrans;                                  // Sets vector equal to newly calculated balance
      } 
      
      if (transNames.at(i) == "d" || transNames.at(i) == "D") { // If statement for if transaction is a deposit 
          totTrans = totTrans + numTrans.at(i);                 // Equation for totTrans to calculate balance. Adds transaction amount to original balance
          newBal.at(i) = totTrans;                              // Sets vector equal to newly calculated balance 
      }
      
   }
 
    cout << endl;                                                        // Creates a space
    cout << "*************************************************" << endl; // Inputs top border
    cout << "*************************************************" << endl; // Inputs top border
    cout << "*********  CHECKBOOK BALANCE SHEET  *************" << endl; // Inputs title for all output 
    cout << "*************************************************" << endl; // Inputs part of top border
    cout << "   Beginning Balance " << setw(8) << "$   ";                // Ouputs title, aligns and sets dollar sign
    cout << fixed << setprecision(2) << begBal << endl;                  // Fixes, sets to two decimals and outputs original balance
    cout << "                **        **                 " << endl;             // Inputs border 
    cout << "   Transactions **        ** Amount    Balance           " << endl; // Inputs Column titles
    cout << "*************************************************" << endl;         // Inputs border
    for (i = 0; i < numTrans.size(); ++i) {                              // For loop to output each transaction
      cout << "    " << transNames.at(i);                                // Ouputs space and type of transaction (D/W)
                                  
          cout << right << setw(24) << "$   ";                // Ouputs and aligns dollar sign
          cout << fixed << setprecision(2) << numTrans.at(i); // Outputs, fixes and sets to two decimals the amount of transaction
          cout << right << setw(3) << "     $ ";              // Aligns and ouputs dollar sign
          cout << fixed << setprecision(2) << newBal.at(i);   // Outputs, fixes and sets to two decimals new balance
                                  
        cout << endl;                                                  // Creates a space
   }
    
    cout << "*************************************************" << endl;         // Inputs border
    cout << "  Total Balance" << setw(14) << "$   ";                             // Ouputs and aligns title and dollar sign
    cout << fixed << setprecision(2) << totTrans << endl;                        // Fixes, sets to two decimals and outputs Final and ending balance
    cout << "*************************************************" << endl;         // Inputs border
    cout << "*************************************************" << endl;         // Inputs border
    
    ofstream outFS; // Output file stream
    
    cout << "Do you want to copy the balance sheet to a file (Y/N): "; // Asks user if they want to copy output to a file 
        cin >> userAns;                                                // User inputed answer
                                   
        
    cout << " " << endl; // Creates a space
   
   
   outFS.open("check.txt"); // Opens file
   
   if (!outFS.is_open()) {                    // If statement for if the file could not be opened
      cout << "Could not open file." << endl; // Tells user the file could not be opened
      return 1;                               // Ends program
   }
   
   
   if (userAns == 'Y' || userAns == 'y') {  // If statement for if the user wants to copy the output to a file    
        
    outFS << "*************************************************" << endl; // Inputs top border
    outFS << "*************************************************" << endl; // Inputs top border
    outFS << "*********  CHECKBOOK BALANCE SHEET  *************" << endl; // Inputs title for all output 
    outFS << "*************************************************" << endl; // Inputs part of top border
    outFS << "   Beginning Balance " << setw(8) << "$   ";                // Ouputs title, aligns and sets dollar sign
    outFS << fixed << setprecision(2) << begBal << endl;                  // Fixes, sets to two decimals and outputs original balance
    outFS << "                **        **                 " << endl;             // Inputs border 
    outFS << "   Transactions **        ** Amount    Balance           " << endl; // Inputs Column titles
    outFS << "*************************************************" << endl;         // Inputs border
    for (i = 0; i < numTrans.size(); ++i) {                                       // For loop to output each transaction                     
      outFS << "    " << transNames.at(i);                                        // Ouputs space and type of transaction (D/W)
                                  
          outFS << right << setw(24) << "$   ";                // Ouputs and aligns dollar sign 
          outFS << fixed << setprecision(2) << numTrans.at(i); // Outputs, fixes and sets to two decimals the amount of transaction 
          outFS << right << setw(3) << "     $ ";              // Aligns and ouputs dollar sign
          outFS << fixed << setprecision(2) << newBal.at(i);   // Outputs, fixes and sets to two decimals new balance

      outFS << endl;                                                  // Creates a space
   }
    
    outFS << "*************************************************" << endl;         // Inputs border
    outFS << "  Total Balance" << setw(14) << "$   ";                             // Ouputs and aligns title and dollar sign
    outFS << fixed << setprecision(2) << totTrans << endl;                        // Fixes, sets to two decimals and outputs Final and ending balance
    outFS << "*************************************************" << endl;         // Inputs border
    outFS << "*************************************************" << endl;         // Inputs border 
    
    cout << "Copy was made to file!" << endl;   // Tells user the copy was made
 
   }
   
    
    else if (userAns == 'N' || userAns == 'n') { // Else if statement for if user doesn't want a copy
        
    cout << "'No' was entered so no copy was made on file." << endl; // Tells user no copy was made
    }
    
    
    else { // Else statement for if wrong input
            cout << "Y or N was not entered, so no copy was made on file! " << endl; // Tells user the input was invalid 
        }
   
   
   outFS.close(); // Closes the file
   
   	   error = cin.fail();                                                             // Sets bool error equal to a failed cin input
		
		if (error)                                                                  // If statement for invalid input (Error Checking)
			cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
   
    cout << endl;                                                             // Creates a space
    cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
    cin >> runProg;                                                           // User inputed answer
    
    while (runProg == 'Y' || runProg == 'y') {   // While loop for when the user wants to run the program again
    int error = 0;
	bool invalid = false;
    double begBal;            // Variable for original beginning balance
    vector <double> newBal;   // Vector for balance in between transactions
    double totTrans = 0;      // Variable for final balance
    char userAns;             // Variable for if the user wants to copy output to a file
    char runProg;             // Variable for if the user wants to run the program again
   vector<double> numTrans;   // Vector for dollar amount of each transaction
   vector<string> transNames; // Vector for if transaction is a deposit or withdrawal
   int numVals;               // Variable for number of transactions
   int i;                     // Variable for loops
   
   do{ // Do loop for error checking
   do{ // Do loop for error checking
   cout << "What is your beginning balance: "; // Asks user their beginning balance
   cin >> totTrans;                            // User inputed balance
      	   error = cin.fail();                                                             // Sets bool error equal to a failed cin input
		
		if (error)                                                                  // If statement for invalid input (Error Checking)
			cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
   
    cout << endl;                                                             // Creates a space
   
   begBal = totTrans;                          // Sets begBal equal to user inputed totTrans
   
   cout << "Enter in the number of transactions: "; // Asks user to enter in the number of transactions
   cin >> numVals;                                  // User inputed number of transactions             
   
   numTrans.resize(numVals);      // Resizes the vector to the number that the user inputed for numVals
   transNames.resize(numVals);    // Resizes the vector to the number that the user inputed for numVals  
   newBal.resize(numVals);        // Resizes the vector to the number that the user inputed for numVals
   
   cout << endl;                  // Creates a space  
   
   for (i = 0; i < numTrans.size(); ++i) {  // For loop for asking user if each transaction is D/W and the amount of it                         
       cout << "Is transaction " << i + 1 << " a deposit(D) or withdrawal(W): "; // Asks user if D/W 
       cin >> transNames.at(i);                                                  // User inputed D/W
       cout << "Enter in the amount of the " << transNames.at(i)  << " : $";     // Asks user amount of transaction
       cin >> numTrans.at(i);                                                    // User inputed amount of transactino
   }
   
      for (i = 0; i < numTrans.size(); ++i) { // For loop for checking input
       
       if (transNames.at(i) != "D" && transNames.at(i) != "d" && transNames.at(i) != "W" && transNames.at(i) != "w") { // If statement for invalid input (Error Checking)
       cout << endl;                                              // Creates a space
       cout << "----------------------------------------" << endl;// Input border
       cout << " INVALID ENTRY! D OR W WAS NOT ENTERED!" << endl; // Tells user input was invalid
       cout << " PROGRAM DID NOT RUN CORRECTLY!        " << endl; // Tels user the program did not run correctly 
       cout << "----------------------------------------" << endl;// Input border
       }
      }
   
                                                        
   for (i = 0; i < numTrans.size(); ++i) { // For loop for calculating balances                       
      
      if (transNames.at(i) == "w" || transNames.at(i) == "W") { // If statement for if transaction is a withdrawal
      totTrans = totTrans - numTrans.at(i);                     // Equation for totTrans to calculate balance. Takes transaction amount away from original balance
      newBal.at(i) = totTrans;                                  // Sets vector equal to newly calculated balance
      } 
      
      if (transNames.at(i) == "d" || transNames.at(i) == "D") { // If statement for if transaction is a deposit 
          totTrans = totTrans + numTrans.at(i);                 // Equation for totTrans to calculate balance. Adds transaction amount to original balance
          newBal.at(i) = totTrans;                              // Sets vector equal to newly calculated balance 
      }
      
   }
 
    cout << endl;                                                        // Creates a space
    cout << "*************************************************" << endl; // Inputs top border
    cout << "*************************************************" << endl; // Inputs top border
    cout << "*********  CHECKBOOK BALANCE SHEET  *************" << endl; // Inputs title for all output 
    cout << "*************************************************" << endl; // Inputs part of top border
    cout << "   Beginning Balance " << setw(8) << "$   ";                // Ouputs title, aligns and sets dollar sign
    cout << fixed << setprecision(2) << begBal << endl;                  // Fixes, sets to two decimals and outputs original balance
    cout << "                **        **                 " << endl;             // Inputs border 
    cout << "   Transactions **        ** Amount    Balance           " << endl; // Inputs Column titles
    cout << "*************************************************" << endl;         // Inputs border
    for (i = 0; i < numTrans.size(); ++i) {                              // For loop to output each transaction
      cout << "    " << transNames.at(i);                                // Ouputs space and type of transaction (D/W)
                                  
          cout << right << setw(24) << "$   ";                // Ouputs and aligns dollar sign
          cout << fixed << setprecision(2) << numTrans.at(i); // Outputs, fixes and sets to two decimals the amount of transaction
          cout << right << setw(3) << "     $ ";              // Aligns and ouputs dollar sign
          cout << fixed << setprecision(2) << newBal.at(i);   // Outputs, fixes and sets to two decimals new balance
                                  
        cout << endl;                                                  // Creates a space
   }
    
    cout << "*************************************************" << endl;         // Inputs border
    cout << "  Total Balance" << setw(14) << "$   ";                             // Ouputs and aligns title and dollar sign
    cout << fixed << setprecision(2) << totTrans << endl;                        // Fixes, sets to two decimals and outputs Final and ending balance
    cout << "*************************************************" << endl;         // Inputs border
    cout << "*************************************************" << endl;         // Inputs border
    
    ofstream outFS; // Output file stream
 
    cout << "Do you want to copy the balance sheet to a file (Y/N): "; // Asks user if they want to copy output to a file 
        cin >> userAns;                                                // User inputed answer
                                   
        
    cout << " " << endl; // Creates a space
   
   
   outFS.open("check.txt"); // Opens file
   
   if (!outFS.is_open()) {                    // If statement for if the file could not be opened
      cout << "Could not open file." << endl; // Tells user the file could not be opened
      return 1;                               // Ends program
   }
   
   
   if (userAns == 'Y' || userAns == 'y') {  // If statement for if the user wants to copy the output to a file    
        
    outFS << "*************************************************" << endl; // Inputs top border
    outFS << "*************************************************" << endl; // Inputs top border
    outFS << "*********  CHECKBOOK BALANCE SHEET  *************" << endl; // Inputs title for all output 
    outFS << "*************************************************" << endl; // Inputs part of top border
    outFS << "   Beginning Balance " << setw(8) << "$   ";                // Ouputs title, aligns and sets dollar sign
    outFS << fixed << setprecision(2) << begBal << endl;                  // Fixes, sets to two decimals and outputs original balance
    outFS << "                **        **                 " << endl;             // Inputs border 
    outFS << "   Transactions **        ** Amount    Balance           " << endl; // Inputs Column titles
    outFS << "*************************************************" << endl;         // Inputs border
    for (i = 0; i < numTrans.size(); ++i) {                                       // For loop to output each transaction                     
      outFS << "    " << transNames.at(i);                                        // Ouputs space and type of transaction (D/W)
                                  
          outFS << right << setw(24) << "$   ";                // Ouputs and aligns dollar sign 
          outFS << fixed << setprecision(2) << numTrans.at(i); // Outputs, fixes and sets to two decimals the amount of transaction 
          outFS << right << setw(3) << "     $ ";              // Aligns and ouputs dollar sign
          outFS << fixed << setprecision(2) << newBal.at(i);   // Outputs, fixes and sets to two decimals new balance

      outFS << endl;                                                  // Creates a space
   }
    
    outFS << "*************************************************" << endl;         // Inputs border
    outFS << "  Total Balance" << setw(14) << "$   ";                             // Ouputs and aligns title and dollar sign
    outFS << fixed << setprecision(2) << totTrans << endl;                        // Fixes, sets to two decimals and outputs Final and ending balance
    outFS << "*************************************************" << endl;         // Inputs border
    outFS << "*************************************************" << endl;         // Inputs border 
    
    cout << "Copy was made to file!" << endl;   // Tells user the copy was made
       
   }
    
    else if (userAns == 'N' || userAns == 'n') { // Else if statement for if user doesn't want a copy
        
    cout << "'No' was entered so no copy was made on file." << endl; // Tells user no copy was made
    }
    
    else { // Else statement for if wrong input
            cout << "Y or N was not entered, so no copy was made on file! " << endl; // Tells user the input was invalid 
            }
            
     outFS.close(); // Closes the file
     
        	   invalid = cin.fail();                                                             // Sets bool error equal to a failed cin input
		
		if (invalid)                                                                  // If statement for invalid input (Error Checking)
			cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(invalid);                                                                 // While statement for invalid input
        
        cout << endl;                                                             // Creates a space
        cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
        cin >> runProg;                                                           // User inputed answer
    
       if (runProg == 'N' || runProg == 'n') { // Second while loop for 2+ times running through the program when user wants to end the program 
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Lines 860-868 inputs border/title
            cout << "-------------------------------------------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------          THANK-YOU          -------" << endl; 
            cout << "-------          FOR USING          -------" << endl; 
            cout << "-------         OUR PROGRAM!        -------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------------------------------------------" << endl; 
            cout << "-------------------------------------------" << endl; 
                break;                               // Ends while loop
            }
            
            
        
    }
        
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for original function when user wants to end the program
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // !! ** Lines 875-883 inputs border/title ** !!
            cout << "-------------------------------------------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------          THANK-YOU          -------" << endl;
            cout << "-------          FOR USING          -------" << endl; 
            cout << "-------         OUR PROGRAM!        -------" << endl; 
            cout << "-------                             -------" << endl; 
            cout << "-------------------------------------------" << endl; 
            cout << "-------------------------------------------" << endl; 
                                                      
            }
            
            cout << "Press Y to go back to the main menu: "; // Asks user if they want to return to the main menu  
        }
        
        else if (numOp == 4) { // Else if statment for program 4
    int invalid = 0;
	bool error = false;

int civHour;     // Variable for civilian hour
int civMin;      // Variable for civilian minute
char userType;   // Variable for civilian or military
string timeType; // Variable for AM or PM
int milHour;     // Variable for military hour
int milMin;      // Variable for military minute
char runProg;    // Variable for if the user wants to run the program again
   
    cout << "--------------------------------------------------------------------" << endl; // Input border
    cout << "----------     WELCOM TO THE TIME CONVERSTION PROGRAM!    ----------" << endl; // Input border and title
    cout << "---------- HERE YOU CAN CONVERT CIVILIAN TIME TO MILITARY ----------" << endl; // Input border and title
    cout << "----------         AND MILITARY TIME TO CIVILIAN!         ----------" << endl; // Input border and title
    cout << "--------------------------------------------------------------------" << endl; // Input border
    cout << endl; 
    cout << "Is the time Civilian (C) or Military (M) ? "; // Asks the user if it is civilian or military time   
        cin >> userType;                                   // User inputed answer 
        
    cout << " " << endl;                                   // Space in between input and output. 

     if (userType == 'C' || userType == 'c') {          // If statement for if it is civilian time
        
        cout << "Enter the time in civilian: " << endl; // Tells user to enter in the civilian time
        cout << "Enter the hour: ";                     // Tells user to enter in civilian hour 
        cin >> civHour;                                 // User inputed civilian hour
        cout << "Enter the minutes: ";                  // Tells user to enter civilian minutes
        cin >> civMin;                                  // User inputed civilian minutes
        cout << "Enter AM or PM: ";                     // Tells user to enter AM or PM
        cin >> timeType;                                // User inputed AM or PM
        cout << endl;                                   // Creates a space
        
        if (timeType != "AM" && timeType != "Am" && timeType != "aM" && timeType != "am" && timeType != "PM" && timeType != "pM" && timeType != "Pm" && timeType != "pm") { // If statement for invalid entry (Error Checking)
            cout << "Invalid Entry! AM or PM was not entered!" << endl; // Tells user input was invalid
        }
        
       if (civHour >= 1 && civHour <= 11 && (timeType == "AM" || timeType == "Am" || timeType == "am" || timeType == "aM")) { // If statement for civilian time between 1-11 and AM
        cout << "************    TIME CONVERSION   ************" << endl;  // Inputs border and output title
        cout << "**********************************************" << endl;  // Inputs border
        cout << "**                                          **" << endl;  // Inputs border
        cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0. 
        cout << "Military time is: " << "0" << civHour << setfill('0') << setw(2) <<  civMin << endl;                   // Outputs converted military time. Fills space in time with 0. 
        cout << "**                                          **" << endl; // Inputs border
        cout << "**********************************************" << endl; // Inputs border
        
        }
        
        else if (civHour >= 1 && civHour <= 11 && (timeType == "PM" || timeType == "Pm" || timeType == "pm" || timeType == "pM")) { // Else if statement for civilian time between 1-11 and PM
        cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
        cout << "**********************************************" << endl; // Inputs border 
        cout << "**                                          **" << endl; // Inputs border 
        cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin  << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
        civHour = civHour + 12;                                           // Equation to convert civilian hours to military hours
        cout << "Military time is: " << civHour << fixed << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
        cout << "**                                          **" << endl; // Inputs border 
        cout << "**********************************************" << endl; // Inputs border 
        
        }
        
         else if (civHour == 12 && (timeType == "PM" || timeType == "pm" || timeType == "Pm" || timeType == "pM") && civMin == 0 || civMin == 00)  { // Else if statement for 12 civilian hours and 0 minutes and PM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title 
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour;                                           // Equation to convert civilian hours to military hours
            cout << "Military time isx: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
            
         }
        
       else if (civHour == 12 && (timeType == "AM" || timeType == "am" || timeType == "Am" || timeType == "aM") && civMin == 0 || civMin == 00)  { // Else if statement for 12 civilian hours and 0 minutes and AM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title 
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour + 12;                                           // Equation to convert civilian hours to military hours
            cout << "Military time isx: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
            
            
        }
        
        else if (civHour == 12 && (timeType == "PM" || timeType == "pm" || timeType == "Pm" || timeType == "pM") && civMin >= 01) { //Else if statement for 12 civilian hours and 1+ minutes and PM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour;                                                // Equation to convert civilian hours to military hours
            cout << "Military time is: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
       
        else if (civHour == 12 && (timeType == "AM" || timeType == "am" || timeType == "Am" || timeType == "aM") && civMin >= 01) { // Esle if statement for 12 civilian hours, 1+ minutes and AM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour - 12;                                           // Equation to convert civilian hours to military hours
            cout << "Military time is: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        
    }
    
    else if (userType == 'M' || userType == 'm') {      // Else if statement for if it is military time  
        
        cout << "Enter the time in military: " << endl; // Ask user to input military time
        cout << "Enter the hour: ";                     // Ask user to input military hours
        cin >> milHour;                                 // User inputed military hours
        cout << "Enter the minutes: ";                  // Ask user to input miltary minutes
        cin >> milMin;                                  // User inputed military minutes
        cout << endl;                                   // Creates a space
        
        if (milHour == 24 && (milMin == 0 || milMin == 00)) {                 // If statement for 24 military hours and 0 minutes 
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2)  << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour - 12;                                           // Equation to converty military hours to civilian
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " AM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
        }
        
        else if (milHour >= 13 && milHour <= 23) {                            // Else if statement for 13-23 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2) << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour - 12;                                           // Equation to convert military hours to civilian
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " PM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        else if (milHour < 12) {                                              // Else if statement for less than 12 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2)  << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour;                                                // Equation for military hours
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " AM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        else if (milHour == 12) {                                             // Else if statement for 12 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2) << milMin << endl; // Ouputs military time. Fills time spaces with 0. 
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " PM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
    }
    
    else { 
            cout << "C or M was not entered! No time was calculated!" << endl; // Else statement for wrong input. 
                                                                                  
        }
        
    cout << endl;                                                             // Creates a space
    cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
    cin >> runProg;                                                           // User inputed answer
    cout << endl;
    
    while (runProg == 'Y' || runProg == 'y') {   // While loop for when the user wants to run the program again
        
int civHour;     // Variable for civilian hour
int civMin;      // Variable for civilian minute
char userType;   // Variable for civilian or military
string timeType; // Variable for AM or PM
int milHour;     // Variable for military hour
int milMin;      // Variable for military minute
char runProg;    // Variable for if the user wants to run the program again

    do{ // Do loop for error checking
    cout << "Is the time Civilian (C) or Military (M) ? "; // Asks the user if it is civilian or military time   
        cin >> userType;                                   // User inputed answer 
        
    cout << " " << endl;                                   // Space in between input and output. 

     if (userType == 'C' || userType == 'c') {          // If statement for if it is civilian time
        
        cout << "Enter the time in civilian: " << endl; // Tells user to enter in the civilian time
        cout << "Enter the hour: ";                     // Tells user to enter in civilian hour 
        cin >> civHour;                                 // User inputed civilian hour
        cout << "Enter the minutes: ";                  // Tells user to enter civilian minutes
        cin >> civMin;                                  // User inputed civilian minutes
        cout << "Enter AM or PM: ";                     // Tells user to enter AM or PM
        cin >> timeType;                                // User inputed AM or PM
        cout << endl;                                   // Creates a space
        
        if (timeType != "AM" && timeType != "Am" && timeType != "aM" && timeType != "am" && timeType != "PM" && timeType != "pM" && timeType != "Pm" && timeType != "pm") { // If statment for invalid input (Error Checking)
            cout << "Invalid Entry! AM or PM was not entered!" << endl; // Tells user input was invalid 
        }
        
       if (civHour >= 1 && civHour <= 11 && (timeType == "AM" || timeType == "Am" || timeType == "am" || timeType == "aM")) { // If statement for civilian time between 1-11 and AM
        cout << "************    TIME CONVERSION   ************" << endl;  // Inputs border and output title
        cout << "**********************************************" << endl;  // Inputs border
        cout << "**                                          **" << endl;  // Inputs border
        cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0. 
        cout << "Military time is: " << "0" << civHour << setfill('0') << setw(2) <<  civMin << endl;                   // Outputs converted military time. Fills space in time with 0. 
        cout << "**                                          **" << endl; // Inputs border
        cout << "**********************************************" << endl; // Inputs border
        
        }
        
        else if (civHour >= 1 && civHour <= 11 && (timeType == "PM" || timeType == "Pm" || timeType == "pm" || timeType == "pM")) { // Else if statement for civilian time between 1-11 and PM
        cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
        cout << "**********************************************" << endl; // Inputs border 
        cout << "**                                          **" << endl; // Inputs border 
        cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin  << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
        civHour = civHour + 12;                                           // Equation to convert civilian hours to military hours
        cout << "Military time is: " << civHour << fixed << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
        cout << "**                                          **" << endl; // Inputs border 
        cout << "**********************************************" << endl; // Inputs border 
        
        }
        
         else if (civHour == 12 && (timeType == "PM" || timeType == "pm" || timeType == "Pm" || timeType == "pM") && civMin == 0 || civMin == 00)  { // Else if statement for 12 civilian hours and 0 minutes and PM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title 
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour;                                           // Equation to convert civilian hours to military hours
            cout << "Military time isx: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
            
         }
        
       else if (civHour == 12 && (timeType == "AM" || timeType == "am" || timeType == "Am" || timeType == "aM") && civMin == 0 || civMin == 00)  { // Else if statement for 12 civilian hours and 0 minutes and AM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title 
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour + 12;                                           // Equation to convert civilian hours to military hours
            cout << "Military time isx: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
            
            
        }
        
        else if (civHour == 12 && (timeType == "PM" || timeType == "pm" || timeType == "Pm" || timeType == "pM") && civMin >= 01) { //Else if statement for 12 civilian hours and 1+ minutes and PM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour;                                                // Equation to convert civilian hours to military hours
            cout << "Military time is: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
       
        else if (civHour == 12 && (timeType == "AM" || timeType == "am" || timeType == "Am" || timeType == "aM") && civMin >= 01) { // Esle if statement for 12 civilian hours, 1+ minutes and AM
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Civilian Time is: " << civHour << ":" << setfill('0') << setw(2) << civMin << " " << timeType << endl; // Ouputs civilian time and AM/PM. Fills space in time with 0.
            civHour = civHour - 12;                                           // Equation to convert civilian hours to military hours
            cout << "Military time is: " << civHour << setfill('0') << setw(2) << civMin << endl; // Outputs converted military time. Fills space in time with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        
    }
    
    else if (userType == 'M' || userType == 'm') {      // Else if statement for if it is military time  
        
        cout << "Enter the time in military: " << endl; // Ask user to input military time
        cout << "Enter the hour: ";                     // Ask user to input military hours
        cin >> milHour;                                 // User inputed military hours
        cout << "Enter the minutes: ";                  // Ask user to input miltary minutes
        cin >> milMin;                                  // User inputed military minutes
        cout << endl;                                   // Creates a space
        
        if (milHour == 24 && (milMin == 0 || milMin == 00)) {                 // If statement for 24 military hours and 0 minutes 
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2)  << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour - 12;                                           // Equation to converty military hours to civilian
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " AM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border
        }
        
        else if (milHour >= 13 && milHour <= 23) {                            // Else if statement for 13-23 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2) << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour - 12;                                           // Equation to convert military hours to civilian
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " PM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0. 
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        else if (milHour < 12) {                                              // Else if statement for less than 12 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border 
            cout << "**                                          **" << endl; // Inputs border
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2)  << milMin << endl; // Ouputs military time. Fills time spaces with 0.
            milHour = milHour;                                                // Equation for military hours
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " AM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
        
        else if (milHour == 12) {                                             // Else if statement for 12 military hours
            cout << "************    TIME CONVERSION   ************" << endl; // Inputs border and output title
            cout << "**********************************************" << endl; // Inputs border
            cout << "**                                          **" << endl; // Inputs border 
            cout << "Military Time is: " << setfill('0') << setw(2) << milHour << setfill('0') << setw(2) << milMin << endl; // Ouputs military time. Fills time spaces with 0. 
            cout << "Civilian Time is: " << milHour << ":" << setfill('0') << setw(2) << milMin << " PM" << endl; // Outputs converted civilian time and AM/PM. Fills time spaces with 0.
            cout << "**                                          **" << endl; // Inputs border 
            cout << "**********************************************" << endl; // Inputs border 
        }
    }
    
    else { 
            cout << "C or M was not entered! No time was calculated!" << endl; // Else statement for wrong input. 
                                                                                  
        }
    
        if (error)                                                                  // If statement for invalid input (Error Checking)
		cout << "Invalid reply! Please enter a valid number response!" << endl; // Tells user they had an invalid reply
		cin.clear();                                                                // Clears the invalid cin input
		cin.ignore(10, '\n');                                                       // Skips 10 characters or until a newline
	} while(error);                                                                 // While statement for invalid input
        cout << endl;                                                               // Creates a space
    
        cout << endl;                                                             // Creates a space
        cout << "Do you want to run the program again? (Y/N): ";                  // Asks user if they want to run the program again
        cin >> runProg;                                                           // User inputed answer
        cout << endl;                                                             // Creates a space
    
       if (runProg == 'N' || runProg == 'n') { // Second while loop for 2+ times running through the program when user wants to end the program 
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
                break;                               // Ends while loop
            }
            
            if (runProg != 'N' && runProg != 'n' && runProg != 'Y' && runProg != 'y') { // If statement for invalid input (Error Checking)
                break;                               // Ends while loop
            }
        
    }
        
    
            if (runProg == 'N' || runProg == 'n') { // Second while loop for original function when user wants to end the program
                cout << endl;                          // Creates space
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
                                                      
            }
            
            cout << "Press Y to go back to the main menu: "; // Asks user if they want to return to the main menu 
        }
        
        else if (numOp == 5) { // Else if statment for program 5
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            
            return 0; // Ends program
        }
    
        
        cin >> mMenu; // User inputed answer
    
    }
    
    while (mMenu == 'n' || mMenu == 'N') { // While loop for while mMenu = 0 and user wants to end the program
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
        return 0; // Ends program
         
    }
    
    while (mMenu != 'y' && mMenu !='Y' && mMenu != 'n' && mMenu != 'N') { // While loop for invalid input (Error Checking)
        cout << "Invalid entry! Press Y to go back to the main menu: "; // Tells user input was invalid and asks if they want to return to the main menu
         cin >> mMenu; // User inputed answer
        
        if (mMenu == 'n' || mMenu == 'N') { // If statment for if user does not want to continue
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------                             -------" << endl; // Input border
            cout << "-------          THANK-YOU          -------" << endl; // Input border and title
            cout << "-------          FOR USING          -------" << endl; // Input border and title
            cout << "-------         OUR PROGRAM!        -------" << endl; // Input border and title
            cout << "-------                             -------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border
            cout << "-------------------------------------------" << endl; // Input border 
            return 0; // Ends program 
        }
    }
}
return 0; } // End of Main function
