# Roderisk
#include <iostream>
using namespace std;
void bubblesore(int * arr, int len)//引入*arr是为了使用地址传递从而修饰实参，如果引入为arr则无法影响实参的输出
{
	for (int i = 0; i < len; i++)
	{
		for (int j = 0; j < len - 1; j++)
		{
			if (arr[j] > arr[j+1])
			{
				int temp = arr[j];
				arr[j] = arr[j+1];
				arr[j+1] = temp;
			}
		}
	}
}
void printsore(int* arr,int len)
{
	for (int i = 0; i < 10; i++)
	{
		cout << arr[i] << endl;
	}
}
int main() 
{
	int arr[10] = { 8,5,6,1,3,4,2,7,9,10 };
	int len = sizeof(arr) / sizeof(arr[0]);
	bubblesore(arr, len);
	printsore(arr, len);
	system("pause");
	return 0;
}
