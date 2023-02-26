#include <iostream>
#include <vector>
#include <cstdlib>
using namespace std;

bool checkRight (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + y > matrix[x].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y < matrix[y].size()){
        y = y + 1; 
        }
        
    }
    return true;
}


bool checkLeft (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + y > matrix[x].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y > 0){
        y = y - 1;
        }
        
    }
    return true;
}

bool checkDown (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + x > matrix[y].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(x < matrix[x].size()){
        x = x + 1;
        }
    }
    return true;
}

bool checkUp (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + x > matrix[y].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(x > 0){
        x = x - 1;
        }

    }
    
    return true;
}

bool checkRightUp (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + x > matrix[y].size() && strlen(word) + y > matrix[x].size()){
        return false;
    }

    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y < matrix[y].size() && x > 0){
        y = y + 1; 
        x = x - 1;
        }
        
    }
    return true;
}
bool checkLeftUp (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + y > matrix[x].size() && strlen(word) + x > matrix[y].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y > 0 && x > 0){
        y = y - 1;
        x = x - 1;
        }
        
    }
    return true;
}

bool checkRightDown (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + y > matrix[x].size() && strlen(word) + x > matrix[y].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y < matrix[y].size() && x < matrix[x].size() ){
        y = y + 1; 
        x = x + 1;
        }
        
    }
    return true;
}

bool checkLeftDown (vector< vector<char> > &matrix, char *word, int x, int y){

    if(strlen(word) + y > matrix[x].size() && strlen(word) + x > matrix[y].size()){
        return false;
    }
    
    for(int i = 0; i < strlen(word); i++){
        if(word[i] != matrix[x][y]){
            return false;
        }
        if(y > 0 && x < matrix[x].size()){
        y = y - 1;
        x = x + 1;
        }
    }
    return true;
}

int main(int argc, char *argv[]){
    
    int x, y;
    int c = 0;
    vector< vector<char> > matrix;
    vector< vector<bool> > grid;
    
    cin >> y;
    cin >> x;

    matrix.resize(x);
    for(int i = 0; i < x; i++){
        matrix[i].resize(y);
    }

    grid.resize(x);
    for(int i = 0; i < x; i++){
        grid[i].resize(y);
    }

    for(int i = 0; i < y; i++){
        for(int j = 0; j < x; j++){
            cin >> matrix[i][j];
        }
    }

    for(int i = 1; i < argc; i++){
        for(int j = 0; j < y; j++){
            for(int k = 0; k < x; k++){
                if(grid[j][k] == true){
                    continue;
                }
                else if (checkRight(matrix, argv[i], j, k) == true){
                    while(k + c < k + strlen(argv[i])){
                    grid[j][k+c] = true;
                    c++;
                    }
                }
                else if (checkLeft(matrix, argv[i], j, k) == true){
                    while(k + c < k + strlen(argv[i])){
                    grid[j][k-c] = true;
                    c++;
                    }
                }
                else if (checkDown(matrix, argv[i], j, k) == true){
                    while(j + c < j + strlen(argv[i])){
                    grid[j+c][k] = true;
                    c++;
                    }
                }
                else if (checkUp(matrix, argv[i], j, k) == true){
                    while(j + c < j + strlen(argv[i])){
                    grid[j-c][k] = true;
                    c++;
                    }
                }
                else if (checkRightUp(matrix, argv[i], j, k) == true){
                    while(j + c < j + strlen(argv[i]) && k + c < k + strlen(argv[i])){
                    grid[j - c][k + c] = true;
                    c++;
                    }
                }
                else if (checkLeftUp(matrix, argv[i], j, k) == true){
                    while(j + c < j + strlen(argv[i]) && k + c < k + strlen(argv[i])){
                    grid[j - c][k - c] = true;
                    c++;
                    }
                }
                else if (checkRightDown(matrix, argv[i], j, k) == true){
                    while(k + c < k + strlen(argv[i]) && j + c < j + strlen(argv[i])){
                    grid[j + c][k + c] = true;
                    c++;
                    }
                }
                else if (checkLeftDown(matrix, argv[i], j, k) == true){
                    while(k + c < k + strlen(argv[i]) && j + c < j + strlen(argv[i])){
                    grid[j + c][k - c] = true;
                    c++;
                    }
                }
                else{
                    grid[j][k] = false;
                }
                c = 0;
            }
        }
    }


        for(int j = 0; j < y; j++){
            for(int k = 0; k < x; k++){
                if(grid[j][k] == true){
                    cout << matrix[j][k] << " ";
                }
                else{
                    cout << "*" << " ";
                }
            }
            cout << endl;
        }

    return 0;
}

