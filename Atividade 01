import java.util.Scanner;

public class AnalisadorDePalavra {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        
        // Solicita ao usuário para digitar uma palavra
        System.out.print("Digite uma palavra: ");
        String palavra = scanner.nextLine();
        
        // Análise da palavra
        int tamanho = palavra.length();
        char primeiraLetra = palavra.charAt(0);
        char letraCentral = (tamanho % 2 == 0) ? palavra.charAt(tamanho / 2 - 1) : palavra.charAt(tamanho / 2);
        char ultimaLetra = palavra.charAt(tamanho - 1);
        String palavraInvertida = new StringBuilder(palavra).reverse().toString();
        String palavraMaiuscula = palavra.toUpperCase();
        String palavraMinuscula = palavra.toLowerCase();

        // Apresenta os resultados
        System.out.println("A palavra digitada foi: " + palavra);
        System.out.println("A palavra tem " + tamanho + " dígitos.");
        System.out.println("A primeira letra: " + primeiraLetra);
        System.out.println("A letra central da palavra: " + letraCentral);
        System.out.println("A última letra da palavra: " + ultimaLetra);
        System.out.println("A palavra escrita ao contrário: " + palavraInvertida);
        System.out.println("A palavra toda em maiúsculo: " + palavraMaiuscula);
        System.out.println("A palavra toda em minúsculo: " + palavraMinuscula);
        
        // Fecha o scanner
        scanner.close();
    }
}

