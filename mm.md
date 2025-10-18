# 第一次作业
* 第一项:斐波那契额数列（太菜了只会这样写，其他功能实现不了）
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
* 第二项:排序
1. 选择排序
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
	for (int i = 0; i < n; i++) {//进行赋值
	    arr[i] = rand() % 100;
		cout  << arr[i] << " ";
	
	}
	cout <<"这是之前的数列" << endl;

	for (int f = 0; f < n ; f++) {
		int p = f;
		for (int j = f + 1; j < n; j++) {
			if (arr[p] > arr[j]) {
				p = j;
			}
		}
			int t = arr[f];
			arr[f] = arr[p];
			arr[p] = t;
			cout << arr[f] << " ";
		
	}
	cout << "这是之后的数列" << endl;

	
	system("pause");
	return 0;
}
````
2. 冒泡排序
```

<!--stackedit_data:
eyJoaXN0b3J5IjpbLTQxNTE3NTQ5MCw3MjQwOTY5NzldfQ==
-->