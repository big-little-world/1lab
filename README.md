# 1lab
// laba_tech_number_1.cpp: определяет точку входа для консольного приложения.


#include "stdafx.h"
#include <iostream>
#include <conio.h>
using namespace std;

/** @function Функция main
*/
int main()
{
	int size;
	cin >> size;
	int *a = new int[size];

	for (int i = 0; i < size; i++)
	{
		cin >> a[i];
	}
	for (int i = 0; i < size; i++)
	{
		for (int j = size - 1; j > i; j--)
		{
			if (a[j] < a[j - 1])
			{
				swap(a[j], a[j - 1]);
			}
		}
	}
	for (int i = 0; i < size; i++)
	{
		cout << a[i] << ' ';
	}
	_getch();
	return 0;
}
