# 第一次作业
```c++
#include<iostream>
using namespace std;
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
		cout<<"这是斐波那契数列“ << An[j] << " " ;
        cout<<"这是第n项<<An[n-1]<<endl;
	}
	system("pause");
	return0
	}
	
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTgyNzQ5MzQ2NCwxMzUyMTY0NTk1XX0=
-->