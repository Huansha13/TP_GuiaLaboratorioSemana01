# TP_GuiaLaboratorioSemana01
Guía laboratorio Semana 01 - Taller de programacion
### Ejercicios a desarrollar
> 1. Pide un número y muestra si es positivo o negativo y si es par o impar

```
import java.util.Scanner;
public class parimpar {
    public static void main(String[] args) {
        int numero;
        Scanner teclado = new Scanner(System.in);
        System.out.println("Introduce un numero");
        numero = teclado.nextInt();
        if(numero<0) {
            System.out.println ("El numero "+numero+" es negativo\n");  
        }   
        else {
            System.out.println ("El numero "+numero+" es positivo\n"); 
        }
        if(numero%2==0) {
            System.out.println ("El numero "+numero+" es par\n");  
        }   
        else {
            System.out.println ("El numero "+numero+" es impar\n"); 
        }
    }
}
```
> 2. Pide 2 números y muestra cual es el mayor, el menor, o si son iguales.
```
import java.util.Scanner;
puclic class maiormenor {
    public static void main(String[] args) {
        Scanner teclado = new Scanner(System.in);
        int num1;
        int num2;
        System.out.println ("Introduce un numero");
        num1 = teclado.nextInt();
        System.out.println ("Introduce otro numero");
        num2 = teclado.nextInt();
        if(num1==num2) {
            System.out.println ("Son iguales");
        }
        else if(num1>num2) {
            System.out.println ("El mayor e "+num1);		
        }
        else {
            System.out.println ("El mayor e "+num2); 
        }
    }
}
```
> 3. Pide dos números por teclado, los suma y muestra el resultado.
```
import java.util.Scanner;
public class sumanum {

    public static void main(String[] args) {
	Scanner teclado = new Scanner(System.in);
	int num1;
	int num2;
	int suma;
	System.out.println ("Introduce un numero");
	num1 = teclado.nextInt();
	System.out.println ("Introduce otro numero");
	num2 = teclado.nextInt();
	suma = num1 + num2;
	System.out.println ("El resultado de la suma es "+suma);
    }
}
```
> 4. Haz una aplicación que calcule el área de un círculo(pi*R2). El radio se pedirá por teclado (recuerda pasar de String a double con Double.parseDouble). Usa la constante PI y el método pow de Math. (realizar una versión aplicando JOptionPane).
```
import javax.swing.JOptionPane;
public class DivisibleApp {
 
    public static void main(String[] args) {
 
        String texto=JOptionPane.showInputDialog("Introduce un numero");
        //Pasamos el String a int
        int numero=Integer.parseInt(texto);
 
        //Comprobamos si es divisible entre 2, es decir, si el resto de la division es 0
        if (numero%2==0){
            System.out.println("El numero "+numero+" es divisible entre 2");
        }else{
            System.out.println("El numero "+numero+" no es divisible entre 2");
        }
    }
}
```
> 5. Lee un número por teclado e indica si es divisible entre 2 (resto = 0). Si no lo es, también debemos indicarlo:
    
    - Versión con Scanner.
```
import java.util.Scanner;

public class PrecioProductoApp {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);
        System.out.println("Introduce un caracter ASCII");
        char caracter = sc.next().charAt(0);

        //Pasamos el caracter a codigo
        int codigo = (int) caracter;

        System.out.println(codigo);
    }
}
```
    - Versión con JOptionPane.
```
import javax.swing.JOptionPane;
public class PrecioProductoApp {
 
    public static void main(String[] args) {
 
        //Declaramos una constante
        final double IVA=0.21;
 
        String texto=JOptionPane.showInputDialog("Introduce el precio de un producto");
        //Pasamos el String a double
        double precio=Double.parseDouble(texto);
 
        //Obtenemos el precio final (precio+(precio*IVA))
        double precioFinal=precio+(precio*IVA);
 
        System.out.println(precioFinal);
    }
}
```
