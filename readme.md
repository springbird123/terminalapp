# terminalapp
Repository Link: https://github.com/danielkellydev/dispensary_manager

Presentation Link: https://watch.screencastify.com/v/Fyy6sKvs4ceahntxuAkL

# Code style
This application follows the PEP 8 code style.

[PEP 8 – Style Guide for Python Code](https://peps.python.org/pep-0008/)



# Features

### Feature 1 Main Navigation Menu
This feature allows users to select different options on this application.
It firstly uses a welcome function to clear the screen and load the logo and welcome message.
It displays all the main options that the user can select by entering the number before the option. The application will execute the function corresponding to the option using if/else conditions.
If user's input is not a number between 1-4 or any other invalid, an error message will be displayed. Then the user can try again.

### Feature 2 Create a saving goal
This feature allows the users to create a new saving goal and this new saving goal will be saved in a csv file for future use.
The users will be asked to input the name of the new saving goal and the goal amount they want to save.
When the goal amount input is not a number above 0, an error prompt will be displayed and user can try again.


### Feature 3 Add Money 
This feature allows the users to add money to saving goals (one saving goal at a time).
User will be asked to choose the goal they want to add money by inputing index of the goal. Then they can input the amount they want to add. 
Then check_process feature will be excuted to add the amount to the current amount. the "current amount" and the "process" will be updated and saved in csv file and updated saving goal will be displayed. 
Error handling: when there is no saving goal in the csv file, this feature will not run; when the amount input is not a number above 0, an error prompt will be displayed and user can try again; when current amount is below 0, it will not be updated and an error prompt will be displayed.

### Feature 4 View saving goal(s)
This feature allows the users to view all the saving goals.
if there is no saving goal in the csv file, a message "There is no saving goal yet, return to the main menu to create a new one!" and ASCII text"EMPTY......" will be displayed and user can return to main menu.

### Feature 5 Edit saving goal(s)
This feature allows the users to choose other edit features such as, change the goal name, change the goal amount, and delete a saving goal.
It uses "view saving goals" feature (feature 4) to display all the saving goals, user will be asked to choose edit feature by inputing edit number. then it displays the editing menu that the user can select by entering the number before the option. The application will execute the feature corresponding to the option using if/else conditions.
Error handling: When users index is not valid, this feature will not run; if user's input is not a number between 1-5 or any other invalid input, an error message will be displayed. Then the user can try again.

### Feature 6 Edit the goal name
This feature allows the users to edit the goal name.
The users will be asked to input the new saving name, then this new saving name will be saved in a csv file and displayed.

### Feature 7 Edit the goal amount
This feature allows the users to edit the goal amount.
The users will be asked to input the new goal amount, then Check_process fuction will  be excuted to update the goal amount. The "Current amount" and the "Process" will be updated and saved in csv file and updated saving goal will be displayed.
Error handling: if the new goal amount is below 0, the file will not be updated and an error prompt will be displayed.

### Feature 8 Delete the goal
This feature allows the users to delete saving goals.
The deleted saving goal will be removed from the csv file, and the updated goal list or empty goal table message will be displayed.

#  Implementation plan
Trello Board link: https://trello.com/b/J0Msym7k/t1a3

# Help documentation


# Manual Tests

### Manual Test 1
To test weather a new goal is correct added.

Case 1, a new goal with a valid saving amount 100 is saved in saving_goal.csv: 
1.	Run main.py, main menu displays
2.	From menu, input "1"   to add a new saving goal, screen shows "Please enter the goal name: "
3.	Enter "A new goal", screen shows "Please enter the amount you want to save: ".
4.	Enter "100", screen shows "Your new saving goal has been created!". and "Please Press Enter to back to menu: ". The "saving_goal.csv" file will include a new goal named "A new goal" with current amount "0", current amount "100", and process "0%".
5.	Press "Enter", main menu displays. 

Case 2, a new goal with a invalid saving amount '-100' is not successfully created and amount input prompt until valid saving amount is inputed.
1.	Run main.py, main menu displays
2.	From menu, input "1"   to add a new saving goal, screen shows "Please enter the goal name: "

3.	Enter "A new goal", screen shows "Please enter the amount you want to save: "
4.	Enter "-100", screen shows "Please enter a positive number." and "Please enter the amount you want to save: " again. The "saving_goal.csv" file is not changed
5.  Enter "x", screen shows "Please enter a valid amount" and "Please enter the amount you want to save: " again. The "saving_goal.csv" file is not changed
6.  Enter "100", screen shows "Your new saving goal has been created!". and "Please Press Enter to back to menu: ". The "saving_goal.csv" file will include a new goal named "A new goal" with current amount "0", current amount "100", and process "0%".
7.	Press Enter, main menu displays. 

### Manual Test 2
Check when edit 
case