# Code Forces
# No of solve: 1
# Screenshot:
<img width="895" alt="Image" src="https://github.com/user-attachments/assets/82731edf-291b-4e6a-899e-91bff2af4778" />

# Experiment Number: 05
# Experiment Name: Checking a Date is valid or invalid
# Submission Date: 24/05/2025
## Code :
```C++
#include <iostream>
#include <vector>
#include <string>
#include <algorithm>
#include <set>
#include <cmath>

using namespace std;

class Date
{
private:
    int date, month, year;

public:
    Date(int date, int month, int year)
    {
        this->date = date;
        this->month = month;
        this->year = year;
    }
    int getDate()
    {
        return date;
    }
    int getMonth()
    {
        return month;
    }
    int getYear()
    {
        return year;
    }
};

int main()
{
    int a, b, c;
    cout << "Input date,month,year:";
    cin >> a >> b >> c;
    Date d1(a, b, c);
    int d = d1.getDate();
    int e = d1.getMonth();
    int f = d1.getYear();
    int arr[] = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
    if ((f % 4 == 0) && ((f % 100 != 0) || (f % 400 == 0)))
    {
        arr[1] = 29;
    }
    if (arr[e - 1] >= d)
    {
        cout << "The date is correct" << endl;
    }
    else
    {
        cout << "The date is incorrect" << endl;
    }

    return 0;
}
```
# Output (Screenshot):
<img width="988" alt="Image" src="https://github.com/user-attachments/assets/cc32f4be-f5d3-44d9-8c04-32e48387b047" />
