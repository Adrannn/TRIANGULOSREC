##C++
#include <iostream>
using namespace std;

int main() {
    int numero;
    
    cout << "Ingrese un numero entero positivo: ";
    cin >> numero;
    
    cout << "Elija el tipo de triangulo rectangulo:" << endl;
    cout << "1. Triangulo rectangulo con angulo derecho" << endl;
    cout << "2. Triangulo rectangulo con angulo izquierdo" << endl;
    cout << "3. Triangulo rectangulo con angulo superior" << endl;
    cout << "4. Triangulo rectangulo con angulo inferior" << endl;
    
    int opcion;
    cin >> opcion;
    
    if (opcion == 1) {
        for (int i = 1; i <= numero; i++) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else if (opcion == 2) {
        for (int i = numero; i >= 1; i--) {
            for (int j = 1; j <= i; j++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else if (opcion == 3) {
        for (int i = 1; i <= numero; i++) {
            for (int j = 1; j <= numero - i; j++) {
                cout << "  ";
            }
            for (int k = 1; k <= i; k++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else if (opcion == 4) {
        for (int i = numero; i >= 1; i--) {
            for (int j = 1; j <= numero - i; j++) {
                cout << "  ";
            }
            for (int k = 1; k <= i; k++) {
                cout << "* ";
            }
            cout << endl;
        }
    } else {
        cout << "Opcion no valida." << endl;
    }
    
    return 0;
}

##Pseudocodigo
Algoritmo TrianguloRectangulo
		
		Escribir("Ingrese un número entero positivo:")
		Leer numero
		
		// Solicitar al usuario el tipo de triángulo rectángulo
		Escribir("Elija el tipo de triángulo rectángulo:")
		Escribir("1. Triángulo rectángulo con ángulo derecho")
		Escribir("2. Triángulo rectángulo con ángulo izquierdo")
		Escribir("3. Triángulo rectángulo con ángulo superior")
		Escribir("4. Triángulo rectángulo con ángulo inferior")
		Leer opcion
		
		
		Si opcion >= 1 y opcion <= 4 Entonces
			Si opcion = 1 Entonces
				Para i <- 0 Hasta numero Hacer
					Para j <- 0 Hasta i Hacer
						Escribir Sin Saltar "*";
					Fin Para
					Escribir "";
				Fin Para

			Sino Si opcion = 2 Entonces
					Para i <- 0 Hasta numero Hacer
						Para j <- numero Hasta i Hacer
							Escribir Sin Saltar "*";
						Fin Para
						Escribir "";
					Fin Para
				Sino Si opcion = 3 Entonces
						Para i <- 1 Hasta numero Hacer
							Para j <- 1 Hasta numero - i Hacer
								Escribir Sin Saltar "";
							Fin Para
							Para k <- 1 Hasta i Hacer
								Escribir Sin Saltar "*";
							Fin Para
							Escribir " ";
						Fin Para
					Sino Si opcion = 4 Entonces
							Para i <- 1 Hasta numero Hacer
								Para j <- 1 Hasta numero - i Hacer
									Escribir "";
								Fin Para
								Para k <- 1 Hasta i Hacer
									Escribir Sin Saltar "*";
								Fin Para
								Escribir "";
							Fin Para
						Fin Si
		
						
						Escribir("Opción no válida.")
						
						
					FinSi
					
				FinSi
			FinSi
		Fin Si
Fin Algoritmo

##Pythom
numero = int(input("Ingrese un numero entero positivo: "))

print("Elija el tipo de triangulo rectangulo:")
print("1. Triangulo rectangulo con angulo derecho")
print("2. Triangulo rectangulo con angulo izquierdo")
print("3. Triangulo rectangulo con angulo superior")
print("4. Triangulo rectangulo con angulo inferior")

opcion = int(input())

if opcion == 1:
    for i in range(1, numero + 1):
        print("* " * i)
elif opcion == 2:
    for i in range(numero, 0, -1):
        print("* " * i)
elif opcion == 3:
    for i in range(1, numero + 1):
        print("  " * (numero - i) + "* " * i)
elif opcion == 4:
    for i in range(numero, 0, -1):
        print("  " * (numero - i) + "* " * i)
else:
    print("Opcion no valida.")
