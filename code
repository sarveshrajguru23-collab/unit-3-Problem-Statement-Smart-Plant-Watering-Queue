
#include <iostream>
#include <string>
#include <limits>
using namespace std;

#define MAX 10

struct Plant {
    string name;
    int moisture;
};

Plant plants[MAX];
int front = 0, rear = -1;

// Add a plant
void enqueue() {
    if (rear == MAX - 1) {
        cout << "Queue is full!\n";
        return;
    }

    Plant p;

    cout << "Enter plant name: ";
    getline(cin >> ws, p.name);

    cout << "Enter soil moisture (0-100): ";
    if (!(cin >> p.moisture)) {
        cout << "Invalid input! Enter a number.\n";
        cin.clear();
        cin.ignore(numeric_limits<streamsize>::max(), '\n');
        return;
    }

    if (p.moisture < 0 || p.moisture > 100) {
        cout << "Invalid moisture value!\n";
        return;
    }

    if (p.moisture >= 40) {
        cout << "Sufficient moisture. No watering needed.\n";
        return;
    }

    plants[++rear] = p;
    cout << p.name << " added to the watering queue.\n";
}

// Water the next plant
void dequeue() {
    if (front > rear) {
        cout << "No plants are waiting for watering.\n";
        return;
    }

    cout << "Watering plant: " << plants[front].name << endl;
    cout << "Moisture before watering: "
         << plants[front].moisture << "%\n";
    cout << "Watering completed!\n";

    front++;

    if (front > rear) {
        front = 0;
        rear = -1;
    }
}

// Display pending plants
void display() {
    if (front > rear) {
        cout << "Watering queue is empty.\n";
        return;
    }

    cout << "\n--- Pending Watering Queue ---\n";

    for (int i = front; i <= rear; i++) {
        cout << "Plant: " << plants[i].name
             << " | Moisture: " << plants[i].moisture
             << "%\n";
    }
}

// Show next plant
void peek() {
    if (front > rear) {
        cout << "No plant is waiting for watering.\n";
        return;
    }

    cout << "Next plant to water: "
         << plants[front].name << endl;
}

int main() {
    int choice;

    do {
        cout << "\n===== SMART PLANT WATERING QUEUE =====\n";
        cout << "1. Add Plant\n";
        cout << "2. Water Next Plant\n";
        cout << "3. Display Pending Plants\n";
        cout << "4. Show Next Plant\n";
        cout << "5. Exit\n";
        cout << "Enter your choice: ";

        if (!(cin >> choice)) {
            cout << "Invalid input! Enter a number from 1 to 5.\n";
            cin.clear();
            cin.ignore(numeric_limits<streamsize>::max(), '\n');
            continue;
        }

        switch (choice) {
            case 1: enqueue(); break;
            case 2: dequeue(); break;
            case 3: display(); break;
            case 4: peek(); break;
            case 5: cout << "Exiting Smart Plant Watering Queue.\n"; break;
            default: cout << "Invalid choice! Try again.\n";
        }

    } while (choice != 5);

    return 0;
}
