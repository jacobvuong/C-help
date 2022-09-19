printTitle()
{
	cout <<"-----------------------" << endl;
	cout <<"Enter your letter grade: " << endl;
	cout <<"Grade value is [" << "]" << endl;

}
string getInput()
{
	cout << "Enter your letter grade: ";
	string letter;
	cin >> letter;
	return letter;

}
double letterToPoints(stringIn letterGrade)
{
	double result;
	if(letterGrade == "A")
	{
		result = 4.0;
		return result;
	}
	else if(letterGrade == "A-")
	{
		return 4.0 - 0.3;
	}
	else if(letterGrade == "B")
	{
		return 3.0;
	}
	else if(letterGrade == "B-")
	{
		return 3.0 - 0.3;
	}
	else if(letterGrade == "B+")
	{
		return 3.0 + 0.3;
	}
	else if(letterGrade == "C")
	{
		return 2.0;
	}
	else if(letterGrade == "C-")
	{
		return 2.0 - 0.3;
	}
	else if(letterGrade == "C+")
	{
		return 2.0 + 0.3;
	}
	else if(letterGrade == "D")
	{
		return 1.0;
	}
	else if(letterGrade == "D+")
	{
		return 1.0 + 0.3;
	}
	else if(letterGrade == "D-")
	{
		return 1.0 - 0.3;
	}
	else if(letterGrade == "F")
	{
		return 0.0;
	}
	else if(letterGrade == "A+" || letterGrade == "F+" ||
	letterGrade == "F-")
	{
		return INVALID_COMBINATION;
	}
	else
	{
		return INVALID_INPUT;
	}
}
void printReport(double points)
{
	cout << "Grade value is [";
	if(points >= 0.0)
	{
		cout << points;
	}
	else if (points == INVALID_COMBINATION)
	{
		cout << "Invalid combination";
	}
	else
	{
		cout << "Invalid input";
	}
	cout << "]/n";
}
