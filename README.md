# Exercicios_Desenvolvimento_BD
17 exercícios da aula de desenvolvimento de banco de dados do dia 19/02/2025

<h1>1. Faça um algoritmo que leia a idade de uma pessoa expressa em anos, meses e dias e escreva a idade dessa pessoa expressa apenas em dias. Considerar ano com 365 dias e mês com 30 dias.</h1>


```java
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

```java
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
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `brancoPor = 0.0`, `nulosPor = 0.0`, `validosPor = 0.0` | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Número de Eleitores** | `eleitores = 1000`                 | O usuário digita o número total de eleitores, que é 1000. |
| **3. Entrada de Votos em Branco** | `branco = 200`                     | O usuário digita o número de votos em branco, que é 200. |
| **4. Entrada de Votos Nulos**  | `nulos = 150`                       | O usuário digita o número de votos nulos, que é 150.   |
| **5. Entrada de Votos Válidos**| `validos = 650`                      | O usuário digita o número de votos válidos, que é 650. |
| **6. Cálculo da Porcentagem de Votos em Branco** | `brancoPor = (200/1000) * 100 = 20.0` | O programa calcula a porcentagem de votos em branco: 200 / 1000 * 100 = 20.0%. |
| **7. Cálculo da Porcentagem de Votos Nulos**  | `nulosPor = (150/1000) * 100 = 15.0`  | O programa calcula a porcentagem de votos nulos: 150 / 1000 * 100 = 15.0%. |
| **8. Cálculo da Porcentagem de Votos Válidos**| `validosPor = (650/1000) * 100 = 65.0`  | O programa calcula a porcentagem de votos válidos: 650 / 1000 * 100 = 65.0%. |
| **9. Saída**                   | `brancoPor = 20.0`, `nulosPor = 15.0`, `validosPor = 65.0` | O programa exibe as porcentagens calculadas.          |



<h1>3.Escreva um algoritmo para ler o salário mensal atual de um funcionário e o percentual de reajuste. Calcular e escrever o valor do novo salário.</h1> 

```java
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
**## Execução Passo a Passo (Teste de Mesa):**
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `salario = 0.0`, `reajuste = 0.0`, `novoSalario = 0.0` | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Salário**      | `salario = 3000`                     | O usuário digita o salário de 3000.                     |
| **3. Entrada do Reajuste**     | `reajuste = 10`                      | O usuário digita o percentual de reajuste de 10%.      |
| **4. Cálculo do Novo Salário** | `novoSalario = 3000 * (1 + (10 / 100.0)) = 3000 * 1.1 = 3300.0` | O programa calcula o novo salário: 3000 * 1.1 = 3300.0.|
| **5. Saída**                   | `novoSalario = 3300.0`               | O programa imprime o novo salário com o reajuste.      |



<h1> 4. O custo de um carro novo ao consumidor é a soma do custo de fábrica com a porcentagem do distribuidor e dos impostos (aplicados ao custo de fábrica). Supondo que o percentual do distribuidor seja de 28% e os impostos de 45%, escrever um algoritmo para ler o custo de fábrica de um carro, calcular e escrever o custo final ao consumidor. </h1>

```java
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
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `custoFabrica = 0.0`, `precoFinal = 0.0`, `imposto = 45.0`, `distribuidor = 28.0` | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Custo de Fabrica** | `custoFabrica = 20000`              | O usuário digita o custo de fábrica de 20000.          |
| **3. Cálculo do Valor do Distribuidor** | `distribuidor = (20000 * 28.0 / 100) = 5600.0` | O programa calcula o valor do distribuidor: 20000 * 28% = 5600.0. |
| **4. Cálculo do Imposto**     | `imposto = (20000 * 45.0 / 100) = 9000.0` | O programa calcula o valor do imposto: 20000 * 45% = 9000.0. |
| **5. Cálculo do Preço Final** | `precoFinal = 5600.0 + 9000.0 + 20000 = 35600.0` | O programa calcula o preço final do carro: 5600 + 9000 + 20000 = 35600.0. |
| **6. Saída**                   | `distribuidor = 5600.0`, `imposto = 9000.0`, `precoFinal = 35600.0` | O programa exibe os valores calculados.               |






