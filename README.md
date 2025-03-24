# ExerciciosArraylist

1:
        // Criando o ArrayList de inteiros
        ArrayList<Integer> listaDeNumeros = new ArrayList<>();
        
        // Criando o scanner para ler entradas do usuário
        Scanner scanner = new Scanner(System.in);
        
        // Solicitando ao usuário que insira cinco números
        System.out.println("Por favor, insira 5 números inteiros:");

        for (int i = 0; i < 5; i++) {
            System.out.print("Digite o número " + (i + 1) + ": ");
            int numero = scanner.nextInt();  // Lê o número inteiro inserido pelo usuário
            listaDeNumeros.add(numero);      // Adiciona o número ao ArrayList
        }
        
        // Exibindo os números armazenados no ArrayList
        System.out.println("\nOs números inseridos foram:");
         listaDeNumeros.forEach((numero) -> {
            System.out.println(numero);
        });
        
        // Fechando o scanner
        scanner.close();
    }
   }
  
2:import java.util.ArrayList;
import java.util.Scanner;

public class RemoverElementoArrayList {
    public static void main(String[] args) {
        // Criando o ArrayList de strings
        ArrayList<String> listaDeNomes = new ArrayList<>();
        
        // Adicionando os nomes ao ArrayList
        listaDeNomes.add("Patrícia");
        listaDeNomes.add("Marcio");
        listaDeNomes.add("Athur");
        listaDeNomes.add("Jorge");
        listaDeNomes.add("Ana");
        
        // Criando o scanner para ler entradas do usuário
        Scanner scanner = new Scanner(System.in);
        
        // Exibindo os nomes atuais na lista
        System.out.println("Lista de nomes:");
        listaDeNomes.forEach(nome -> System.out.println(nome));
        
        // Solicitando ao usuário um nome para remover
        System.out.print("\nDigite o nome que você deseja remover: ");
        String nomeParaRemover = scanner.nextLine();
        
        // Verificando se o nome existe na lista e removendo-o
        if (listaDeNomes.contains(nomeParaRemover)) {
            listaDeNomes.remove(nomeParaRemover);  // Remove o nome da lista
            System.out.println("\nNome removido com sucesso!");
        } else {
            System.out.println("\nNome não encontrado na lista.");
        }
        
        // Exibindo a lista atualizada
        System.out.println("\nLista atualizada:");
        listaDeNomes.forEach(nome -> System.out.println(nome));
        
        // Fechando o scanner
        scanner.close();
    }
}

3:package arraylist;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Random;

public class Arraylist {

    public static void main(String[] args) {
   

        // Criando o ArrayList de números inteiros
        ArrayList<Integer> listaDeNumeros = new ArrayList<>();
        
        // Gerador de números aleatórios
        Random random = new Random();
        
        // Adicionando 10 números aleatórios entre 1 e 100 ao ArrayList
        for (int i = 0; i < 10; i++) {
            int numeroAleatorio = random.nextInt(100) + 1;  // Gera números entre 1 e 100
            listaDeNumeros.add(numeroAleatorio);
        }
        
        // Exibindo a lista de números aleatórios
        System.out.println("Lista de números antes da ordenação:");
        listaDeNumeros.forEach(numero -> System.out.println(numero));
        
        // Ordenando a lista em ordem crescente
        Collections.sort(listaDeNumeros);
        
        // Exibindo a lista ordenada
        System.out.println("\nLista de números ordenada em ordem crescente:");
        listaDeNumeros.forEach(numero -> System.out.println(numero));
    }
}

4:package arraylist;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Random;
import java.util.Scanner;

public class Arraylist {

    public static void main(String[] args) {
   
   // Criando o ArrayList de produtos
        ArrayList<String> listaDeProdutos = new ArrayList<>();
        
        // Adicionando alguns produtos à lista
        listaDeProdutos.add("Arroz");
        listaDeProdutos.add("Feijão");
        listaDeProdutos.add("Macarrão");
        listaDeProdutos.add("Óleo");
        listaDeProdutos.add("Açúcar");
        
        // Exibindo os produtos na lista
        System.out.println("Lista de produtos:");

        listaDeProdutos.forEach((produto) -> {
            System.out.println(produto);
        });
        
        // Pedindo ao usuário para inserir o nome do produto a ser buscado
        try ( // Criando o Scanner para receber a entrada do usuário
                Scanner scanner = new Scanner(System.in)) {
            // Pedindo ao usuário para inserir o nome do produto a ser buscado
            System.out.print("\nDigite o nome do produto que deseja buscar: ");
            String produtoBusca = scanner.nextLine();
            
            // Verificando se o produto está na lista
            if (listaDeProdutos.contains(produtoBusca)) {
                System.out.println("\nProduto encontrado: " + produtoBusca);
            } else {
                System.out.println("\nProduto não encontrado.");
            }
        }
    }
}

