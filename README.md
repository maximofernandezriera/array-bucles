# array-bucles
Ejemplos de clase

# con mientras

//################################################################################
//Implementar un programa que permita declarar un vector de diez elementos enteros y pida números al usuario hasta 
//o bien se introduzca un número negativo. 
//Al finalizar la introducción de los números, el programa deberá imprimir el array (sólo los elementos introducidos).

//################################################################################
//Análisis del Algoritmo 

//Recorro el vector y voy inicializando sus elementos. Si introduzco un número 
//negativo salimos del bucle. También termino el bucle si introduzco todos los 
//elementos de vector. El número negativo me sirve de indicador de que hasta 
//esa posición el vector tiene elementos. 
//Recorro hasta el tamaño del vector o encuentre un número negativo para mostrar 
//los elementos del vector.
// Datos de entrada: Leo número positivos y los guardo en el vector, hasta que lea 
//un número negativo o lea todos los elementos del vector.
// Información de salida:Los elementos (números positivos) guardados en el vector.
// Variables, por ejemplo: vector (vector de 10 enteros), tam_vector,indice (Entero)
//################################################################################

Algoritmo arrayPositivosMientras
	
	Definir vector Entero;
	Dimension vector[10];
	Definir tam_vector,indice Entero;
	Definir seguir Logico;
	indice<-1;
	tam_vector<-10;
	seguir <- Verdadero;
	
	//Recorro el vector y voy inicializando sus elementos
	//No uso un para, porque si introduzco un número negativo salimos del bucle.
	//También termino el bucle si introduzco todos los elementos de vector.
	//El número negativo me sirve de indicador de que hasta esa posición el vector tiene elemento-
	
	Mientras indice < tam_vector y seguir = Verdadero Hacer
		Escribir "Introduce un número en el vector. Número: ",indice;
		Leer vector[indice];
		Si vector[indice]<=0 Entonces
			seguir <- Falso;
		FinSi
		indice<-indice+1;
	FinMientras
	

	//Recorro hasta el tamaño del vector o encuentre un número negativo.
	Escribir "Estos son los elementos del vector: ";
	indice<-1;
	Mientras indice<tam_vector Y vector[indice]>=0 Hacer
		Escribir vector[indice]," ";
		indice<-indice+1;
	FinMientras
	
FinAlgoritmo

# con Repetir

//################################################################################
//Programa que declare un vector de diez elementos enteros y pida números para 
//rellenarlo hasta que se llene el vector o se introduzca un número negativo. 
//Entonces se debe imprimir el vector (sólo los elementos introducidos).
//################################################################################
//Análisis
//Recorro el vector y voy inicializando sus elementos. Si introduzco un número 
//negativo salimos del bucle. También termino el bucle si introduzco todos los 
//elementos de vector. El número negativo me sirve de indicador de que hasta 
//esa posición el vector tiene elementos. 
//Recorro hasta el tamaño del vector o encuentre un número negativo para mostrar 
//los elementos del vector.
// Datos de entrada: Leo número positivos y los guardo en el vector, hasta que lea 
//un número negativo o lea todos los elementos del vector.
// Información de salida:Los elementos (números positivos) guardados en el vector.
// Variables: vector (vector de 10 enteros), tam_vector,indice,num (Entero)
//################################################################################

Proceso arrayPositivosRepetir
	Definir vector Como Entero;
	Dimension vector[10];
	Definir tam_vector,indice,num como Entero;
	indice<-1;
	tam_vector<-10;
	//Recorro el vector y voy inicializando sus elementos
	//No uso un para, porque si introduzco un número negativo salimos del bucle.
	//También termino el bucle si introduzco todos los elementos de vector.
	//El número negativo me sirve de indicador de que hasta esa posición el vector tiene elemento-
	Repetir
		Escribir Sin Saltar "Introduce un número en el vector. Número: ",indice;
		Leer vector[indice];
		indice<-indice+1;
	Hasta Que indice>=tam_vector O vector[indice-1]<0;
	indice<-1;
	//Recorro hasta el tamaño del vector o encuentre un número negativo.
	Escribir "Elementos del vector";
	Mientras indice<tam_vector-1 Y vector[indice]>=0 Hacer
		Escribir sin saltar vector[indice]," ";
		indice<-indice+1;
	FinMientras
FinProceso