<h1>5. Uma revendedora de carros usados paga a seus funcionários vendedores um salário fixo por mês, mais uma comissão também fixa para cada carro vendido e mais 5% do valor das vendas por ele efetuadas. Escrever um algoritmo que leia o número de carros por ele vendidos, o valor total de suas vendas, o salário fixo e o valor que ele recebe por carro vendido. Calcule e escreva o salário final do vendedor.</h1>


```java
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
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                             | Descrição                                              |
|-------------------------------|---------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `salarioFixo = 0.0`, `salarioFinal = 0.0`, `comissaoFixa = 0.0`, `comissaoTotal = 0.0`, `valorVenda = 0.0`, `carrosVendidos = 0` | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Salário Fixo** | `salarioFixo = 1500.0`                | O usuário digita o salário fixo como 1500.0.            |
| **3. Entrada do Valor da Venda** | `valorVenda = 20000.0`               | O usuário digita o valor de venda de cada carro, 20000.0. |
| **4. Entrada do Número de Carros Vendidos** | `carrosVendidos = 5`            | O usuário digita o número de carros vendidos como 5.     |
| **5. Cálculo da Comissão Fixa** | `comissaoFixa = 0.05 * 20000.0 = 1000.0` | O programa calcula a comissão fixa: 0.05 * 20000 = 1000.0. |
| **6. Cálculo da Comissão Total** | `comissaoTotal = 1000.0 * 5 = 5000.0` | O programa calcula a comissão total: 1000 * 5 = 5000.0. |
| **7. Cálculo do Salário Final** | `salarioFinal = 1500.0 + 5000.0 = 6500.0` | O programa calcula o salário final: 1500 + 5000 = 6500.0. |
| **8. Saída**                   | `salarioFinal = 6500.0`               | O programa exibe o salário final como 6500.0.            |



<h1>6. Escreva um algoritmo para ler uma temperatura em graus Fahrenheit, calcular e escrever o valor correspondente em graus Celsius. Observação: Para testar se a sua resposta está correta saiba que 100°C = 212°F</h1>

```java
/* Exercicio 6 */
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

## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                             | Descrição                                              |
|-------------------------------|---------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `celsius = 0.0`, `fahrenheit = 0.0`, `conversor = 0.0` | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada da Temperatura em Fahrenheit** | `fahrenheit = 98.6`            | O usuário digita a temperatura em Fahrenheit, 98.6.     |
| **3. Cálculo da Temperatura em Celsius** | `celsius = (5.0 / 9.0) * (98.6 - 32) = (5.0 / 9.0) * 66.6 = 37.0` | O programa converte a temperatura para Celsius: (5 / 9) * (98.6 - 32) = 37.0. |
| **4. Saída**                   | `celsius = 37.0`                     | O programa exibe o valor convertido para Celsius como 37.0. |


<h1>7. Ler um valor e escrever a mensagem É MAIOR QUE 10! se o valor lido for maior que 10, caso contrário escrever NÃO É MAIOR QUE 10! </h1>


```java
import java.util.Scanner;

public class Questao7 {
	public static void main(String[] args) {
		
		//Ler um valor e escrever a mensagem É MAIOR QUE 10! se o valor lido for maior que 10, 
//		caso contrário escrever NÃO É MAIOR QUE 10! 
		
		Scanner entrada = new Scanner(System.in);
		
		System.out.println("Insira um valor: ");
		int num = entrada.nextInt();
		if(num>10) {
			String mensagem = "É MAIOR QUE 10!";
			System.out.println(mensagem);
		}
		else {
			String mensagem = "NÃO É MAIOR QUE 10!";
			System.out.println(mensagem);
		}
		entrada.close();
	}

}
```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `num = 0`, `mensagem = ""`           | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Valor**       | `num = 15`                           | O usuário digita o valor 15.                           |
| **3. Verificação da Condição** | `num > 10`                           | O valor de `num` é maior que 10.                       |
| **4. Saída**                   | `mensagem = "É MAIOR QUE 10!"`       | O programa exibe "É MAIOR QUE 10!".                   |



