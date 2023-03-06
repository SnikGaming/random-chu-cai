#include <iostream>
#include <cstdlib>
#include <time.h>
#include <cstring>
using namespace std;

void rand_text(int length, char *result) {
    int i, rand_int;
    char char_set[] = "0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz&quot";
 
    for (i = 0; i <length; i++) {
        result[i] = char_set[rand() % sizeof(char_set)];
    }
    result[length] = 0;
}
 
int main(){
    cout << "Nhap đo dai chuoi: ";
    int length;
    cin >> length;    

    char result[length + 1];
    srand(time(NULL));
 
    rand_text(length, result);
    cout << result;
}
