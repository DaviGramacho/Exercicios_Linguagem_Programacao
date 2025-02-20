# Exercicios_Desenvolvimento_BD
17 exercícios da aula de desenvolvimento de banco de dados do dia 19/02/2025

<h1>1. Faça um algoritmo que leia a idade de uma pessoa expressa em anos, meses e dias e escreva a idade dessa pessoa expressa apenas em dias. Considerar ano com 365 dias e mês com 30 dias.</h1>


```
  /* Exercicio 1 */

/*Importando imput para o usuario*/
import java.util.Scanner;

public class Atividade_Um{
    public static void main(String []args){
        /*Criando as variaveis para converter*/
        int mesConver,anoConver,totalDias;
        
        
        /*Adiciona o scanner*/
        Scanner sc = new Scanner(System.in);

        /*Solicita a idade e gera o input*/
        System.out.print("Escreva sua idade: ");
        int idade = sc.nextInt();
        
        System.out.print("Escreva o dia em que nasceu: ");
        int dias = sc.nextInt();
        
        System.out.print("Escreva o mes que voce nasceu: ");
        int mes = sc.nextInt();

        /*Calculos para o resultado*/
        anoConver = 365*idade;
        mesConver = (30*mes);
        totalDias = (anoConver+mesConver+dias);
        
        /*output do resultado*/
        System.out.print("Sua idade em DIAS : " + totalDias);
     }
}

```

<h1>2.Escreva um algoritmo para ler o número total de eleitores de um município, o número de votos brancos, nulos e válidos. Calcular e escrever o percentual que cada um representa em relação ao total de eleitores.</h1>

```
  /* Exercicio 2 */

/*Importando imput para o usuario*/
import java.util.Scanner;

public class Atividade_Dois{
    public static void main(String []args){
        /*Criando as variaveis para converter*/
        double brancoPor, nulosPor, validosPor ;
        
        /*Adiciona o scanner*/
        Scanner sc = new Scanner(System.in);

        /*Solicita as informações e gera o input*/
        System.out.print("Escreva a quantidade de eleitores: ");
        double eleitores = sc.nextInt();
        
        System.out.print("Escreva a quantidade de votos em branco: ");
        double branco = sc.nextInt();
        
        System.out.print("Escreva a quantidades de votos nulos: ");
        double nulos = sc.nextInt();
        
        System.out.print("Escreva de votos validos: ");
        double validos = sc.nextInt();

        /*Calculos para o resultado*/
        brancoPor = (branco/eleitores) * 100;
        nulosPor = (nulos/eleitores) * 100;
        validosPor = (validos/eleitores) * 100;
        
        /*output do resultado*/
        System.out.print("Porcentagem de pessoas que votaram em branco: " + brancoPor +"%");
        
        System.out.print("Porcentagem de pessoas que votaram em branco: " + nulosPor +"%");
        
        System.out.print("Porcentagem de pessoas que votaram em branco: " + validosPor +"%");
     }
}

```

<h1>3.Escreva um algoritmo para ler o salário mensal atual de um funcionário e o percentual de reajuste. Calcular e escrever o valor do novo salário.</h1> 

```
  /* Exercicio 3 */

/*Importando imput para o usuario*/
import java.util.Scanner;

public class Atividade_Tres{
    public static void main(String []args){
        /*Criando as variaveis para converter*/
        double salario, reajuste, novoSalario, total;
        
        /*Adiciona o scanner*/
        Scanner sc = new Scanner(System.in);

        /*Solicita as informações e gera o input*/
        System.out.print("ALERTA: Digite apenas numeros!\nEscreva o salario: ");
        salario = sc.nextInt();
        
        System.out.print("Escreva o reajuste do salario em porcentagem: ");
        reajuste = sc.nextInt();

        /*Calculos para o resultado*/
        novoSalario = salario * (1 + (reajuste / 100.0));
        
        /*output do resultado*/
        System.out.print("O salario com o reajuste: " + novoSalario);
        
     }
}

```

<h1> O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos (aplicados ao custo de fábrica). Supondo que o percentual do distribuidor seja de 28% e os impostos de 45%, escrever um algoritmo para ler o custo de fábrica de um carro, calcular e escrever o custo final ao consumidor. </h1>

```
  /* Exercicio 4 */

/*Importando imput para o usuario*/
import java.util.Scanner;

public class Atividade_quatro{
    public static void main(String []args){
        /*Criando as variaveis para converter*/
        double custoFabrica, precoFinal;
        double imposto = 45.0;
        double distribuidor = 28.0;
        /*Adiciona o scanner*/
        Scanner sc = new Scanner(System.in);

        /*Solicita as informações e gera o input*/
        System.out.print("Custo de fabrica do seu carro: ");
        custoFabrica = sc.nextInt();
        

        /*Calculos para o resultado*/
        distribuidor = (custoFabrica * distribuidor / 100);
        imposto = (custoFabrica * imposto / 100);
        precoFinal = distribuidor + imposto + custoFabrica;
        
        /*output do resultado*/
        System.out.println(distribuidor);
        System.out.println(imposto);
        System.out.print("Preco final do carro: " + precoFinal);
        
     }
}

```

