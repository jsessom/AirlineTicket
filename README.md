# AirlineTicket
AirFare
#include <iostream>
#include <math.h>
#include <string>
#include <iomanip>

using namespace std;

int main()
{
	const double kPriceForHawaii = 199.99;
	const double kPriceForBahamas = 201.11;
	const double kPriceForCancun = 250.50;
	const double kPriceForLasVegas = 150.75;
	const double kPriceForEurope = 600.15;

	//.. do for the remaining destination

	const double kPriceForDelta = 200.99;
	const double kPriceForSouthwest = 150.99;
	const double kPriceForContinental = 250.50;
	const double kPriceForAmerican = 275.45;
	const double kPriceForUsAir = 199.99;




	int option;
	string destination, airline;
	double price, pricetotal;
	bool isRoundTrip = false;
	int numberOfPassengers, numberOfUnderage;

	cout << "Please choose your destination\n";
	cout << "1. Hawaii\n";
	cout << "2. Bahamas \n";
	cout << "3. Cancun \n";
	cout << "4. Las Vegas \n";
	cout << "5. Europe \n";

	// Ask for destination
	cin >> option;

	if (option == 1)
	{// for hawaii
		price = kPriceForHawaii;
		destination = "Hawaii";
	}

	else if (option == 2)
	{ // for bahamas
		price = kPriceForBahamas;
		destination = "Bahamas";
	} // do for remaining destination 


	else if (option == 3)
	{ // for Cancun
		price = kPriceForCancun;
		destination = "Cancun";
	} // do for remaining destination 


	else if (option == 4)
	{ // for bahamas
		price = kPriceForLasVegas;
		destination = "Las Vegas";
	} // do for remaining destination 

	else if (option == 5)
	{ // for bahamas
		price = kPriceForEurope;
		destination = "Europe";
	} // do for remaining destination 

	else
	{ // for bahamas

		destination = "You have selected the wrong option. Please contact our direct number for assistance (832-799-4828).\n";
	} // do for remaining destination 








	double TicketCost;

	cout << "Choose an airline\n";
	cout << "1. Delta\n";
	cout << "2. SouthWest \n";
	cout << "3. Us Air \n";
	cout << "4. Continental \n";
	cout << "5. American \n";

	// Ask for airline
	cin >> option;

	if (option == 1)
	{ // for Delta
		TicketCost = price + kPriceForDelta;
		airline = "Delta";
	}
	else if (option == 2)
	{ // for Southwest
		TicketCost = price + kPriceForSouthwest; // same as price = price + kPriceForSouthwest;
		airline = "Southwest";
	} // do for remaining airlines 


	else if (option == 3)
	{
		TicketCost = price + kPriceForUsAir;
		airline = "Us Air";
	}


	else if (option == 4)
	{
		TicketCost = price + kPriceForContinental;
		airline = "Continental";
	}


	else if (option == 5)
	{
		TicketCost = price + kPriceForAmerican;
		airline = "American";
	}


	else
	{ // for Southwest
		airline = "You have selected the wrong option. Please contact our direct number for assistance (832-799-4828).\n";
	} // do for remaining airlines 




	double RoundTripCost;
	// Ask for rountrip information
	cout << "Is this a round trip? 1 for yes, 2 for no\n";
	cin >> option;

	if (option == 1)
	{
		isRoundTrip = true;
		RoundTripCost = TicketCost * 2;
	}


	double PassCost;

	cout << "Enter number of passengers: ";
	cin >> numberOfPassengers;

	switch (numberOfPassengers)
	{
	case 1:
		PassCost = RoundTripCost * 1;
	
		break;
	case 2: PassCost = RoundTripCost * 2;
		break;
	case 3: PassCost = RoundTripCost * 3;
		break;
	case 4: PassCost = RoundTripCost * 4;
		break;
	case 5: PassCost = RoundTripCost * 5;
		break;

	default: cout << "You have selected the wrong option. Please contact our direct number for assistance (832-799-4828).\n";

	}



	double TotalCost;
	// Ask for underage
	cout << "How many passengers are under 18 \n";
	cin >> numberOfUnderage;

	// calculate the discount 
	double discount = PassCost * numberOfUnderage * 0.25;
	TotalCost = PassCost - discount;


	cout << "Your trip to " << destination << " flying with " << airline <<
		" with " << numberOfPassengers << " passenger(s) and  " << numberOfUnderage << " passengers under 18 will = " << TotalCost << endl; // finish the rest 




	system("pause");

	return 0;
}
