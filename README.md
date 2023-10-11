#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main()
{

    srand(time(0));

    int lowerBound = 1;
    int upperBound = 100;
    int numberToGuess = rand() % (upperBound - lowerBound + 1) + lowerBound;
    int numberOfTries = 0;
    int guess;

    cout << "Welcome to the Number Guessing Game!" << endl;
    cout << "I've selected a number between " << lowerBound << " and " << upperBound << ". Try to guess it!" << endl;

    do
    {
        cout << "Enter your guess: ";
        cin >> guess;
        numberOfTries++;

        if (guess < numberToGuess)
        {
            cout << "Too low! Try again." << endl;
        }
        else if (guess > numberToGuess)
        {
            cout << "Too high! Try again." << endl;
        }
        else
        {
            cout << "Congratulations! You've guessed the number in " << numberOfTries << " tries." << endl;
        }
    } while (guess != numberToGuess);

    return 0;
}
