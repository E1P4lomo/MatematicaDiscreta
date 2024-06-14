# MatematicaDiscreta
import java.util.ArrayList;
import java.util.Scanner;

public class FibonacciRange {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Solicitamos al usuario los valores de a y b
        System.out.print("Ingrese el valor de a: ");
        int a = scanner.nextInt();
        
        System.out.print("Ingrese el valor de b: ");
        int b = scanner.nextInt();
        
        // Generamos la sucesión de Fibonacci dentro del rango [a, b]
        ArrayList<Integer> fibSequence = fibonacciRange(a, b);
        
        // Imprimimos el resultado
        System.out.println("La sucesión de Fibonacci desde " + a + " hasta " + b + " es: " + fibSequence);
    }
    
    public static ArrayList<Integer> fibonacciRange(int a, int b) {
        // Inicializamos los dos primeros números de la sucesión de Fibonacci
        int fib1 = 0, fib2 = 1;
        
        // Lista para almacenar la secuencia de Fibonacci dentro del rango
        ArrayList<Integer> fibSequence = new ArrayList<>();
        
        // Generamos los números de la sucesión de Fibonacci
        while (fib1 <= b) {
            if (fib1 >= a) {
                fibSequence.add(fib1);
            }
            int nextFib = fib1 + fib2;
            fib1 = fib2;
            fib2 = nextFib;
        }
        
        return fibSequence;
    }
}
