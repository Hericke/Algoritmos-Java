# Algoritmos-Java
Estudos Algoritmos x Java
ALGORITMO X LINGUAGEM JAVA

BIBLIOTECAS
ALGORITMO	LINGUAGEM JAVA
	#import java.util.Scanner  //entrada e saída de dados

TIPOS DE DADOS
ALGORITMO	LINGUAGEM JAVA
literal	String
caracter	char
inteiro	int
real	float
real	double
	
	
DECLARAÇÃO DE VARIÁVEIS
ALGORITMO	LINGUAGEM JAVA
idade numerico	int idade;
preco numerico	float preco;
nome literal	String nome;
sexo literal	char sexo;
	
	
COMENTÁRIOS
ALGORITMO	LINGUAGEM JAVA
Delimitado por  /*  r */	Delimitado por /*    */
EX:	EX:
N1 numérico /*primeira nota*/	/* Isso é um comentário */
 	Se o comentário for em apenas uma linha pode-se usar //
 	EX: //comentário
OPERADORES ARITMÉTICOS
ALGORITMO	LINGUAGEM JAVA
Adição: +	+
Subtração: -	-
Multiplicação: *	*
Divisão: /  	/  
Resto: %	%
Atribuição: <-	=
 	Obs.: caso a divisão seja feita entre dois números inteiros o resultado será o quociente inteiro da divisão Ex.: RESULT = 5/2;      A variável RESULT receberá 2 e não 2.5
 	Se a resposta esperada é a divisão exata, ou seja, 2.5 precisa-se transformar um dos números em float Ex.: RESULT = 5f/2; ou RESULT = 5.0f/2; ou RESULT = (float)5/2;
OPERADORES RELACIONAIS
ALGORITMO	LINGUAGEM JAVA
Igual a: =	==
Diferente de: ≠ ou  <>	!=
Maior que: >	> 
Menor que: <	< 
Maior ou igual a: ≥	>=
Menor ou igual a: ≤	<=
	
OPERADORES LÓGICOS
ALGORITMO	LINGUAGEM JAVA
Conjunção:  e	&&
Disjunção: ou	||
Negação: não	!


COMANDOS DE ENTRADA DE DADOS
ALGORITMO	LINGUAGEM JAVA
Para fazer a entrada de dados através do prompt de comando o primeiro ato necessário é criar um objeto da classe Scanner, por isso recomenda-se que assim que iniciar o método main, escreva a seguinte linha de código que cria este objeto:                        Scanner leia = new Scanner(System.in);
idade inteiro	int idade;
preco real	float preco;
salario real	double salario;
nome literal	String nome;
sexo caracter	char sexo;
 	 
leia idade	idade = leia.nextInt();
leia preco	preco = leia.nextFloat();
leia salario	salario = leia.nextDouble();
leia nome	nome = leia.next(); //sem espaço em branco
leia sexo	sexo = leia.next().charAt(0);
 	 
Obs : Para fazer a leitura do nome com espaço em branco utilizando a classe Scanner utiliza-se a definição do delimitador de linha, como  sendo o enter repressentado na linguagem por "\n".  Para isso basta acrescentar logo após a linha de criação do objeto leia da classe Scanner a seguinte linha de comando:  leia.useDelimiter("\n"); 

COMANDOS DE SAÍDA DE DADOS
ALGORITMO	LINGUAGEM JAVA
escreva "Digite o salario:"	System.out.println("Digite o salário:");
escreva "O valor do salário atual:"	System.out.println("O valor do salário atual:"+salario);
escreva "O funcionário ", nome, " tem salário de R$", salario	System.out.println("O funcionário "+nome+" tem salário de R$"+salario);
escreva "O salario com aumento de 10% é ", salario+salario*0.10	System.out.println("O salario com aumento de 10% é "+(salario+salario*0.10));
Obs.: O comando de saída de dados System.out.println("Teste"), mostra a mensagem no video e pula uma linha no final, caso deseje mostrar a mensagem mas não pular uma linha no final usa-se System.out.print("Teste").  Além dos métodos println e print ainda podemos utilizar o comando printf que é herança da linguagem C, a vantagem de se utilizar o printf é a formatação para casas decimais na saída dos dados. Exemplo:

System.out.printf("O valor do salário atual:%.2f",salario);//será impresso o valor do salário com no máximo 2 casas decimais  O valor do salário atual:645.42 
Outros exemplos utilizando o printf:
 System.out.printf("O funcionário %s tem salarário de R$%.2f", nome, salario);
System.out.printf("O funcionario %s de sexo %s com o aumento terá novo salário de %.2f ",nome, sexo, salario+salario*0.10);
 System.out.printf("O funcionario %s tem idade de %d anos", nome, idade);