5:package arraylist;

import java.util.ArrayList;
import java.util.Collections;
import java.util.Random;
import java.util.Scanner;

public class Arraylist {

    public static void main(String[] args) {


        // Criando o ArrayList de cidades
        ArrayList<String> listaDeCidades = new ArrayList<>();
        
        // Adicionando algumas cidades à lista
        listaDeCidades.add("São Paulo");
        listaDeCidades.add("Rio de Janeiro");
        listaDeCidades.add("Belo Horizonte");
        listaDeCidades.add("Salvador");
        listaDeCidades.add("Porto Alegre");
        
        // Exibindo as cidades na lista
        System.out.println("Lista de cidades:");
        listaDeCidades.forEach(cidade -> {
            System.out.println(cidade);
        });
        
        // Pedindo ao usuário para inserir o nome da cidade a ser substituída e a nova cidade
        try (Scanner scanner = new Scanner(System.in)) {
            // Pedindo o nome da cidade para ser substituída
            System.out.print("\nDigite o nome da cidade que deseja substituir: ");
            String cidadeSubstituida = scanner.nextLine();
            
            // Verificando se a cidade está na lista
            if (listaDeCidades.contains(cidadeSubstituida)) {
                // Pedindo o nome da nova cidade
                System.out.print("Digite o nome da nova cidade: ");
                String novaCidade = scanner.nextLine();
                
                // Substituindo a cidade
                int indice = listaDeCidades.indexOf(cidadeSubstituida);
                listaDeCidades.set(indice, novaCidade);
                
                // Exibindo a lista modificada
                System.out.println("\nLista de cidades atualizada:");
                listaDeCidades.forEach(cidade -> {
                    System.out.println(cidade);
                });
            } else {
                System.out.println("\nCidade não encontrada.");
            }
        }
    }
}
6:import java.util.ArrayList;
import java.util.Scanner;

public class ContandoOcorrencias {
    public static void main(String[] args) {
        // Criando o ArrayList de palavras
        ArrayList<String> listaDePalavras = new ArrayList<>();
        
        // Criando o Scanner para entrada do usuário
        try (Scanner scanner = new Scanner(System.in)) {
            // Pedindo ao usuário para inserir as palavras
            System.out.println("Digite várias palavras. Digite 'fim' para encerrar.");
            
            // Loop para receber várias palavras até o usuário digitar 'fim'
            String palavra;
            while (true) {
                System.out.print("Digite uma palavra: ");
                palavra = scanner.nextLine();
                
                if (palavra.equalsIgnoreCase("fim")) {
                    break; // Sai do loop quando o usuário digita 'fim'
                }
                
                listaDePalavras.add(palavra); // Adiciona a palavra à lista
            }

            // Exibindo a lista de palavras inseridas
            System.out.println("\nLista de palavras inseridas:");
            listaDePalavras.forEach(p -> System.out.println(p));

            // Pedindo ao usuário para inserir a palavra que deseja contar
            System.out.print("\nDigite a palavra que deseja contar as ocorrências: ");
            String palavraParaContar = scanner.nextLine();
            
            // Contando quantas vezes a palavra aparece na lista
            int ocorrencias = 0;
            ocorrencias = listaDePalavras.stream().filter((palavraNaLista) -> (palavraNaLista.equalsIgnoreCase(palavraParaContar))).map((_item) -> 1).reduce(ocorrencias, Integer::sum);
            
            // Exibindo o resultado
            System.out.println("\nA palavra \"" + palavraParaContar + "\" aparece " + ocorrencias + " vez(es) na lista.");
        }
    }
}

7:import java.util.ArrayList;
import java.util.HashSet;

