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
## Teste de Mesa - Exemplo de Execução do Código

### Código:

O algoritmo calcula a idade de uma pessoa em dias, levando em consideração o número de anos, meses e dias fornecidos pelo usuário.

#### Entradas:
- Idade: 25 anos
- Mês de nascimento: 3 (março)
- Dia de nascimento: 15

### Execução Passo a Passo (Teste de Mesa):

| Passo                         | Variáveis                    | Descrição                                             |
|-------------------------------|------------------------------|-------------------------------------------------------|
| **1. Inicialização**           | `anoConver`, `mesConver`, `totalDias ` | O código começa com todas as variáveis inicializadas. |
| **2. Entrada da Idade**        | `idade = 25`                 | O usuário digita a idade como 25 anos.                |
| **3. Entrada do Mês**          | `mes = 3`                    | O usuário digita o mês de nascimento como 3 (março). |
| **4. Entrada do Dia**          | `dias = 15`                  | O usuário digita o dia de nascimento como 15.        |
| **5. Cálculo dos Anos em Dias**| `anoConver = 365 * 25 = 9125` | A idade em anos é convertida para dias (365 dias por ano). |
| **6. Cálculo dos Meses em Dias**| `mesConver = 30 * 3 = 90`    | O mês de nascimento é convertido para dias (30 dias por mês). |
| **7. Cálculo do Total de Dias**| `totalDias = 9125 + 90 + 15 = 9230` | A soma dos dias é feita: anos, meses e dias.         |
| **8. Saída**                   | `totalDias = 9230`           | O programa exibe o total de dias como 9230.          |





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
<h1>Uma revendedora de carros usados paga a seus funcionários vendedores um salário fixo por mês, mais uma comissão também fixa para cada carro vendido e mais 5% do valor das vendas por ele efetuadas. Escrever um algoritmo que leia o número de carros por ele vendidos, o valor total de suas vendas, o salário fixo e o valor que ele recebe por carro vendido. Calcule e escreva o salário final do vendedor.</h1>


```
/* Exercicio 5 */
import java.util.Scanner;
public class atividade_Cinco{

     public static void main(String []args){
        Scanner sc = new Scanner(System.in);
        
        double salarioFixo, salarioFinal, comissaoFixa, comissaoTotal ,valorVenda;
        
        int carrosVendidos;
        System.out.println("Qual seu salario fixo: ");
        salarioFixo = sc.nextDouble();
        
        System.out.println("Qual o valor da sua venda: ");
        valorVenda = sc.nextDouble();
        
        System.out.println("Quantidades de carros vendidos: ");
        carrosVendidos = sc.nextInt();
        
        
        comissaoFixa = 0.05 * valorVenda;
        comissaoTotal = comissaoFixa * carrosVendidos;
        salarioFinal = salarioFixo + comissaoTotal;
        
        System.out.println("Salario final: " + salarioFinal);
     }
}

```
<h1>6. Escreva um algoritmo para ler uma temperatura em graus Fahrenheit, calcular e escrever o valor correspondente em graus Celsius. Observação: Para testar se a sua resposta está correta saiba que 100°C = 212°F</h1>

```
/* Exercicio 5 */
import java.util.Scanner;
public class atividade_Cinco{

     public static void main(String []args){
        Scanner sc = new Scanner(System.in);
        
        double celsius, fahrenheit, conversor;
        
        System.out.println("Temperatura em Fahrenheit: ");
        fahrenheit = sc.nextDouble();
        
        celsius = (5.0 / 9.0) * (fahrenheit - 32);
        
        System.out.println("O valor em Graus Celsius: " + celsius);
     }
}

```




