# Write program that gets the following information from the user:  The subtotal of the restaurant bill The sales tax rate The desired tip rate The number of people in the party The program will then calculate the grand total and divide it by the number of people to let each person know what they owe on the bill. It will use the formula: 1 patron’s payment = (subtotal + subtotal * tax rate + subtotal * tip rate) / number of patrons Equivalently, this can be written as: 1 patron’s payment = (subtotal * (1 + tax rate + tip rate)) / number of patrons  Make sure to round up in the final answer to the nearest cent.

#include <iostream>
#include <cmath>

using namespace std;

int main() {
	float subTotal; // Subtotal of the restaurant bill 
	float taxRate;    // Sales tax rate 
	float tipRate;  // Desired tip rate 
	float numPeople;   // Number of people in the party
	float patronPayment1;

	cout << " Enter the sub total: ";
	cin >> subTotal;

	cout << " Enter the sales tax rate: ";
	cin >> taxRate;
	taxRate = taxRate / 100.0;

	cout << " Enter the desired tip rate: ";
	cin >> tipRate;
	tipRate = tipRate / 100.0;


	cout << " Enter the number of people in the party: ";
	cin >> numPeople;

	patronPayment1 = (subTotal * (1 + taxRate + tipRate)) / numPeople; // What each person owes

	float roundedpatronPayment1 = ceil(patronPayment1 * 100) / 100;
	
	cout << " Each person owes: $" << roundedpatronPayment1 << endl;


	return 0;
}
