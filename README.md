# DreamShaper

Segue em anexo o projeto final desenvolvido em Java utilizando ArrayList, estruturas condicionais, repetição e métodos. O sistema foi testado e organizado conforme os conteúdos estudados durante a disciplina.


import java.util.ArrayList;
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        ArrayList<String> alunos = new ArrayList<>();

        int opcao;

        do {

            System.out.println("\n--- MENU ---");
            System.out.println("1 - Cadastrar aluno");
            System.out.println("2 - Listar alunos");
            System.out.println("3 - Remover aluno");
            System.out.println("0 - Sair");

            System.out.print("Escolha uma opção: ");
            opcao = sc.nextInt();
            sc.nextLine();

            if (opcao == 1) {

                System.out.print("Digite o nome do aluno: ");
                String nome = sc.nextLine();

                alunos.add(nome);

                System.out.println("Aluno cadastrado com sucesso!");

            } else if (opcao == 2) {

                System.out.println("\nAlunos cadastrados:");

                for (int i = 0; i < alunos.size(); i++) {
                    System.out.println((i + 1) + " - " + alunos.get(i));
                }

            } else if (opcao == 3) {

                System.out.print("Digite o nome do aluno para remover: ");
                String nomeRemover = sc.nextLine();

                if (alunos.remove(nomeRemover)) {
                    System.out.println("Aluno removido!");
                } else {
                    System.out.println("Aluno não encontrado.");
                }

            } else if (opcao == 0) {

                System.out.println("Programa encerrado.");

            } else {

                System.out.println("Opção inválida!");

            }

        } while (opcao != 0);

        sc.close();
    }
}