<h1>8. Ler um valor e escrever se é positivo ou negativo (considere o valor zero como positivo). </h1>


```java

import java.util.Scanner;

public class Questao8 {

	public static void main(String[] args) {
//		Ler um valor e escrever é positivo ou negativo (considere o valor zero como positivo)
		Scanner entrada = new Scanner(System.in);
		
		System.out.println("Insira um valor: ");
		int num = entrada.nextInt();	
		if(num>=0){
			String mensagem = "Número positivo!" ;
			System.out.println(mensagem);		
		}else {
			String mensagem = "Número negativo!";
			System.out.println(mensagem);
		}
		entrada.close();
	}
}
```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `num = 0`, `mensagem = ""`           | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Valor**       | `num = 5`                            | O usuário digita o valor 5.                            |
| **3. Verificação da Condição** | `num >= 0`                           | O valor de `num` é maior ou igual a 0 (positivo).      |
| **4. Saída**                   | `mensagem = "Número positivo!"`      | O programa exibe "Número positivo!".                   |


<h1>9. As maçãs custam R$ 1,30 cada se forem compradas menos de uma dúzia, e R$ 1,00 se forem compradas pelo menos doze. Escreva um programa que leia o número de maçãs compradas, calcule e escreva o custo total da compra.</h1>


```java
import java.util.Scanner;

public class Questao9 {

	public static void main(String[] args) {
//		Ler um valor e escrever é positivo ou negativo (considere o valor zero como positivo)
		Scanner entrada = new Scanner(System.in);
		
		System.out.println("Insira um valor: ");
		int num = entrada.nextInt();	
		if(num>=0){
			String mensagem = "Número positivo!" ;
			System.out.println(mensagem);		
		}else {
			String mensagem = "Número negativo!";
			System.out.println(mensagem);
		}
		entrada.close();
	}
}


```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                            | Descrição                                              |
|-------------------------------|--------------------------------------|--------------------------------------------------------|
| **1. Inicialização**           | `num = 0`, `mensagem = ""`           | O código começa com todas as variáveis inicializadas.  |
| **2. Entrada do Valor**       | `num = 10`                           | O usuário digita o valor 10.                            |
| **3. Verificação da Condição** | `num >= 0`                           | O valor de `num` é maior ou igual a 0 (positivo).      |
| **4. Saída**                   | `mensagem = "Número positivo!"`      | O programa exibe "Número positivo!".                   |




<h1>10. Ler as notas da 1a. e 2a. avaliações de um aluno. Calcular a média aritmética simples e escrever uma mensagem que diga se o aluno foi ou não aprovado (considerar que nota igual ou maior que 6 o aluno é aprovado). Escrever também a média calculada.</h1>

