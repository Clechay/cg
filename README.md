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
* `a.begin()` - interator początku wektora, np dla funkcji sort
* `a.end()` - interator końca wektora, np dla funkcji sort
* `a.rbegin()` - cofający się interator początku wektora, np dla funkcji sort
* `a.rend()` - cofający się interator końca wektora, np dla funkcji sort
### modyfikacja
* `a[n] = x;` - (n+1)-ty element wektora = x, działa tak samo jak w tablicy
* `a.push_back(x);` - dodaj na końcu wektora nowy element o wartości x
* `a.pop_back();` - usuń ostatni element wektora (wektor będzie miał po tej operacji o jeden element mniej)