PRINCIPAIS FUNÇÕES MATEMÁTICAS
Math.PI	constante do valor PI
Math.abs(x)	Retorna o valor absoluto (módulo) do numero passado por parametro.
Math.ceil(x)	Arredonda um numero real para cima. Ex.: Math.ceil(3.7) é 4
Math.cos(x)	Calcula o cosseno de x . ( x deve estar representado em radiandos)
Math.exp(x)	Obtem o logarimo natural e elevado a x
Math.floor(x)	Arredonda um numero real para baixo. Ex.: Math.floor(3.7) é 3
Math.log(x)	Obtém o logaritmo natural de x.
Math.log10(x)	Obtém o logaritmo de base 10 de x.
Math.pow(x,y)	Calcula a potência de x elevado a y.
Math.sin(x)	Calcula o seno de x (x deve estar representado em radiandos)
Math.cbrt(x)	Calcula a raiz cúbica de x
Math.sqrt(x)	Calcula a raiz quadrada de x
Math.tan(x)	Calcula a tangente de x (x deve estar representado em radiandos)
Math.toDegress(x)	Converte a medida de x de radiandos para graus.
Math.toRadians(x)	Converte a medida de x de graus para radiandos.










ESTRUTURA DE DECISÃO OU CONDICIONAL - Se
ALGORITMO	LINGUAGEM JAVA
se (preco<100) então	if (preco<100) {
     novopreco = preco*1.10	   novopreco=preco*1.10
 	}
 	 
 	 
se (sexo = ‘F’) então	if (sexo == ‘F’) {
    qMulheres = qMulheres + 1	       qMulheres = qMulheres + 1
 	}
senão	else{
    qHomens = qHomens + 1	          qHomens = qHomens + 1
fimse	}
 	 
 	 
se (cor = “azul”) então	if (cor.equalsIgnoreCase("azul")){
     qAzul = qAzul + 1	    System.out.println("A cor é azul");
 	}
senão	else{
    se cor = “vermelho”  então	    if (cor.equalsIgnoreCase("vermelho")){
         qVermelho = qVermelho + 1	       System.out.println("A cor é vermelha");
 	    }
    senao	    else {
        qQualquer = qQualquer + 1]	       System.out.println("A cor não é azul e nem vermelha");
    fimse	    }
fimse	}
	
	






	
ESTRUTURA DE DECISÃO OU CONDICIONAL - ESCOLHA
ALGORITMO	LINGUAGEM JAVA
escolha (op)	switch (op)
inicio  	{
    caso 1:	    case 1:
        escreva "soma : ", a + b	        System.out.println("soma : "+( a + b));
        parar;	        break;
    case 2:	    case 2:
        escreva "subtração : ", a - b	        System.out.println("subtração : "+( a - b));
        parar;	        break;
    case 3:	    case 3:
        escreva "multiplicação : ", a * b	        System.out.println("multiplicação : "+( a * b));
        parar;	        break;
    padrão:	    default:
        escreva "divisão : ", a*1.0 / b	        System.out.println("divisão : "+( a*1.0/ b));
        parar;	        break;
fimescolha	}
	
	
	
ESTRUTURA DE REPETIÇÃO – ENQUANTO 	
ALGORITMO	LINGUAGEM JAVA
Algoritmo	int main(){
  raio, v numerico	  float raio, v;
  raio <-0;	  raio = 0;
  enquanto (raio <= 20) faça	  while (raio <= 20)  {
     v <- 4/3*3.14*raio^3	     v = 4/3*(float)3.14* (float)pow(raio, 3);
     escreva("Para raio:”, raio, “o volume é:", v)	     System.out.println("Para raio: " + raio + " o volume é: "+ v);     
     raio <- raio + 0.5;	     raio = raio + 0.5f;
  fimenquanto	  }
 	  system(“pause”);
fimalgoritmo	}
	

ESTRUTURA DE REPETIÇÃO – FAÇA  ENQUANTO	
ALGORITMO	LINGUAGEM JAVA
Algoritmo	int main(){
  raio, v numerico	  float raio, v;
  raio <- 0	  raio = 0;
  faça	  do {
     v <- 4/3*3.14*raio^3	     v = 4/3*(float)3.14* (float)pow(raio, 3);
     escreva("Para raio:”, raio, “o volume é:", v)	     System.out.println("Para raio: " + raio + " o volume é: "+ v);     
     raio <- raio + 0.5;	     raio = raio + 0.5f;
  enquanto (raio <= 20);	  }while(raio<20);
 	  System("pause");
fimalgoritmo	}
	
ESTRUTURA DE REPETIÇÃO – PARA	
ALGORITMO	LINGUAGEM PARA
Algoritmo	static void Main(string[] args){
    raio, v, cont numerico	  float raio, v;
  	  int cont;
    raio, v numerico	  raio=0;
    para cont de 0 até 40 passo 1 faça 	  for(cont=0; cont<=40; cont=cont+1)  {
       v <- 4.0/3*3.14*raio^3;	     v = 4.0/3*(float)3.14* (float)pow(raio, 3);
       escreva("Para raio:”, raio, “o volume é:", v);	     System.out.println("Para raio: " + raio + " o volume é: "+ v);     
       raio <- raio + 0.5;	     raio = raio + 0.5f;
    fimpara	  }
 	  System("pause");
fimalgoritmo	}
