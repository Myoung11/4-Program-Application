# 4-Program-Application
# C++
Driven by a menu screen. User can choose which program to enter using the menu screen. Can exit using the menu screen. Thank you screen when user exits.
# Programs
♣	Calculate Sales Tax on Multiple Items (Sales Receipt)
♣	Customer Contact Card (User inputs info, outputs info in card format)
♣	Check Book Balancer (Input deposits, withdrawals, beg balance, will balance and keep track of check book)
♣ Time Converter (Military and Civilian)

OUTPUT FORMAT IS NOT DISPLAYED CORRECTLY IN DESCRIPTION. IT IS FORMATTED CORRECTLY WHEN PROGRAM IS RUN.

# Exmaple Input/Output from Start 
-------------------------------------------                                                              
-------------------------------------------                                                              
----------     HELLO WELCOME     ----------                                                              
----------     TO THE PROGRAM    ----------                                                              
-------------------------------------------                                                              
-------------------------------------------                                                              
Enter your first name: Matt                                                                              
                                                                                                         
-------------------------------------------                                                              
-------------------------------------------                                                              
----------          HELLO        ----------                                                              
----------           Matt         ----------                                                             
-------------------------------------------                                                              
-------------------------------------------                                                              
Press Y to continue: Y                                                                                   
                                                                                                         
       -------------------------------------------                                                       
       -------------------------------------------                                                       
       -------          MAIN MENU          -------                                                       
       -------------------------------------------                                                       
       -------------------------------------------                                                       
                                                                                                         
 Number                   Operation                                                                      
***************************************************************************                              
 1  ..................... Calculate Sales Tax on Multiple Sales Items                                    
 2  ..................... Create a Customer Contact Card                                                 
 3  ..................... Balance a Checkbook                                                            
 4  ..................... Time Conversion Utility                                                        
 5  ..................... Exit                                                                           
***************************************************************************                              
                                                                                                         
Enter the desired operation: 1  

# Example Input/Output from Sales Receipt
*******************************************************************                                      
*********                                                **********                                      
**********     WELCOME TO THE SALES RECEIPT PROGRAM!     **********                                      
********** THIS PROGRAM WILL COMPUTE A RECEIPT THAT WILL **********                                      
**********  DISPLAY THE NAME AND PRICE OF A SALES ITEM,  **********                                      
**********  THE TOTAL SALES PRICE, THE TOTAL SALES TAX,  **********                                      
**********  AND THE GRAND TOTAL PRICE OF THE PURCHASE    **********                                      
**********                                               **********                                      
*******************************************************************                                      
Press Y to continue: y                                                                                   
                                                                                                         
Enter in the number of sales items to be calculated: 2                                                   
                                                                                                         
Enter in the name of sales item number 1: pen                                                            
Enter in the price of the pen : $1.00                                                                    
Enter in the name of sales item number 2: pencil                                                         
Enter in the price of the pencil : $2.34                                                                 
                                                                                                         
Enter in the sales tax percentage                                                                        
(Enter 10 for 10%): 6  

*********************************************                                                            
*********************************************                                                            
********  S A L E S  R E C E I P T  *********                                                            
*********************************************                                                            
**              **        **               **                                                            
**  Item Names  **        **   Price       **                                                            
*********************************************                                                            
**  pen                  $    1.00                                                                       
**  pencil              $   2.34                                                                         
*********************************************                                                            
**  Sales Total          $   3.34                                                                        
**  Sales Tax            $    0.20                                                                       
**                        ----------                                                                     
**  Grand Total          $   3.54                                                                        
**                                         **                                                            
*********************************************                                                            
*********************************************                                                            
                                                                                                         
Do you want to run the program again? (Y/N): n 

# Example Input/Output from Customer Contact Card
Enter customer's full name: Joe Smith                                                                    
Enter Street Address (Ex: 123 Main Street): 123 Main Street                                              
Enter City: New York                                                                                     
Enter State: New York                                                                                    
Enter Zip Code: 12345                                                                                    
Enter Phone Number: (123)-456-7890                                                                       
                                                                                                         
****************************************                                                                 
****************    JS    **************                                                                 
****************************************                                                                 
***           CONTACT CARD           ***                                                                 
****************************************                                                                 
***                                  ***                                                                 
*** Joe Smith                                                                                            
*** 123 Main Street                                                                                      
*** New York, New York 12345                                                                             
*** (123)-456-7890                                                                                       
***                                   ***                                                                
*****************************************                                                                
                                                                                                         
Would you like to create another contact card? (Y/N): n 

# Example Input/Output from Check Book Balancer
What is your beginning balance: 500                                                                      
Enter in the number of transactions: 2                                                                   
                                                                                                         
Is transaction 1 a deposit(D) or withdrawal(W): d                                                        
Enter in the amount of the d : $300                                                                      
Is transaction 2 a deposit(D) or withdrawal(W): w                                                        
Enter in the amount of the w : $100                                                                      
                                                                                                         
*************************************************                                                        
*************************************************                                                        
*********  CHECKBOOK BALANCE SHEET  *************                                                        
*************************************************                                                        
   Beginning Balance     $   500.00                                                                      
                **        **                                                                             
   Transactions **        ** Amount    Balance                                                           
*************************************************                                                        
    d                    $   300.00     $ 800.00                                                         
    w                    $   100.00     $ 700.00                                                         
*************************************************                                                        
  Total Balance          $   700.00                                                                      
*************************************************                                                        
*************************************************                                                        
Do you want to copy the balance sheet to a file (Y/N): y                                                 
                                                                                                         
Copy was made to file!                                                                                   
                                                                                                         
Do you want to run the program again? (Y/N): n  

# Example Input/Output from Time Converter
--------------------------------------------------------------------                                     
----------     WELCOM TO THE TIME CONVERSTION PROGRAM!    ----------                                     
---------- HERE YOU CAN CONVERT CIVILIAN TIME TO MILITARY ----------                                     
----------         AND MILITARY TIME TO CIVILIAN!         ----------                                     
--------------------------------------------------------------------                                     
                                                                                                         
Is the time Civilian (C) or Military (M) ? c                                                             
                                                                                                         
Enter the time in civilian:                                                                              
Enter the hour: 1                                                                                        
Enter the minutes: 34                                                                                    
Enter AM or PM: am                                                                                       
                                                                                                         
************    TIME CONVERSION   ************                                                           
**********************************************                                                           
**                                          **                                                           
Civilian Time is: 1:34 am                                                                                
Military time is: 0134                                                                                   
**                                          **                                                           
**********************************************                                                           
                                                                                                         
Do you want to run the program again? (Y/N): n  

# Example of Exit
Press Y to go back to the main menu: y                                                                   
       -------------------------------------------                                                       
       -------------------------------------------                                                       
       -------          MAIN MENU          -------                                                       
       -------------------------------------------                                                       
       -------------------------------------------                                                       
                                                                                                         
 Number                   Operation                                                                      
***************************************************************************                              
 1  ..................... Calculate Sales Tax on Multiple Sales Items                                    
 2  ..................... Create a Customer Contact Card                                                 
 3  ..................... Balance a Checkbook                                                            
 4  ..................... Time Conversion Utility                                                        
 5  ..................... Exit                                                                           
***************************************************************************                              
                                                                                                         
Enter the desired operation: 5                                                                           
                                                                                                         
-------------------------------------------                                                              
-------------------------------------------                                                              
-------                             -------                                                              
-------          THANK-YOU          -------                                                              
-------          FOR USING          -------                                                              
-------         OUR PROGRAM!        -------                                                              
-------                             -------                                                              
-------------------------------------------                                                              
------------------------------------------- 

