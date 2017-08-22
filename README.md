# practico2
// chachon.cpp : Defines the entry point for the console application.
//

#include "stdafx.h"
#include <iostream>
#include "stdio.h"
#include "conio.h"
#include "math.h"

using namespace std;

void leer(float &A, float &B, float &C);
void calculo(float A, float B, float C, float &X1, float &X2);


void main()
{float A, B, C, X1, X2;
leer(A, B, C);
calculo( A, B, C, X1, X2);
getch();
}


void leer(float &A, float &B, float &C)
{ cout<<" Ingrese el valor de A: ";
  cin>>A;
  cout<<" Ingrese el valor de B: ";
  cin>>B;
cout<<" Ingrese el valor de C: ";
  cin>>C;
}



void calculo(float A, float B, float C, float &X1, float &X2)
{float d;
float Xr, Xi;
d = ((B*B)-(4*A*C));
if (d<0)
{cout<<"X es imaginario \n";
Xr= ((-B)/(2*A));
Xi= ((sqrt(-d))/(2*A));
cout<<"X = "<<Xr<<"+-"<<Xi<<"(-1)";
}else
{if (d==0)
{cout<<"Solucion unica";
X1= (-B/(2*A));
cout<<" X = "<<X1;
}else
{cout<<"2 soluciones:";
X1= ((-B+(sqrt(d)))/(2*A));
cout<<"X1 ="<<X1;
X2= ((-B-(sqrt(d)))/(2*A));
cout<<"X2 ="<<X2;
}
}
}
