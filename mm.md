# 第一次作业
* 第一项
```c++
#include<iostream>
using namespace std;
#include<ctime>

	int main() {
		int n = 0, An[100] = { 0 };
		cout << "请输入n的值" << endl;
		cin >> n;
		An[0] = 0;
		An[1] = 1;
		for (int i = 2; i < n; i++) {
			An[i] = An[i - 1] + An[i - 2];
		}
		for (int j = 0; j < n; j++) {
			cout << An[j] << " " ;

		}
		cout << "这是第n项"<<An[n-1]<<endl;
			
	
	

	
	system("pause");
	return 0;}
	
```
* 第二项
```c++
#include<iostream>
using namespace std;
#include<ctime>
const int N = 100;
int main() {
	cout << "请输入n的值:" << endl;
	srand((unsigned int)time(NULL));
	int n = 0;
	cin >> n;
	
	int arr[N] = { 0 };
	for (int i = 0; i < n; i++) {
	    arr[i] = rand() % 100;
		

	
	}
	for (int f = 0; f < n - 1; f++) {
		int p = f;
		for (int j = f + 1; j < n; j++) {
			if (arr[p] > arr[j]) {
				p = j;
			}
		}
			int t = arr[f];
			arr[f] = arr[p];
			arr[p] = t;
			cout << arr[p] << " ";
		
	}

	
	system("pause");
	return 0;
}


	
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzI0MDk2OTc5LDM2NjI3NzY5NywxNDIzMD
Y2NjY3LDg2Mjg0NTI3NiwxMzUyMTY0NTk1XX0=
-->