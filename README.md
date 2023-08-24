# LAB1
 Lab1 COMSC-165 Advanced C/C++ Programming
#include <iostream>
using std::cin;
using std::cout;
using std::ios;

#include <fstream>
using std::ofstream;
using std::ifstream;

#include <string>
using std::string;
using std::getline;



/*********************************************************************
* Name: Amber Fisk
* Lab 1:Console Programming Basics
* Editor(s) used: Notepad ++
* Compiler(s) used: Microsoft Visual Studio
* Description: Seemingly simple "console program".
* This program reads and outputs two sets of inputs, including two calculated values in the output.
**********************************************************************/;

// Declaring function prototypes
void print_id(string lab_desc);


/*********************************************************************
* Function: Main
**********************************************************************/;

int main() {
	int age;
	string name, city;
	double fahrenheit, celsius;	
	string buf;// example from "how2ignore.cpp"



	cout << "Enter your age:";	
	cin >> buf;	
	age = atoi(buf.c_str());//set to 0 
	cin.ignore(200,'\n');	//to skip the rest of the input line
	
	cout << "Enter your name:";
	getline(cin, name);//to read multiple words

	cout << "Enter the temperature outside right now (degress F):";
	cin >> buf;	
	fahrenheit = atol(buf.c_str());
	cin.ignore(200, '\n');	
	cout.setf(ios::fixed);
	cout.precision(2);

	cout << "What city are you in? :";
	getline(cin, city);


	celsius = (fahrenheit - 32) * (5.0 / 9.0);// Fahrenheit to Celsius conversion 
	
	cout << name << " is " << age << " and will be " << age + 2 << " two years from now." << std::endl;
	cout << "Its " << fahrenheit << " degrees F in " << city << "-- thats "<<celsius<<" degress C" << std::endl << std::endl;


	print_id("lab1");
	
	
}

void print_id(string lab_desc) {
	cout << "Amber Fisk\n";
	cout << lab_desc;
	cout << "Editor(s) used:Notepad ++\n";
	cout << "Compiler(s) used:Microsoft Visual Studio\n";
	cout << "File: " << __FILE__ << "\n";
	cout << "Compiled: " << __DATE__ << " at " << __TIME__ << "\n\n";
}