```java
import java.util.Scanner;

public class Questao10 {
	
	public static void main(String[] args) {
//		LER AS NOTAS DA 1A. E 2A. AVALIAÇÕES DE UM ALUNO. 
//		CALCULAR A MÉDIA ARITMÉTICA SIMPLES E ESCREVER UMA 
//		MENSAGEM QUE DIGA SE O ALUNO FOI OU NÃO APROVADO 
//		(CONSIDERAR QUE NOTA IGUAL OU MAIOR QUE 6 O ALUNO É APROVADO). 
//		ESCREVER TAMBÉM A MÉDIA CALCULADA. 
		Scanner entrada = new Scanner(System.in);
		System.out.println("Insira a sua primeira nota: ");
		double nota1 = entrada.nextDouble();
		entrada.nextLine();
		
		System.out.println("Insira a sua segunda nota: ");
		double nota2 = entrada.nextDouble();
		entrada.nextLine();
		String mensagem;
		double media = (nota1 + nota2)/2;
		if(media >= 6){
			System.out.println("-----------------------");
			mensagem = "O aluno foi Aprovado!";
			System.out.printf("Sua média é: %.1f %n", media );
			System.out.println(mensagem);
		}else {
			System.out.println("-----------------------");
			mensagem = "O aluno não foi Aprovado!";
			System.out.printf("Sua média é: %.1f %n", media );
			System.out.println(mensagem);
		}
		entrada.close();
	
	} 
}
```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                             | Descrição                                                |
|-------------------------------|---------------------------------------|----------------------------------------------------------|
| **1. Inicialização**           | `nota1 = 0`, `nota2 = 0`, `media = 0`, `mensagem = ""` | O código começa com todas as variáveis inicializadas.    |
| **2. Entrada da Primeira Nota**| `nota1 = 7.5`                        | O usuário digita a primeira nota: 7.5                    |
| **3. Entrada da Segunda Nota** | `nota2 = 8.0`                        | O usuário digita a segunda nota: 8.0                     |
| **4. Cálculo da Média**        | `media = (7.5 + 8.0) / 2 = 7.75`     | A média é calculada como (7.5 + 8.0) / 2 = 7.75          |
| **5. Condição de Aprovação**   | `media = 7.75`                       | A média é maior que 6, então o aluno é aprovado.         |
| **6. Saída**                   | `mensagem = "O aluno foi Aprovado!"` | A mensagem de aprovação é gerada e exibida: "O aluno foi Aprovado!" |
| **7. Exibição da Média**       | `media = 7.75`                       | O programa exibe "Sua média é: 7.8" (arredondado)         |
| **8. Exibição da Mensagem**    | `mensagem = "O aluno foi Aprovado!"` | A mensagem de aprovação é exibida após a média.           |



<h1>11. Ler o ano atual e o ano de nascimento de uma pessoa. Escrever uma mensagem que diga se ela poderá ou não votar este ano (não é necessário considerar o mês em que a pessoa nasceu).</h1>

```java

import java.util.Scanner;

public class Votacao {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Obtendo o ano atual
        int anoAtual = 2025;

        // Solicita o ano de nascimento da pessoa
        System.out.print("Digite seu ano de nascimento: ");
        int anoNascimento = scanner.nextInt();

        // Calcula a idade
        int idade = anoAtual - anoNascimento;

        // Verifica se a pessoa pode votar
        if (idade >= 16) {
            System.out.println("Você tem " + idade + " anos e pode votar este ano!");
        } else {
            System.out.println("Você tem " + idade + " anos e não pode votar este ano.");
        }

        scanner.close();
    }
}

```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                    | Descrição                                                   |
|-------------------------------|------------------------------|-------------------------------------------------------------|
| **1. Inicialização**           | `anoAtual = 2025`, `anoNascimento = 0`, `idade = 0` | O código começa com as variáveis `anoAtual` e `anoNascimento` inicializadas. |
| **2. Entrada do Ano de Nascimento** | `anoNascimento = 2005`      | O usuário digita 2005 como ano de nascimento.              |
| **3. Cálculo da Idade**        | `idade = 2025 - 2005 = 20`   | O cálculo da idade é feito: 2025 - 2005 = 20.               |
| **4. Verificação de Votação**  | `idade = 20`                 | A idade é maior ou igual a 16, então a pessoa pode votar.   |
| **5. Saída**                   | `"Você tem 20 anos e pode votar este ano!"` | O programa exibe que a pessoa tem 20 anos e pode votar.     |


<h1>12. Ler dois valores (considere que não serão lidos valores iguais) e escrever o maior deles.</h1>

```java
import java.util.Scanner;

public class MaiorValor {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita o primeiro valor
        System.out.print("Digite o primeiro valor: ");
        int valor1 = scanner.nextInt();

        // Solicita o segundo valor
        System.out.print("Digite o segundo valor: ");
        int valor2 = scanner.nextInt();

        // Verifica e imprime o maior valor
        if (valor1 > valor2) {
            System.out.println("O maior valor é: " + valor1);
        } else {
            System.out.println("O maior valor é: " + valor2);
        }

        scanner.close();
    }
}

```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                    | Descrição                                                   |
|-------------------------------|------------------------------|-------------------------------------------------------------|
| **1. Inicialização**           | `valor1 = 10`, `valor2 = 5`   | O código começa com as variáveis `valor1` e `valor2` inicializadas. |
| **2. Entrada do Primeiro Valor** | `valor1 = 10`               | O usuário digita 10 como o primeiro valor.                 |
| **3. Entrada do Segundo Valor** | `valor2 = 5`                | O usuário digita 5 como o segundo valor.                   |
| **4. Comparação**              | `valor1 > valor2`            | O programa compara os valores: 10 > 5.                     |
| **5. Saída**                   | `"O maior valor é: 10"`      | O programa imprime que o maior valor é 10.                 |


