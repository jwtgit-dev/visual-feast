```cpp
#include <iostream>
#include <cstring>
#include <cmath>
using namespace std;
class Fraction {
private:
	int fenzi, fenmu;
	int god(int a, int b);
public:
	Fraction() :fenzi(0), fenmu(1) {};
	void set(int a, int b) {
		if (b < 0) {
			a = -a;
			b = -b;
		}
		int t = god(abs(a),abs(b));
		fenzi = a / t;
		fenmu = b / t;

	}
	friend istream& operator>>(istream& in, Fraction& f);
	friend ostream& operator<<(ostream& out, Fraction& f);
	bool operator>(Fraction & t) {
		if (fenzi * t.fenmu > t.fenzi * fenmu) {
			return true;
		}
		else {
			return false;
		}
	}
	Fraction operator +(const Fraction& t) {
		int a, b;
		a = fenzi * t.fenmu + t.fenzi * fenmu;
		b = fenmu * t.fenmu;
		Fraction f;
		f.set(a, b);
		return f;
	}
	Fraction operator -(const Fraction& t) {
		int a, b;
		a = fenzi * t.fenmu - t.fenzi * fenmu;
		b = fenmu * t.fenmu;
		Fraction f;
		f.set(a, b);
		return f;

	}
	Fraction operator *(const Fraction& t) {
		int a, b;
		a = fenzi * t.fenzi;
		b = fenmu * t.fenmu;
		Fraction f;
		f.set(a, b);
		return f;
	}
};
int Fraction::god(int a, int b) {
	int t;
	while (b) {
		t = a % b;
		a = b;
		b = t;
	}
	return a;
}
istream& operator >> (istream& in, Fraction& f) {
	int a, b;
	in >> a >> b;
	f.set(a, b);
	return in;
}
ostream& operator<<(ostream& out, Fraction& f) {
	out << f.fenzi << "/" << f.fenmu;
	return out;
}
```

# 这里的分数类很巧妙，其核心在于god函数找出最大公因数再用set函数给他出去达到最简的效果。





