# 第一次作业
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


	
<!--stackedit_data:
eyJoaXN0b3J5IjpbMTQyMzA2NjY2Nyw4NjI4NDUyNzYsMTM1Mj
E2NDU5NV19
-->