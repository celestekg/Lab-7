# Lab-7: This program allows the user to enter two numbers. The program then switches the two numbers using a swap function. The original two values, along with the swapped values, are then printed.

#include <iostream>
#include <string>

using namespace std;

void Read(double& a, double& b);
void Print(double a, double b);
void Swap(double& a, double& b);

int main()
{
	double a;
	double b;

	Read(a, b);

	while (a != 0)
	{
		Print(a, b);

		Swap(a, b);

		Print(a, b);

		Read(a, b);
	}

	cout << endl;
	return 0;
}

void Read(double& a, double& b)
{
	cout << "Enter the first value:  ";
	cin >> a;

	cout << "Enter the second value: ";
	cin >> b;
}

void Print(double a, double b)
{
	cout << endl;
	cout << "The first value is: " << a << endl;
	cout << "The second value is: " << b << endl;
	cout << endl;
}

void Swap(double& a, double& b)
{
	double temp = a;
	a = b;
	b = temp;
}
