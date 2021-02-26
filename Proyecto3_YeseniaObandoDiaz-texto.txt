Algoritmo proyecto_3
	//Declaración de variables
	Definir numArab, unidades, decenas, centenas, millares como entero;
	Definir seguir como caracter; 
	Definir digitoM, digitoC, digitoD, digitoU Como Caracter;
	numArab=0;
	seguir='s';
	
	
	//Mensaje de bienvenida al usuario
	Escribir 'CONVERSOR DE NÚMEROS ARÁBIGOS A ROMANOS';
	
//Se usa mientras para hacer se el proceso se haga cuantas veces el usuario quiera
	Mientras seguir='s' o seguir='S' Hacer
	
	//Pide el número a convertir y lo lee
	Escribir 'Digite un número entero entre 1 a 3999';
	Leer numArab;
	 
	      //Valida que el número esté en el rango
	    Si (numArab>0) y (numArab<4000) Entonces
		
		//Primero, se separa el número en unidades, decenas, centenas, millares
		millares <- trunc (numArab/1000)mod 10;
		centenas <- trunc (numArab/100)mod 10;
		decenas <- trunc (numArab/10)mod 10;
		unidades <- numArab mod 10;

		   //Luego, se convierte de números arábigos a romanos
		   Segun millares Hacer
			0: digitoM <-'';
			1: digitoM <- 'M';
			2: digitoM <- 'MM';
			3: digitoM <- 'MMM';
		   FinSegun
		   Segun centenas Hacer
			0: digitoC <- '';
			1: digitoC <- 'C'; 
			2: digitoC <- 'CC';
			3: digitoC <- 'CCC';
			4: digitoC <- 'CD';
			5: digitoC <- 'D';
			6: digitoC <- 'DC';
			7: digitoC <- 'DCC';
			8: digitoC <- 'DCCC';
			9: digitoC <- 'CM';
		   FinSegun;
		   Segun decenas Hacer
			0: digitoD <- '';
			1: digitoD <- 'X'; 
			2: digitoD <- 'XX';
			3: digitoD <- 'XXX';
			4: digitoD <- 'XL';
			5: digitoD <- 'L';
			6: digitoD <- 'LX';
			7: digitoD <- 'LXX';
			8: digitoD <- 'LXXX';
			9: digitoD <- 'XC';
		   FinSegun;
		   Segun unidades Hacer
			0: digitoU <- '';
			1: digitoU <- 'I'; 
			2: digitoU <- 'II';
			3: digitoU <- 'III';
			4: digitoU <- 'IV';
			5: digitoU <- 'V';
			6: digitoU <- 'VI';
			7: digitoU <- 'VII';
			8: digitoU <- 'VIII';
			9: digitoU <- 'IX';
		  FinSegun;
		  Escribir 'La conversión del número arábigo ', numArab, ' en números romanos es ', digitoM,digitoC,digitoD,digitoU;		
		  Esperar 2.4 Segundos;
		  
		  //Pide otro número si no está en el rango	
	    SiNo
		Escribir 'El número digitado no está entre 1 y 3999. Por favor, inténtelo de nuevo. Presione cualquier tecla para continuar';
	    Esperar Tecla;
	    FinSi;
		Borrar Pantalla;
		
	//Para ver si quiere seguir convirtiendo otros numeros
	Escribir '¿Desea realizar otra conversión? n=no, s=sí';
	Leer seguir;
FinMientras;
	
FinAlgoritmo
