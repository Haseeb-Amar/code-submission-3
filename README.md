# code-submission-3


#include <iostream>
#include <string>
#include <array>
#include <algorithm>
using namespace std;

void menue();

int main()
{
    menue();
    string tea[6] = { "1.Ice Tea = 3 dhs ", "2.Milk Tea = 2 dhs", "3.Black Tea = 1 dhs", "4.Ice Coffee = 3 dhs", "5.Milk Coffee = 2 dhs", "6.Black Coffee = 1 dhs" };

    for (int i = 0; i < 6; i++)
    {
        cout << tea[i] << endl;
    }
    cout << "\nABOVE IS OUR MENUE PLEASE SELECT WHAT YOU WILL LIKE TO HAVE\n";
    cout << "\nPLEASE ENTER THE ITEM NO:";

    int order;
    cin >> order;

    while (cin.fail())
    {
        cin.clear();
        cin.ignore(1000, '\n');
        cout << "ENTER VALID NO:";
        cin >> order;

    }
   
    char sugar;
    cout << "\nPLEASE ENTER IF YOU WANT SUGAR\n ";
    cout << "\nPLEASE ENTER Y if yes and N or any other key if no: ";
    cin >>sugar ;
  
    switch (sugar)
    {
    case 'y':
    case 'Y':
    {
        cout << "sugar will be included.\n";
        break;
    }
    case 'n':
    case 'N':
    {
        cout << "sugar will not be included.\n";
        break;
    }
    default:
    {
        cout << "sugar will not be included. \n ";
    }
    }

    int quantity;
    int ICECOFFEE = 3;
    int totalamaountoficecoffee = 0;
    int MILKCOFFEE = 2;
    int totalamountofmilkcoffee = 0;
    int BLACKCOFFEE = 1;
    int totalamountofblackcoffee = 0;
    int ICETEA = 3;
    int totalamountoficetea = 0;
    int MILKTEA = 2;
    int totalamountofmilktea = 0;
    int BLACKTEA = 1;
    int totalamaountofblacktea = 0;
    int money;
    float total = 0;
    cout << "How many do you want?:";
    cin >> quantity;
    
    switch (order)
    {
    case 1:
        cout << " icetea AED 3 x " << quantity << "=" << quantity * ICECOFFEE << "\n";
        totalamaountoficecoffee = quantity * ICECOFFEE;
        break;

    case 2:
        cout << "milktea AED 2 x " << quantity << " = " << quantity * MILKCOFFEE << "\n";
        totalamountofmilkcoffee = quantity * MILKCOFFEE;
        break;

    case 3:
        cout << "blacktea AED 1 x " << quantity << " = " << quantity * BLACKCOFFEE << "\n";
        totalamountofblackcoffee = quantity * BLACKCOFFEE;
        break;
    case 4:
        cout << "icecoffee AED 3 x " << quantity << " = " << quantity * ICETEA << "\n";
        totalamountoficetea = quantity * ICETEA;
        break;

    case 5:
        cout << "milkcoffee AED 2 x " << quantity << " = " << quantity * MILKTEA << "\n";
        totalamountofmilktea = quantity * MILKTEA;
        break;

    case 6:
        cout << "blackcoffee AED 1 x " << quantity << " = " << quantity * BLACKTEA << "\n";
        totalamaountofblacktea = quantity * BLACKTEA;
        break;
    }
 

    total = 0;
    total = total + totalamaountoficecoffee + totalamountofmilkcoffee + totalamountofblackcoffee + totalamountoficetea + totalamountofmilktea + totalamaountofblacktea;

    cout << "Total Amount is:" << total << "\n";
    cout << "cash:";
    cin >> money;
    cout << "change:" << money - total << "\n";
    cout << "\nTHANKYOU VISIT AGAIN!\n";
  
  
    return 0;

}

void menue()
{
    cout << "-----MENUE-----\n";
}


