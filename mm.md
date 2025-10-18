# 第一次作业
本文使用cpp
* 第一项:斐波那契数列（太菜了只会这样写，其他功能实现不了）
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
```c++
#include<iostream>
using namespace std;
#include<ctime>
int main() {
	int n = 0;
	cout << "请您输入n的值(n<99)" << endl;
	cin >>n;
	cout << "未排序之前的顺序:";
	int arr[100] = { 0 };
	srand((unsigned int)time(NULL));
	for (int i = 0; i < n; i++) {//for循环给数组赋值
		arr[i] = rand() % 100;
		cout << arr[i] << " ";
	}
	cout << endl;
	cout << "这是排序过的顺序:";
	for (int j = 0; j < n; j++) {
		for (int f = 0; f<n - j - 1; f++) {
			if (arr[f] >arr[f + 1]) {
				int temp = arr[f];
				arr[f] = arr[f + 1];
				arr[f+ 1] = temp;
			}
		}
	}
	for (int i = 0; i < n; i++) {
		cout << arr[i] << " ";
	}
	cout << endl;
	system("pause");
	return 0;
}


```
本小登太菜了只能写成这样，还借助了豆包检查错误和接受了一位学长的济助后面的拔高题太简单了就不做了哈  ：（
>q其实是我试了一下发现用switch写出来的语句不知道咋运行不了，问豆包也没搞好，mi'zhan'yi
<!--stackedit_data:
eyJoaXN0b3J5IjpbLTUyODMxNDM1MCw2MzU5MDYwMTRdfQ==
-->