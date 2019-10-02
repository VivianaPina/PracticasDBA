# Práctica 02:
## Estimación del tamaño de una Base de Datos

Realicé una función llamada **calcularTam** codificada en el lenguaje C, en ella se pasan como parámetros el número
de tuplas o registros, y el números de registros que le caben a cada página de la base de datos.
Dentro de la función, definí como variables cada atributo de la tabla Hospital y le asigné como valores los tamaños de 
cada tipo de dato, para finalmente realizar las operaciones correspondientes. No es una función generalizada para cualquier base de datos,
sólo es para esta BD específica.

`
// Administración de Base de Datos
// Práctica 02: Estimación del tamaño de una base de datos
// PIÑA GUERRERO VIVIANA

// Librerías
#include<conio.h>
#include<stdio.h>

// Constantes

// Variables
/*  Id - int 4
	Nombre del hospital - varchar 80
	Servicio - varchar 10
	No. de trabajadores - int 4
	Horario - varchar 15
	No. de pacientes - int 4
	No. de camas - int 4
	Salas - text 65535
	No. de elevadores - int 4
	No. de edificios - int 4
	Teléfono - int 4
	Extensión - float 4
	Correo - varchar 25
	Página web - varchar 50
	Dirección - varchar 200
	Nombre del director del hospital - varchar 50
	Ranking - int 4
	Fecha de apertura - date 8
*/


// Funciones
void calcularTam(int registros, int rxpag);

main(){
	printf("\n********************ESTIMACION DEL TAMANO DE UNA BASE DE DATOS*********************\n");
	printf("***********************************************************************************\n\n");
	
	int registros = 50627392, rxpag = 35;
	
	calcularTam(registros, rxpag);
	
	getch();
}

void calcularTam(int registros, int rxpag){
	int tamFila = 0, tamPag = 0, tamBD = 0, numPags = 0;
	int id = 4, nHos = 80, serv = 10, numT = 4, hora = 15, numP = 4, numC = 4, salas = 65535, numE = 4, numEd = 4, tel = 4, m2 = 4,
	correo = 25, pagW = 50, dir = 200, nomDirH = 50, rank = 4, fechaA = 8;
	
	numPags = registros / rxpag;
	tamFila = id + nHos + serv + numT + hora + numP + numC + salas + numE + numEd + tel + m2 + correo +pagW + dir + nomDirH + rank + fechaA;
	tamPag = tamFila * rxpag;
	tamBD = numPags * tamPag;
	
	printf("\t\tTamano de una fila: %d bytes\n", tamFila);
	printf("\t\tTamano de una pagina: %d bytes\n", tamPag);
	printf("\t\tTamano de la base de datos: %d bytes\n", tamBD);	
}
`
