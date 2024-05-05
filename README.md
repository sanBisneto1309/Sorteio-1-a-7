# Sorteio-1-a-7
Sorteio de 1 a 7 em C++ usando a biblioteca random

#include <iostream>
#include <vector>
#include <algorithm>
#include <random>

using namespace std;

int main() {
  int num;
  cout << "Insira um número entre 1 e 7: ";
  cin >> num;
  
  vector<int> numeros = {1, 2, 3, 4, 5, 6, 7};
  random_device rd;
  shuffle(numeros.begin(), numeros.end(), rd);
  if (numeros[0] == num){
    cout << "Número sorteado: " << numeros[0] << endl;
    cout << "Você ganhou :D";
  } else if(num < 1 || num > 7){
    cout << "ERRO: Número inválido";
  } else {
    cout << "Número sorteado: " << numeros[0] << endl;
    cout << "Você perdeu :(";
  }
  return 0;
}
