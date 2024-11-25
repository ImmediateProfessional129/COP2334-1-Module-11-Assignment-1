# COP2334-1-Module-11-Assignment-1
This is a repository link of the COP2334-1 Module 11 Assignment Program 1

// This program is designed to caluclate the amount of items in the inventory of a furniture store such as a chair, table, and so on. Plus, it will calculate the total price of the items.

// Include the header file.
#include <iostream>
#include <string> // Include the string library.
using namespace std; // Using standard namespace.

class Item { // Create a class called Item.
private: // Private variables.
    string itemName; // Declare a string variable called itemName.
    int itemID; // Declare an integer variable called itemID.
    int quantity; // Declare an integer variable called quantity.
    double price; // Declare a double variable called price.
public: // Public variables.
    Item(string name, int id, int qty, double p) { // Create a constructor that takes in four parameters.
        itemName = name; // Set the itemName variable to the name parameter.
        itemID = id; // Set the itemID variable to the id parameter.
        quantity = qty; // Set the quantity variable to the qty parameter.
        price = p; // Set the price variable to the p parameter.
    }
    void addStock(int qty) { // Create a function called addStock that takes in an integer parameter.
        quantity += qty; // Add the quantity variable to the qty parameter.
    }
    void sellItem(int qty) { // Create a function called sellItem that takes in an integer parameter.
        if (quantity >= qty) { // If the quantity variable is greater than or equal to the qty parameter.
            quantity -= qty; // Subtract the quantity variable from the qty parameter.
        }
    }
    double getTotalValue() { // Create a function called getTotalValue.
        return quantity * price; // Return the quantity variable multiplied by the price variable.
    } 
    void display() { // Create a function called display.
        cout << "Item Details:" << endl; // Print "Item Details:" to the console.
        cout << "Item Name: " << itemName << endl; // Print "Item Name: " followed by the itemName variable to the console.
        cout << "Item ID: " << itemID << endl; // Print "Item ID: " followed by the itemID variable to the console.
        cout << "Quantity: " << quantity << endl; // Print "Quantity: " followed by the quantity variable to the console.
        cout << "Price: $" << price << endl; // Print "Price: $" followed by the price variable to the console.
        cout << "Total Value: $" << getTotalValue() << endl; // Print "Total Value: $" followed by the getTotalValue function to the console.
    }
}; // End of the Item class.

int main() { // Create the main function.
    Item item1("Coffee Table", 967, 13, 300.00); // Create an object called item1 with the Item constructor.
    Item item2("Couch", 876, 22, 500.00); // Create an object called item2 with the Item constructor.
    Item item3("Patio Awning", 765, 10, 700.00); // Create an object called item3 with the Item constructor.
    item1.display(); // Call the display function for item1.
    cout << endl; // Print a newline to the console.
    cout << "After Adding Stock:" << endl; // Print "After Adding Stock:" to the console.
    item1.addStock(22); // Call the addStock function for item1 with an argument of 22.
    item1.display(); // Call the display function for item1.
    cout << endl; // Print a newline to the console.
    cout << "After Selling:" << endl; // Print "After Selling:" to the console.
    item1.sellItem(10); // Call the sellItem function for item1 with an argument of 10.
    item1.display(); // Call the display function for item1.
    cout << endl; // Print a newline to the console.
    item2.display(); // Call the display function for item2.
    cout << endl; // Print a newline to the console.
    item3.display(); // Call the display function for item3.
    cout << endl; // Print a newline to the console.
    return 0; // Return 0 to the operating system.
} // End of the main function execution.