public class RemoverRepetidos {
    public static void main(String[] args) {
        // Criando um ArrayList com números inteiros, incluindo duplicatas
        ArrayList<Integer> numeros = new ArrayList<>();
        numeros.add(1);
        numeros.add(2);
        numeros.add(3);
        numeros.add(2);
        numeros.add(4);
        numeros.add(3);
        numeros.add(5);

        // Exibindo o ArrayList original
        System.out.println("ArrayList original: " + numeros);

        // Removendo os elementos duplicados usando um HashSet
        HashSet<Integer> numerosSemRepeticao = new HashSet<>(numeros);

        // Exibindo a lista sem repetições
        System.out.println("ArrayList sem repetições: " + numerosSemRepeticao);
    }
}

8:import java.util.ArrayList;
import java.util.Collections;

public class ExemploArrayList {
    public static void main(String[] args) {
        // Criando o ArrayList e adicionando seis elementos
        ArrayList<String> lista = new ArrayList<>();
        lista.add("Elemento 1");
        lista.add("Elemento 2");
        lista.add("Elemento 3");
        lista.add("Elemento 4");
        lista.add("Elemento 5");
        lista.add("Elemento 6");

        // Exibindo os elementos na ordem original
        System.out.println("Ordem original:");
        for (String elemento : lista) {
            System.out.println(elemento);
        }

        // Exibindo os elementos na ordem inversa
        Collections.reverse(lista);
        System.out.println("\nOrdem inversa:");
        for (String elemento : lista) {
            System.out.println(elemento);
        }
    }
}

9:import java.util.ArrayList;

public class ExemploArrayList {
    public static void main(String[] args) {
        // Criando o ArrayList original com alguns nomes
        ArrayList<String> nomesOriginal = new ArrayList<>();
        nomesOriginal.add("Ana");
        nomesOriginal.add("Carlos");
        nomesOriginal.add("Juliana");
        nomesOriginal.add("Ricardo");
        nomesOriginal.add("Fernanda");

        // Criando o novo ArrayList e copiando os elementos do ArrayList original
        ArrayList<String> nomesCopia = new ArrayList<>(nomesOriginal);

        // Exibindo o ArrayList original
        System.out.println("ArrayList Original:");
        for (String nome : nomesOriginal) {
            System.out.println(nome);
        }

        // Exibindo o novo ArrayList (cópia)
        System.out.println("\nArrayList Cópia:");
        for (String nome : nomesCopia) {
            System.out.println(nome);
        }
    }
}

10:import java.util.ArrayList;
import java.util.Iterator;

public class ExemploArrayListIterator {
    public static void main(String[] args) {
        // Criando o ArrayList com cinco números inteiros
        ArrayList<Integer> numeros = new ArrayList<>();
        numeros.add(10);
        numeros.add(20);
        numeros.add(30);
        numeros.add(40);
        numeros.add(50);

        // Criando um Iterator para percorrer o ArrayList
        Iterator<Integer> iterator = numeros.iterator();

        // Utilizando o Iterator para percorrer e exibir os elementos
        System.out.println("Elementos do ArrayList:");
        while (iterator.hasNext()) {
            System.out.println(iterator.next());
        }
    }
}

11:import java.util.ArrayList;

public class ExemploArrayListDecimal {
    public static void main(String[] args) {
        // Criando o ArrayList com números decimais (do tipo Double)
        ArrayList<Double> numeros = new ArrayList<>();
        numeros.add(10.5);
        numeros.add(20.3);
        numeros.add(30.7);
        numeros.add(40.1);
        numeros.add(50.2);

        // Calculando a soma de todos os valores armazenados no ArrayList
        double soma = 0;
        for (Double numero : numeros) {
            soma += numero;
        }

        // Exibindo a soma
        System.out.println("A soma de todos os números é: " + soma);
    }
}

12:import java.util.ArrayList;
import java.util.Collections;

public class MaiorMenorValor {
    public static void main(String[] args) {
        // Criando o ArrayList com alguns números inteiros
        ArrayList<Integer> listaNumeros = new ArrayList<>();
        listaNumeros.add(15);
        listaNumeros.add(42);
        listaNumeros.add(7);
        listaNumeros.add(100);
        listaNumeros.add(23);
        
        // Encontrando o maior e o menor valor usando Collections
        int maiorValor = Collections.max(listaNumeros);
        int menorValor = Collections.min(listaNumeros);
        
        // Exibindo o resultado
        System.out.println("Maior valor: " + maiorValor);
        System.out.println("Menor valor: " + menorValor);
    }
}
13:import java.util.ArrayList;

