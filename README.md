#include <iostream>
using namespace std;

// Function to ask questions
int askQuestion(string question, string options[], char correctAnswer) {
    char answer;
    
    cout << "\n" << question << endl;
    for(int i = 0; i < 4; i++) {
        cout << options[i] << endl;
    }
    
    cout << "Enter your answer (A/B/C/D): ";
    cin >> answer;

    if(toupper(answer) == correctAnswer) {
        cout << "Correct!\n";
        return 1;
    } else {
        cout << "Wrong! Correct answer is " << correctAnswer << endl;
        return 0;
    }
}

int main() {
    int score = 0;

    // Question 1
    string q1 = "1. What is the capital of India?";
    string opt1[] = {"A. Mumbai", "B. Delhi", "C. Kolkata", "D. Chennai"};
    score += askQuestion(q1, opt1, 'B');

    // Question 2
    string q2 = "2. Which language is used for system programming?";
    string opt2[] = {"A. Python", "B. Java", "C. C++", "D. HTML"};
    score += askQuestion(q2, opt2, 'C');

    // Question 3
    string q3 = "3. What is 2 + 2?";
    string opt3[] = {"A. 3", "B. 4", "C. 5", "D. 6"};
    score += askQuestion(q3, opt3, 'B');

    // Question 4
    string q4 = "4. Who invented C++?";
    string opt4[] = {"A. Dennis Ritchie", "B. Bjarne Stroustrup", "C. James Gosling", "D. Elon Musk"};
    score += askQuestion(q4, opt4, 'B');

    // Question 5
    string q5 = "5. Which is an input device?";
    string opt5[] = {"A. Monitor", "B. Printer", "C. Keyboard", "D. Speaker"};
    score += askQuestion(q5, opt5, 'C');

    // Final Score
    cout << "\n🎉 Quiz Completed!" << endl;
    cout << "Your Score: " << score << "/5" << endl;

    return 0;
}