<h1>13.  Ler dois valores (considere que não serão lidos valores iguais) e escrevê-los em ordem crescente. </h1>

```java
import java.util.Scanner;

public class OrdemCrescente {
    public static void main(String[] args) {
        // Inicializando o Scanner para leitura de dados
        Scanner scanner = new Scanner(System.in);

        // Solicita o primeiro valor
        System.out.print("Digite o primeiro valor: ");
        int valor1 = scanner.nextInt();

        // Solicita o segundo valor
        System.out.print("Digite o segundo valor: ");
        int valor2 = scanner.nextInt();

        // Verifica qual valor é o menor e imprime em ordem crescente
        if (valor1 < valor2) {
            System.out.println("Ordem crescente: " + valor1 + ", " + valor2);
        } else {
            System.out.println("Ordem crescente: " + valor2 + ", " + valor1);
        }

        scanner.close();
    }
}



```
## Execução Passo a Passo (Teste de Mesa):
| Passo                         | Variáveis                    | Descrição                                                   |
|-------------------------------|------------------------------|-------------------------------------------------------------|
| **1. Inicialização**           | `valor1 = 7`, `valor2 = 12`   | O código começa com as variáveis `valor1` e `valor2` inicializadas. |
| **2. Entrada do Primeiro Valor** | `valor1 = 7`               | O usuário digita 7 como o primeiro valor.                 |
| **3. Entrada do Segundo Valor** | `valor2 = 12`               | O usuário digita 12 como o segundo valor.                 |
| **4. Comparação**              | `valor1 < valor2`            | O programa compara os valores: 7 < 12.                     |
| **5. Saída**                   | `"Ordem crescente: 7, 12"`   | O programa imprime os valores em ordem crescente: 7, 12.   |


<h1>14.  Ler a hora de início e a hora de fim de um jogo de Xadrez (considere apenas horas inteiras, sem os minutos) e calcule a duração do jogo em horas, sabendo-se que o tempo máximo de duração do jogo é de 24 horas e que o jogo pode iniciar em um dia e terminar no dia seguinte.</h1>

```java
import java.util.Scanner;

public class DuracaoJogoXadrez {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        // Solicita a hora de início e a hora de fim
        System.out.print("Digite a hora de início do jogo: ");
        int horaInicio = scanner.nextInt();

        System.out.print("Digite a hora de fim do jogo: ");
        int horaFim = scanner.nextInt();

        // Calcula a duração do jogo
        int duracao;
        if (horaFim > horaInicio) {
            duracao = horaFim - horaInicio;
        } else {
            // Caso o jogo termine no dia seguinte
            duracao = (24 - horaInicio) + horaFim;
        }

        // Exibe a duração do jogo
        System.out.println("A duração do jogo foi de " + duracao + " horas.");

        scanner.close();
    }
}


```
## Execução Passo a Passo (Teste de Mesa):

| Passo                         | Variáveis                     | Descrição                                                   |
|-------------------------------|-------------------------------|-------------------------------------------------------------|
| **1. Inicialização**           | `horaInicio = 10`, `horaFim = 14`, `duracao = ?` | O código começa com as variáveis `horaInicio` e `horaFim` inicializadas. |
| **2. Entrada da Hora de Início** | `horaInicio = 10`             | O usuário digita 10 como a hora de início.                 |
| **3. Entrada da Hora de Fim**  | `horaFim = 14`                | O usuário digita 14 como a hora de fim.                    |
| **4. Comparação**              | `horaFim > horaInicio`        | O programa compara `horaFim` e `horaInicio`.                |
| **5. Cálculo da Duração**     | `duracao = horaFim - horaInicio = 14 - 10 = 4` | O programa calcula a duração do jogo como 4 horas.         |
| **6. Saída**                   | `duracao = 4`                 | O programa exibe a duração do jogo: 4 horas.               |


