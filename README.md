# vector

### deklaracja
* `vector <int> a;` -  deklaracja pustego wektora typu `int` o nazwie `a`
* `vector <int> a (11);` -  deklaracja wektora typu `int` o nazwie `a` zawierającego 11 pustych elementów (11 zer)

### dostęp

#### podstawowe
* `a[n]` - (n+1)-ty element wektora, działa tak samo jak w tablicy
* `a.size()` - liczba elementów w wektorze

#### dodatkowe
* `a.front()` - pierwszy element wektora
* `a.back()` - ostatni element wektora
* `a.begin()` - iterator początku wektora, np dla funkcji sort
* `a.end()` - iterator końca wektora, np dla funkcji sort
* `a.rbegin()` - cofający się iterator początku wektora, np dla funkcji sort
* `a.rend()` - cofający się iterator końca wektora, np dla funkcji sort

### modyfikacja
* `a[n] = x;` - (n+1)-ty element wektora = x, działa tak samo jak w tablicy
* `a.push_back(x);` - dodaj na końcu wektora nowy element o wartości x
* `a.pop_back();` - usuń ostatni element wektora (wektor będzie miał po tej operacji o jeden element mniej)

### przykładowy kod

```cpp
#include <iostream>
#include <string>
#include <vector>
int main()
{
	using namespace std;
	vector < vector < int> > graf;
	int n; cin >> n; // liczba wiercholkow
	int k; cin >> k; // liczba krawedzi laczacych wiercholki
	graf.resize(n);
	int a,b;
	// wczytywanie danych o grafie
	for (int i = 0; i < n; ++i)
	{
		cin >> a >>b;
		graf[a].push_back(b);
		graf[b].push_back(a);
	}
	//wypisanie grafu
	for (int i = 0; i < graf.size(); ++i)
	{
		cout << i << ": ";
		for (int j = 0; j < graf[i].size(); ++j)
		{
			cout << graf[i][j] << " ";
		}
		cout << endl;
	}
    return 0;
}
```
