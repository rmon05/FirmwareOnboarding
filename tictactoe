#include <bits/stdc++.h>
using namespace std;


// 3x3 int array for the board
int board[3][3] = {{0, 0, 0}, {0, 0, 0}, {0, 0, 0}};
// char array for the X and O placeholders
char symbols[2] = {'X', 'O'};
// whether game has been won
int win = 0;
// tracker for turn
int turn = 0;
// coordinates
int r = 0;
int c = 0;

// displays board 
void display(){
    for(int i = 0; i < 3; i++){
        for(int j = 0; j < 3; j++){
            if(!board[i][j]){
                cout << "[ ]";
            } else if(board[i][j] == 1){
                cout << "[X]";
            } else {
                cout << "[O]";
            }
        }
        cout << "\n";
    }
}
// checks for a win
void checkWin(){
    for(int i = 0; i < 3; i++){
        if(board[i][0] && board[i][0]==board[i][1] && board[i][0]==board[i][2]){
            win = 1;
            break;
        }
        if(board[0][i] && board[0][i]==board[1][i] && board[0][i]==board[2][i]){
            win = 1;
            break;
        }
    }
    if(board[0][0] && board[0][0]==board[1][1] && board[0][0]==board[2][2]){
        win = 1;
    }
    if(board[2][0] && board[2][0]==board[1][1] && board[2][0]==board[0][2]){
        win = 1;
    }
    if(win){
        cout << turn << " HAS WON THE GAME!\n";
    }
}
int main(){
    cout << "Welcome to tic-tac-toe!\n";
    
    while(!win){
        display();
        // prompt move
        cout << "It is currently " << symbols[turn] << "\'s turn\n";
        cout << "Please enter the row and column of the move (0-indexed):\n";
        cin >> r >> c;
        // check move
        if(r < 0 || r > 2 || c < 0 || c > 2 || board[r][c]){
            while(r < 0 || r > 2 || c < 0 || c > 2 || board[r][c]){
                cout << "Invalid move! Please try again.\n";
                cout << "It is currently " << symbols[turn] << "\'s turn\n";
                cout << "Please enter the row and column of the move (0-indexed):\n";
                cin >> r >> c;
            }
            board[r][c] = turn+1;
        } else {
            board[r][c] = turn+1;
        }
        checkWin();
        // update
        turn = !turn;        
    }
    // check win or tie
    if(win){
        display();
    } else {
        cout << "The game is a tie.\n";
    }
    
}