public class MesclarArrayLists {
    public static void main(String[] args) {
        // Criando o primeiro ArrayList com 5 elementos
        ArrayList<Integer> lista1 = new ArrayList<>();
        lista1.add(10);
        lista1.add(20);
        lista1.add(30);
        lista1.add(40);
        lista1.add(50);

        // Criando o segundo ArrayList com 5 elementos
        ArrayList<Integer> lista2 = new ArrayList<>();
        lista2.add(60);
        lista2.add(70);
        lista2.add(80);
        lista2.add(90);
        lista2.add(100);

        // Criando o terceiro ArrayList que vai armazenar a mescla das duas listas
        ArrayList<Integer> listaMesclada = new ArrayList<>();
        
        // Adicionando todos os elementos de lista1 e lista2 na listaMesclada
        listaMesclada.addAll(lista1);
        listaMesclada.addAll(lista2);
        
        // Exibindo o resultado
        System.out.println("Lista mesclada: " + listaMesclada);
    }
}

14:import java.util.ArrayList;
import java.util.Scanner;

public class GerenciadorDeTarefas {

    public static void main(String[] args) {
        // Criando o ArrayList para armazenar as tarefas
        ArrayList<String> tarefas = new ArrayList<>();
        
        // Scanner para ler a entrada do usuário
        Scanner scanner = new Scanner(System.in);
        
        // Loop do menu interativo
        while (true) {
            System.out.println("\n----- Menu -----");
            System.out.println("1. Adicionar tarefa");
            System.out.println("2. Remover tarefa");
            System.out.println("3. Listar tarefas");
            System.out.println("4. Sair");
            System.out.print("Escolha uma opção: ");
            
            int opcao = scanner.nextInt();
            scanner.nextLine();  // Consumir a quebra de linha após a escolha da opção
            
            switch (opcao) {
                case 1:
                    // Adicionar tarefa
                    System.out.print("Digite a tarefa que deseja adicionar: ");
                    String tarefa = scanner.nextLine();
                    tarefas.add(tarefa);
                    System.out.println("Tarefa adicionada com sucesso!");
                    break;
                
                case 2:
                    // Remover tarefa
                    System.out.print("Digite o índice da tarefa que deseja remover (início em 0): ");
                    int indice = scanner.nextInt();
                    if (indice >= 0 && indice < tarefas.size()) {
                        tarefas.remove(indice);
                        System.out.println("Tarefa removida com sucesso!");
                    } else {
                        System.out.println("Índice inválido.");
                    }
                    break;
                
                case 3:
                    // Listar tarefas
                    if (tarefas.isEmpty()) {
                        System.out.println("Não há tarefas na lista.");
                    } else {
                        System.out.println("\nLista de tarefas:");
                        for (int i = 0; i < tarefas.size(); i++) {
                            System.out.println(i + ". " + tarefas.get(i));
                        }
                    }
                    break;
                
                case 4:
                    // Sair do programa
                    System.out.println("Saindo do programa...");
                    scanner.close();
                    return;
                
                default:
                    System.out.println("Opção inválida! Por favor, escolha uma opção válida.");
            }
        }
    }
}

15:import java.util.ArrayList;

class Aluno {
    private String nome;
    private double nota;

    // Construtor
    public Aluno(String nome, double nota) {
        this.nome = nome;
        this.nota = nota;
    }

    // Getters
    public String getNome() {
        return nome;
    }

    public double getNota() {
        return nota;
    }

    // Método para exibir informações do aluno
    public String toString() {
        return nome + " - Nota: " + nota;
    }
}

public class GerenciadorDeAlunos {
    public static void main(String[] args) {
        // Criando o ArrayList para armazenar os alunos
        ArrayList<Aluno> alunos = new ArrayList<>();

        // Adicionando alguns alunos com suas notas
        alunos.add(new Aluno("João", 7.5));
        alunos.add(new Aluno("Maria", 9.0));
        alunos.add(new Aluno("Carlos", 6.5));
        alunos.add(new Aluno("Ana", 8.0));
        
        // Exibindo a lista de alunos e suas notas
        System.out.println("Lista de alunos e suas notas:");
        for (Aluno aluno : alunos) {
            System.out.println(aluno);
        }

        // Calculando a média das notas
        double somaNotas = 0;
        for (Aluno aluno : alunos) {
            somaNotas += aluno.getNota();
        }
        
        double media = somaNotas / alunos.size();
        
        // Exibindo a média das notas
        System.out.println("\nMédia das notas: " + media);
    }
}

