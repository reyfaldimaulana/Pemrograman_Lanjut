/*
Nama	: Reyfaldi Maulana Firmansyah
NPM		: 20081010163
Kelas	: D081
*/

#include <stdio.h>
#include <stdlib.h>

int iteratif(int x, int y){
	int equal = 1;
	for(int z = 1; z <= y; z++){
		equal = equal * x;
	}
	return equal;
}

int rekursif(int x, int y){
	if(y==0){
		return 1;
	}
	else{
		return x * rekursif (x, y-1);
	}
}

int main(){
	int x, y;
	
	printf("INPUT BILANGAN YANG INGIN DIPANGKATKAN: ");
	scanf("%d", &x);
	printf("INPUT PANGKAT BILANGAN: ");
	scanf("%d", &y);
	printf("Pangkat %d dari bilangan %d adalah \n", y, x, iteratif (x,y));
	printf("ITERATIF : %d\n", iteratif(x,y));
	printf("REKURSIF : %d\n", rekursif(x,y));
	return 0;
}
