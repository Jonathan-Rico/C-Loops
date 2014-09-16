// project4.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include <iostream>
#include <string>
using namespace std;

int _tmain(int argc, _TCHAR* argv[])
{
	int x;
	int total = 0;
	for (int L=0; L<5; L++){
		
			string name;
			cout<<"Enter the Student's First Name.\n";
			cin>>name;
			string name2;
			cout<<"Enter the Student's Last Name.\n";
			cin >> name2;
			cout << "Enter "<< name<< " " <<name2 <<"'s Grade 0 - 100\n";
			cin>> x;
			string z;
			int grade=x;

		do {

			if(x>=0 && x<60) {
				z = "F";
					cout << name<< " "  << name2 << " has failed with a grade of " <<grade<< " percent.\n";
					cout << name<< " "  << name2 <<" will receive a " << z << " for the course.\n";
					cout << name<< " "  << name2 << " must repeat the course.\n\n";
			}
			if(x>59 && x<70) {
				z= "D";
				cout << name<< " "  << name2 << " has passed with a grade of " << grade << " percent.\n";
				cout << name<< " "  << name2  << " will receive a " << z << " for the course.\n\n";
			}
			if(x>69 && x<80) {
				z= "C";
				cout << name<< " "  << name2  << " has passed with a grade of " << grade << " percent.\n";
				cout << name<< " "  << name2  << " will receive a " << z << " for the course.\n\n";
			}
			if(x>79 && x<90) {
				z= "B";
				cout << name<< " "  << name2  << " has passed with a grade of " << grade << " percent.\n";
				cout << name<< " "  << name2  << " will receive a " << z << " for the course.\n\n";
			}
			if(x>89 && x<=100) {
				z= "A";
				cout << name<< " "  << name2  << " has passed with a grade of " << grade << " percent.\n";
				cout << name<< " "  << name2  << " will receive an " << z << " for the course.\n\n";
			}
			if(x<0) {
				cout<< grade << name2 <<" is not within the bounds specified.\n\n";
			}
			if(x>101) {
				cout<< grade << name2 <<" is not within the bounds specified.\n\n";
			}

			total = total + grade;
		
		}while(x<=-1 || x>101);	
	}
	int avg = total/5;
	cout << "Average class grade = " << avg << "\n";
}
