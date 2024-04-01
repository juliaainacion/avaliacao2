*Exercicio1

/**
 *Data: 01/04/2024
 * @author Julia Inacio
 * email: juliainacion@icloud.com
 */
import java.util.Scanner;

// Classe que calcula a média de quatro notas digitadas pelo usuário
public class Aluno {

public static void main(String[] args) {
       // Cria um objeto Scanner para ler entrada do usuário
        Scanner scanner = new Scanner(System.in);

        // Solicita e lê a primeira nota
        System.out.println("Digite a primeira nota:");
        double nota1 = scanner.nextDouble();

        // Solicita e lê a segunda nota
        System.out.println("Digite a segunda nota:");
        double nota2 = scanner.nextDouble();

        // Solicita e lê a terceira nota
        System.out.println("Digite a terceira nota:");
        double nota3 = scanner.nextDouble();

        // Solicita e lê a quarta nota
        System.out.println("Digite a quarta nota:");
        double nota4 = scanner.nextDouble();

        // Calcula a média das notas
        double media = (nota1 + nota2 + nota3 + nota4) / 4;

          // Exibe a média
        System.out.println("A média é: " + media);

        // Fecha o Scanner para liberar recursos
        scanner.close();
    }

  
    }


    
/**
 *Data: 01/04/2024
 * @author Julia Inacio
 * email: juliainacion@icloud.com
 */

import java.util.Scanner;

// Classe que testa o cálculo de média de alunos
public class TesteAlunos {
   public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        Aluno[] alunos = new Aluno[3];

        for (int i = 0; i < 3; i++) {
            // Adiciona as notas de cada aluno
            System.out.println("Digite as notas do aluno " + (i + 1) + ":");
            double n1 = scanner.nextDouble();
            double n2 = scanner.nextDouble();
            double n3 = scanner.nextDouble();
            double n4 = scanner.nextDouble();
            alunos[i] = new Aluno(n1, n2, n3, n4);
        }

         // Calcula a soma das médias de todos os alunos
        double somaDasMedias = 0;
        for (Aluno aluno : alunos) {
            somaDasMedias += aluno.media();
        }

        // Calcula a média geral das notas dos alunos
        double mediaGeral = somaDasMedias / 3;
        System.out.println("Média geral dos alunos: " + mediaGeral);
        
        // Fecha o scanner
        scanner.close();
    }
}

