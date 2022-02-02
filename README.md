#include <iostream>
#include <locale.h>
using namespace std;

int aniosDias (int anios){
	int dias;
	const int DIASENANIO = 365;
	return DIASENANIO*anios;
}
int aniosAMeses (int anios){
	int dias;
	const int MESESENANIO = 12;
	return MESESENANIO*anios;
}

int dientesCaidos(int anios){
	int meses;
	int total = 0;
	meses = aniosAMeses(anios);
	for (int i = 0; i <= meses; i +=5){
		total += i;
	}
	return total;
}

int dientesCaidosTope(int anios, int maximoAnios){
	int meses;
	int maximoMeses;
	int total = 0;
	meses = aniosAMeses(anios);
	maximoMeses = aniosAMeses(maximoAnios)
	for (int i = 0; i <= meses && i< maximoMeses; i +=5){
		total += i; 
	}
	return total;
}

int main(){
	setlocale(LC_CTYPE, "Spanish");

	int aniosTiburon;
	int mesesTiburon;
	int diasTiburon;
	int totalDientes;
	int tope = 8


//imprime tu nombre por pantalla
	cout << "vicky"<< endl;
// pregunta por pantalla cuantos años tiene el tiburon
	cout<< "cuanrtos años tiene el tiburon?";
	cin>> aniosTiburon;
	cout << "el tiburon tiene " <<aniosTiburon<< " años" << endl;
//partiendo de un numero de años calcula cuanto tiempo en dias y en meses ha pasado ?
	diasTiburon = aniosDias(aniosTiburon);
	cout<<"el tiburon tiene " << diasTiburon << " anios " << endl;
//calcula cuantos dientes se le han caido al tiburon 
	totalDientes = dientesCaidos(aniosTiburon);
	cout<<"al tiburon de le han caido "<< totalDientes<< " dientes" << endl;
// SI EL TIBURON TIENE MAS DE OCHO AÑOS YA NO LE QUEDAN DIENTES QUE SE LE PODRAN CAER
// modifica la funcion anterior para que deje de sumar dientes caidos para cuando tenga 8 años 
	totalDientes = dientesCaidosTope(aniosTiburon, tope);
	cout<<"al tiburon de le han caido "<< totalDientes<< " dientes" << endl;
	return 0;
}