<h1>15. A jornada de trabalho semanal de um funcionário é de 40 horas. O funcionário que trabalhar mais de 40 horas receberá hora extra, cujo cálculo é o valor da hora regular com um acréscimo de 50%. Escreva um algoritmo que leia o número de horas trabalhadas em um mês, o salário por hora e escreva o salário total do funcionário, que deverá ser acrescido das horas extras, caso tenham sido trabalhadas (considere que o mês possua 4 semanas exatas). </h1>


```java
import java.util.Scanner;

public class CalculoSalario {
    public static void main(String[] args) {
        // Criar scanner para leitura de dados
        Scanner scanner = new Scanner(System.in);
        
        // Leitura dos dados
        System.out.print("Digite o número de horas trabalhadas no mês: ");
        double horasTrabalhadas = scanner.nextDouble();
        
        System.out.print("Digite o valor do salário por hora: ");
        double salarioPorHora = scanner.nextDouble();
        
        // Cálculo do total de horas regulares no mês
        double horasRegulares = 40 * 4;  // 4 semanas de 40 horas
        
        // Cálculo do salário regular (sem horas extras)
        double salarioRegular = horasRegulares * salarioPorHora;
        
        // Cálculo das horas extras, se houver
        double horasExtras = 0;
        double salarioExtra = 0;
        
        if (horasTrabalhadas > horasRegulares) {
            horasExtras = horasTrabalhadas - horasRegulares;
            salarioExtra = horasExtras * salarioPorHora * 1.5;  // 50% de acréscimo
        }
        
        // Cálculo do salário total
        double salarioTotal = salarioRegular + salarioExtra;
        
        // Exibição do resultado
        System.out.printf("Salário regular: R$ %.2f\n", salarioRegular);
        System.out.printf("Horas extras: %.0f horas\n", horasExtras);
        System.out.printf("Salário extra: R$ %.2f\n", salarioExtra);
        System.out.printf("Salário total: R$ %.2f\n", salarioTotal);
        
        // Fechar o scanner
        scanner.close();
    }
}


```
## Execução Passo a Passo (Teste de Mesa):
| Passo                           | Variáveis                         | Descrição                                                   |
|-----------------------------------|-----------------------------------|-------------------------------------------------------------|
| **1. Inicialização**              | `horasTrabalhadas = 160`, `salarioPorHora = 15`, `horasRegulares = 160`, `salarioRegular = ?`, `horasExtras = 0`, `salarioExtra = 0`, `salarioTotal = ?` | O código começa com as variáveis inicializadas com 160 horas trabalhadas e um salário de 15 reais por hora. |
| **2. Entrada das Horas Trabalhadas** | `horasTrabalhadas = 160`           | O usuário digita 160 horas trabalhadas no mês.              |
| **3. Entrada do Salário por Hora** | `salarioPorHora = 15`             | O usuário digita que o salário por hora é 15 reais.         |
| **4. Cálculo do Salário Regular**  | `salarioRegular = 160 * 15 = 2400` | O programa calcula o salário regular (sem horas extras).    |
| **5. Verificação de Horas Extras** | `horasTrabalhadas <= horasRegulares` | Como o número de horas trabalhadas é igual ao número de horas regulares, não há horas extras. |
| **6. Cálculo das Horas Extras**   | `horasExtras = 0`, `salarioExtra = 0` | O programa determina que não houve horas extras.            |
| **7. Cálculo do Salário Total**   | `salarioTotal = salarioRegular + salarioExtra = 2400 + 0 = 2400` | O programa calcula o salário total.                         |
| **8. Saída**                      | `salarioRegular = 2400`, `horasExtras = 0`, `salarioExtra = 0`, `salarioTotal = 2400` | O programa exibe o salário regular, horas extras, salário extra e salário total. |



