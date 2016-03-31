#include <iostream>
#include <stdlib.h>
using namespace std;
int fim = 0;
int vetor[10];
int ini = 0;
int tam = 10;

int test_full(int n){
	if (fim == 10) {
		return 0;
	} else {
		return 1;
	}
}

int test_empty(int n){
	if (fim == 0) {
		return 0;
	} else {
		return 1;
	}
}


int incluir(int n){
	if (test_full(1) == 0){
		cout << " lotadios ";
	} else {
		int valor;
		cout << " digite o valor ";
		cin >> valor;
		vetor[fim] = valor;
		fim++; 
	}
}

int consultar(int n){
	if (test_empty(1) == 0) {
		cout << " vaziodios ";
	} else {
		for (int x = ini; x<fim; x++) {
			cout << " posicao [" << x <<"] " << vetor[x] << "  \n";
		}
	}
}

int excluir(int n){
	if (test_empty(1) == 0){
		cout << " vazios ";
	} else {
		for (int x = ini; x<=fim; x++) {
			vetor[x] = vetor[x+1];
			
			
		}
		fim--;
	}
}


int main() {
	int opcao = 1;
	while (opcao != 0) {
		cout << " menu \n";
		cout << " opc 1: - incluir \n";
		cout << " opc 2: - excluir \n";
		cout << " opc 3: - consultar \n";
		cout << " digite a opcao ";
		cin >> opcao;
		
		if (opcao == 1) {
			incluir(1);
		}
		
		if (opcao == 2) {
			excluir(1);
		}
		
		if (opcao == 3) {
			consultar(1);
		}
		
		system("PAUSE");
		system("cls");
	}
	
	return 0;
}
