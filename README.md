# tiktoe-game

#include <iostream>
#include <cstdlib>
#include <ctime>

using namespace std;

int main() {
    // Seed the random number generator
    srand(time(0));

    // Generate a random number between 1 and 100
    int secretNumber = rand() % 100 + 1;

    int guess;
    int attempts = 0;

    cout << "Welcome to the Number Guessing Game!" << endl;

    do {
        // Ask the user for a guess
        cout << "Enter your guess (between 1 and 100): ";
        cin >> guess;

        // Increment the number of attempts
        attempts++;

        // Check if the guess is too high, too low, or correct
        if (guess > secretNumber) {
            cout << "Too high! Try again." << endl;
        } else if (guess < secretNumber) {
            cout << "Too low! Try again." << endl;
        } else {
            cout << "Congratulations! You guessed the correct number in " << attempts << " attempts." << endl;
        }

    } while (guess != secretNumber);

    return 0;
}

