#include <iostream>
#include <cmath>
using namespace std;

double stdev(double x[], int n)
{
    double sum = 0, mean, variance = 0;

    for(int i = 0; i < n; i++)
    {
        sum += x[i];
    }

    mean = sum / n;

    for(int i = 0; i < n; i++)
    {
        variance += pow(x[i] - mean, 2);
    }

    variance = variance / n;

    return sqrt(variance);
}

int main()
{
    int n;

    cout << "Enter number of elements: ";
    cin >> n;

    double arr[n];

    cout << "Enter elements:\n";
    for(int i = 0; i < n; i++)
    {
        cin >> arr[i];
    }

    cout << "Standard Deviation is: " << stdev(arr, n);

    return 0;
}
