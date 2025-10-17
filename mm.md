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
		cout<" << An[j] << " " ;

	}
	system("pause");
	return0
	}
	
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTY5MDY3OTAyNCwxMzUyMTY0NTk1XX0=
-->