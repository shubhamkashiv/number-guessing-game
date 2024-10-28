#number-guessing-game
build number guessing game using c++
/*create a program that generates a random number and asks the user to guess
 it. provide feedback on whether the guess is too high or low until the user
 guesses the correct number.*/
 #include<iostream>
 #include<cstdlib>
 #include<ctime>
 using namespace std;
 int main()
 {        
          int inputuser;
          char moves;
          cout<<"------------NUMBER GUESSING GAME-----------"<<endl;
          
          do{
                    srand(time(0));
                    int random=rand()%100+20;
                    cout<<"enter number in between range 1 to 100:      ";
                    cin>>inputuser;
                    cout<<endl;
                    if(inputuser==random){
                    cout<<"your guess is too high"<<endl;
                    }
                    else{
                    cout<<"your guess is too low"<<endl;
                    }
                    cout<<"would you like to try again YES/NO:     ";
                    cin>>moves;
                    cout<<endl;

          }
          while(moves!='NO');
          cout<<"game end"<<endl;
          return 0;
}
