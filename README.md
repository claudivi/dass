#include <stdio.h>
#include <math.h>

int main() {
    float a, b, c;
    float discriminante, parteReal, parteImaginaria, raiz1, raiz2;

    // Solicita al usuario que ingrese los coeficientes de la ecuación cuadrática
    printf("Ingrese los coeficientes a, b y c de la ecuacion cuadratica (ax^2 + bx + c = 0):\n");
    printf("a:");scanf("%f", &a);
    printf("b:");scanf("%f",&b);
    printf("c:");scanf("%f",&c);

   
    discriminante = b * b - 4 * a * c;

    
    if (discriminante > 0) {
        // Raíces reales y diferentes
        raiz1 = (-b + sqrt(discriminante)) / (2 * a);
        raiz2 = (-b - sqrt(discriminante)) / (2 * a);
        printf("Las raices son reales y diferentes:\n");
        printf("Raiz1 = %.2f y Raiz2 = %.2f\n", raiz1, raiz2);
    } else if (discriminante == 0) {
        // Raíces reales e iguales
        raiz1 = raiz2 = -b / (2 * a);
        printf("Las raices son reales e iguales:\n");
        printf("Raiz1 = Raiz2 = %.2f\n", raiz1);
    } else {
        // Raíces complejas
        parteReal = -b / (2 * a);
        parteImaginaria = sqrt(-discriminante) / (2 * a);
        printf("Las raices son complejas:\n");
        printf("Raiz1 = %.2f + %.2fi y Raiz2 = %.2f - %.2fi\n", parteReal, parteImaginaria, parteReal, parteImaginaria);
    }

    return 0;}
