#include <iostream>
#include <string>

using namespace std;

int main()
{
   //array to hold the 9 spots for the tic-tac-toe board
   char arr[9];

   //char array to hold the players signs (i.e. 'x' and 'o)
   char player[2] = {'O', 'X'};

   //string array to hold players names
   string names[2] = {"", ""};

   //player name variables
   string player1 = "",
          player2 = "";

   //welcome message
   cout << "Welcome to my tic-tac-toe game!!!!!!" << endl << endl
        << "This is a 2-player game. GOODLUCK!" << endl << endl
        << "Player 1: Enter your name: ";
  
   //getting players names
   getline(cin, player1);

   names[0] = player1;

   cout << "Player 2: Enter your name: ";

   getline(cin, player2);

   names[1] = player2;
   
   //flag to hold whether a row of 3 is found
   bool flag = false;
   
   //keeps track of which players turn it is.(using % 2 for odd and even)
   int plyrcount = 0;

   //players option initialized to yes('y') -> any key will stop the game
   char again = 'y';

   //game will continue untill a player presses any key besides 'y' || 'Y'
   while(again == 'y' || again == 'Y'){
        
        //for-loop to initialize array to {1,2,3,4...9} at the start of every game
        for(int i = 0; i < 9; i++)
           arr[i] = 49 + i;

   //while flag == false == a row of 3 'o' || 'x' have not been found
      while(flag == false)
           {
           // choice 1-9 to determine which spot the user wants to place their symbol
           int choice; 
         
           //displays array/tic-tac-toe grid
           cout << endl << endl << arr[0] << " | " << arr[1] << " | " << arr[2] <<  endl
                << " ___________ " << endl
                << arr[3] << " | " << arr[4] << " | " << arr[5] << endl
                << " ___________ " << endl
                << arr[6] << " | " << arr[7] << " | " << arr[8] << endl 
                << "____________________________________________" << endl << endl;

           //displays player 1s name 
           if(plyrcount % 2 == 0)
             cout << names[0] << ", choose a number to enter your O" << endl
                  << "______________________________________________" << endl << endl;
           //displays player 2s name
           else
             cout << names[1] << ", choose a number to enter your X" << endl
                  << "_______________________________________________" << endl << endl;

           //flag to detect whether a spot on the grid is already taken
           bool flag = false; 

           cin >> choice;

         //while-loop to validate user's choice
         while(choice < 1 || choice > 9)
              {
              cout << "Invalid choice. Choose again: ";
              cin >> choice;
              }

           while(flag == false)
                { 
                //if-statement to check whether a spot is already taken    
                if(arr[choice - 1] == 'O'|| arr[choice -1 ] == 'X')
                   {
                   flag = false;

                   cout << "Spot is already taken. Choose again!" << endl << endl;

                   cin >> choice;
                   }
                 else 
                   //spot on the grid is not taken
                   flag = true;
                 }
        
                 //if statement to determine whether player 1 or 2 is choosing 
          if(plyrcount % 2 == 0)
             arr[choice - 1] = 'O';
          else 
             arr[choice - 1] = 'X';

            //if statement to detect 3 in a row 
            if((arr[0] == 'O' && arr[1] =='O' && arr[2] == 'O') || 
              (arr[0] == 'X' && arr[1] =='X' && arr[2] == 'X') ||
              (arr[3] == 'O' && arr[4] =='O' && arr[5] == 'O') || 
              (arr[3] == 'X' && arr[4] =='X' && arr[5] == 'X') ||
              (arr[6] == 'O' && arr[7] =='O' && arr[8] == 'O') || 
              (arr[6] == 'X' && arr[7] =='X' && arr[8] == 'X') ||
              (arr[0] == 'O' && arr[3] =='O' && arr[6] == 'O') || 
              (arr[0] == 'X' && arr[3] =='X' && arr[6] == 'X') ||
              (arr[1] == 'O' && arr[4] =='O' && arr[7] == 'O') || 
              (arr[1] == 'X' && arr[4] =='X' && arr[7] == 'X') ||
              (arr[2] == 'O' && arr[5] =='O' && arr[8] == 'O') || 
              (arr[2] == 'X' && arr[5] =='X' && arr[8] == 'X') ||
              (arr[0] == 'O' && arr[4] =='O' && arr[8] == 'O') || 
              (arr[0] == 'X' && arr[4] =='X' && arr[8] == 'X') ||
              (arr[2] == 'O' && arr[4] =='O' && arr[6] == 'O') || 
              (arr[2] == 'X' && arr[4] =='X' && arr[6] == 'X'))
              {
               //displays player 2s name, if they won
               if(plyrcount % 2 == 1)
                {
                cout << endl << endl << names[1] << " has won!!!!!!!!!!" << endl;
                break;
                }
               else 
                {
                //displays player 1s name, if they won
                cout << endl << endl << names[0] << " has won!!!!!!!!!!" << endl;         
                break;
                }
                //3 symbols in a row have been found and the game stops
                flag = true;
                }	
            else
            //3-in-a-row symbols have not been found
            flag = false;

            //counter variable to switch between player 1 & 2
            plyrcount++;

       }
        cout << endl << endl << "Would you like to play again (y or Y for yes, any other"
                                "  key to stop?";
      
        cin >> again;
    }
   return 0;
}
