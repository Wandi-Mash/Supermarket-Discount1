//Calculates the income tax
#include <iostream>
#include <string>
using namespace std;

int main( ) 
{
    const float STANDARD_DISCOUNT = 10; //Standard disvount = 10%
          float price,
                managerDiscount, //Special discount issued by manager
                discount,
                totalDiscount;
                
          
    cout << "Enter the price of the item: ";
    cin >> price;
    
    if (price >= 200) 
        {cout << "Call store manager for discount!" << endl;
        cout << "Store manager discount: ";
        cin >> managerDiscount;
        discount = managerDiscount;
        }
        
    else 
    {discount = STANDARD_DISCOUNT;}
        
        
        
    totalDiscount = price - (price * (discount/100));
    cout.precision(2);
    cout.setf(ios::fixed);
    cout << "Was: " << price << endl;
    cout.precision(0);
    cout << "Discount: " << discount << "%" << endl;
    cout.precision(2);
    cout << "Now: " << totalDiscount << endl; 
return 0;
}