<h1>16. Na empresa em que trabalhamos, há tabelas com o gasto de cada mês. Para fechar o balanço do primeiro trimestre, precisamos somar o gasto total. Sabendo que, em janeiro, foram gastos 15 mil reais, em fevereiro, 23 mil reais e, em março, 17 mil reais, faça um programa que calcule e imprima a despesa total no trimestre e a média mensal de gastos.</h1>

```java

public class DespesaTrimestral {
    public static void main(String[] args) {
        // Valores dos gastos de cada mês
        double janeiro = 15000;  // Gasto em janeiro
        double fevereiro = 23000;  // Gasto em fevereiro
        double marco = 17000;  // Gasto em março
        
        // Cálculo da despesa total no trimestre
        double despesaTotal = janeiro + fevereiro + marco;
        
        // Cálculo da média mensal de gastos
        double mediaMensal = despesaTotal / 3;
        
        // Exibição do resultado
        System.out.printf("Despesa total no trimestre: R$ %.2f\n", despesaTotal);
        System.out.printf("Média mensal de gastos: R$ %.2f\n", mediaMensal);
    }
}


```
## Execução Passo a Passo (Teste de Mesa):
| Passo                           | Variáveis                         | Descrição                                                   |
|-----------------------------------|-----------------------------------|-------------------------------------------------------------|
| **1. Inicialização**              | `janeiro = 15000`, `fevereiro = 23000`, `marco = 17000`, `despesaTotal = ?`, `mediaMensal = ?` | O código começa com as variáveis de gastos para os três meses. |
| **2. Cálculo da Despesa Total**  | `despesaTotal = janeiro + fevereiro + marco = 15000 + 23000 + 17000 = 55000` | O programa calcula a despesa total no trimestre (soma dos três meses). |
| **3. Cálculo da Média Mensal**   | `mediaMensal = despesaTotal / 3 = 55000 / 3 = 18333.33` | O programa calcula a média mensal de gastos, dividindo a despesa total por 3. |
| **4. Saída**                      | `despesaTotal = 55000`, `mediaMensal = 18333.33` | O programa exibe a despesa total e a média mensal.           |


<h1>17. Programa que leia as notas e calcule a média de LP1 deste semestre, referente a um determinado aluno.</h1>


```java

import java.util.Scanner;

public class CalculoMediaLP1 {
    public static void main(String[] args) {
        // Criação do scanner para leitura dos dados
        Scanner scanner = new Scanner(System.in);

        // Leitura das notas
        System.out.print("Digite a nota da primeira prova: ");
        double nota1 = scanner.nextDouble();

        System.out.print("Digite a nota da segunda prova: ");
        double nota2 = scanner.nextDouble();

        System.out.print("Digite a nota do trabalho: ");
        double trabalho = scanner.nextDouble();

        // Cálculo da média
        double media = (nota1 + nota2 + trabalho) / 3;

        // Exibição do resultado
        System.out.printf("A média de LP1 é: %.2f\n", media);

        // Fechar o scanner
        scanner.close();
    }
}


```
## Execução Passo a Passo (Teste de Mesa):
| Passo                           | Variáveis                         | Descrição                                                   |
|-----------------------------------|-----------------------------------|-------------------------------------------------------------|
| **1. Inicialização**              | `nota1 = ?`, `nota2 = ?`, `trabalho = ?`, `media = ?` | O código começa com as variáveis de notas e o cálculo da média. |
| **2. Leitura da Nota 1**         | `nota1 = 7.0`                     | O usuário digita a nota da primeira prova (nota1 = 7.0).     |
| **3. Leitura da Nota 2**         | `nota2 = 8.5`                     | O usuário digita a nota da segunda prova (nota2 = 8.5).      |
| **4. Leitura da Nota do Trabalho** | `trabalho = 9.0`                 | O usuário digita a nota do trabalho (trabalho = 9.0).        |
| **5. Cálculo da Média**          | `media = (7.0 + 8.5 + 9.0) / 3 = 8.17` | A média das três notas é calculada: `(7.0 + 8.5 + 9.0) / 3`. |
| **6. Saída**                     | `media = 8.17`                    | O programa exibe a média calculada: `8.17`.                 |
