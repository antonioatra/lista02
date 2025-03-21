# lista02 - Antônio Augusto

1) Considere o seguinte código JavaScript:

//EX01
let x = 17
let y = 5
let z = 8

resultadoBooleano =  (x < y) && (z > x) || (x - y > z)
console.log(resultadoBooleano)

const listaDeNumeros = [1, 2, 3, 4, 5];
let soma = 0;

for (let i = 0; i < listaDeNumeros.length; i++) {
  soma += listaDeNumeros[i];
}

console.log("A soma dos números é:", soma);
Qual das seguintes alternativas melhor descreve o que o código faz?

A) O código avalia a expressão booleana, imprime o resultado false, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

B) O código avalia a expressão booleana, imprime o resultado true, calcula a soma dos números de 1 a 5 e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime o resultado true e verifica se o número 5 está presente na lista de números.

D) O código avalia a expressão booleana, imprime o resultado false e ordena a lista de números em ordem crescente.

Resposta> Letra B -> A variável resultadoBooleano avalia a condição que é da e verifica se uma das duas condições é verdadeira, como a segunda é verdadeira ele imprime true na tela. No segundo caso da listaDeNumeros é declarado um array e uma variável de soma que recebe os valores de cada número da listaDeNumeros e soma eles pelo uso de += e imprime na tela o resultado.

2) Analise as funções calcularOrcamento() e calcularOrcamento2(). Num cenário em que a lista gastos fosse incializada como var gastos = [3600, 950, 620, 38] em ambas funções.

//Versão 1 da função que calcula orçamento
function calculaOrcamento(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var saldo = 0; 
    var statusSaldo =  'positivo';
    var i = 1;

    do{
        totalGastos += gastos[i];
        i++;
    } while(salario >= totalGastos && i<gastos.length)
    
    saldo = salario - totalGastos;

    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
//Versão 2 da função que calcula orçamento
function calculaOrcamento2(){

    var gastos = [1800, 950, 620, 38];
    var totalGastos = gastos[0];
    var salario = 3500;
    var statusSaldo =  'positivo';
    var saldo = 0;
    var i = 1;

    while(salario >= totalGastos && i<gastos.length){
        totalGastos += gastos[i];
        i++;
    }

    saldo = salario - totalGastos;
    if (saldo < 0 ){
        statusSaldo = 'negativo';
    } 
    console.log (`Seu saldo é ${statusSaldo} de ${saldo}. `);
}
Escolha a opção que responde corretamente qual seria a saída após a execução de cada função:

A) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -1050.'

B) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -1050.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -100.'

C) A saída de calcularOrcamento() seria: 'Seu saldo é negativo de -100.' e a de calcularOrcamento2() seria: 'Seu saldo é negativo de -1050.'

D) As funções calcularOrcamento() e calcularOrcamento2() teriam a mesma saída: 'Seu saldo é negativo de -100.'

Resposta: Letra B -> O primeiro caso faz o que deve ser feito dentro 'do' antes de avaliar a condição, então, o saldo já começa negativa -100 mas depois vai e diminiu 950 resultando em -1050. No segundo caso ele avalia a condição primeiro então como o saldo já começa negativo ele não fará o que está dentro do 'do', resultando no valor que já estava que era de -100
3) Considere o seguinte trecho de código em JavaScript:

//EX03
const numero = 10;

if (numero % 2 === 0) {
  console.log("O número é par!");
} else if (numero % 3 === 0) {
  console.log("O número é divisível por 3!");
} else {
  console.log("O número é ímpar e não é divisível por 3!");
}
Qual das seguintes alternativas é a descrição mais precisa do que o código faz?

A) O código verifica se o número é divisível por 3 e, se for, exibe a mensagem "O número é divisível por 3!".

B) O código verifica se o número é par ou ímpar. Se for par, exibe a mensagem "O número é par!". Se for ímpar, exibe a mensagem "O número é ímpar!".

C) O código verifica se o número é par, ímpar ou divisível por 3. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3, exibe a mensagem "O número é divisível por 3!". Se for ímpar, exibe a mensagem "O número é ímpar e não é divisível por 3!".

D) O código verifica se o número é par, se é divisível por 3 ou se é ímpar. Se for par, exibe a mensagem "O número é par!". Se for divisível por 3 (e não for par), exibe a mensagem "O número é divisível por 3!". Se for ímpar (e não for divisível por 3), exibe a mensagem "O número é ímpar e não é divisível por 3!".

Resposta: Letra D -> O uso de 'if' e 'else if' cria varias condições que são avaliadas em ordem, caso a primeira seja verdadeira ele não lê as outras, caso contrário irá ser avaliada as outras condições até ser verdadeiro ou chegar no 'else' e rodar o que está nele, então, nessse caso ele irá avaiar se o número o número é par ou não, caso ele não seja par irá ser avaliada a condição de que se ele é devisível por 3 só que apenas os ímpares já que ele não entra na condição de par, caso ele também não seja um número ímpar e divisível por 3 ele entrará na condição do else.

4) Qual será o resultado impresso no console após a execução desse código?

//EX04
var saldo = 1000;
var limiteCredito = 500;
var valorCompras = [200, 800, 300, 400, 600];

for (var i = 0; i < valorCompras.length; i++) {
    var valorCompra = valorCompras[i];

    if (valorCompra <= saldo) {
        console.log("Compra " + (i+1) + " aprovada. Saldo restante: " + (saldo - valorCompra));
        saldo -= valorCompra;
    } else if (valorCompra <= saldo + limiteCredito) {
        console.log("Compra " + (i+1) + " aprovada com limite de crédito. Saldo restante: " + ((saldo + limiteCredito) - valorCompra));
        saldo = 0;
        limiteCredito -= (valorCompra - saldo);
    } else {
        console.log("Compra " + (i+1) + " negada. Saldo insuficiente e limite de crédito excedido.");
    }
}
Escolha a opção que responde corretamente:

A) Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 aprovada com limite de crédito. Saldo restante: 0

Compra 5 aprovada. Saldo restante: -200

B) Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

C) Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada com limite de crédito. Saldo restante: 700

Compra 3 aprovada. Saldo restante: 400

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

D)

Compra 1 aprovada. Saldo restante: 800

Compra 2 aprovada. Saldo restante: 0

Compra 3 aprovada com limite de crédito. Saldo restante: 200

Compra 4 negada. Saldo insuficiente e limite de crédito excedido.

Compra 5 negada. Saldo insuficiente e limite de crédito excedido.

Resposta: Letra D -> O primeiro caso com a compra de 200 e ele tem um saldo de 1000 então a compra é aprovada e sobra 800, no segundo caso ele tem um saldo de 800 e a compra é de 800 então a compra é aprovada e sobra 0, no terceiro caso o saldo n cobre o valor de 300 mas ele tem  o limite de crédito de 500 então  sobra 200 do limite de crédito, já nos outros dois últimos caso ele não tem saldo e nem crédito suficiente para fazer nenhuma compra

5) Qual é o principal ciclo de vida de um jogo em Phaser.js?

Escolha a opção que responde corretamente:

A) Setup -> Update -> Draw

B) Preload -> Create -> Update

C) Load -> Initialize -> Render

D) Begin -> Play -> End

Resposta: Letra B -> Os jogos nos Phaser são baseados em 3 ciclos: preload, create e update. O primeiro adiciona as imagens que você quer que tenha no jogo, o criate carrega essas imagens dentro do jogo de acordo com as características que você passa, já o update carrega ações repetidas vezes dentro do jogo

6) Qual é o objetivo principal do módulo Arcade Physics em Phaser.js?

Escolha a opção que responde corretamente:

A) Renderizar gráficos 3D para jogos em HTML5.

B) Simular interações físicas realistas, como colisões e movimentos, em jogos 2D.

C) Criar efeitos de áudio para melhorar a experiência do usuário em jogos.

D) Gerenciar a lógica do jogo e a sincronização de eventos em jogos multiplayer.

Resposta: Letra B -> Arcade Physics é um módulo que como o nome diz é sobre a interação de física dentro do jogo.

Questões dissertativas
7) Implemente o pseudocódigo para o algoritmo representado no fluxograma da imagem. 
```

Pedidos abaixo de R$50,00 → "Frete não disponível!"

Pedidos entre R$50,00 e R$199,99 (inclusive) → "Frete com custo adicional!"

Pedidos de R$200,00 ou mais → "Frete grátis!"
```
Implemente um pseudocódigo que receba o valor total da compra e exiba a classificação correta do frete para o cliente.

Resposta:

```
function retornarFrete(total){

    if(total < 50)
    {
        return "Frete não disponível!"
    }
    else if(total>=50 && total < 200)
    {
        return "Frete com custo adicional"
    }
    else 
    {
        return "Frete grátis"
    }
}

```			 

8) Considere a implementação da classe base FormaGeometrica em um sistema de modelagem de formas geométricas. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Retangulo e Circulo, que herdam da classe FormaGeometrica, adicionando atributos específicos e métodos para calcular a área de um retângulo e de um círculo, respectivamente.

Classe FormaGeometrica:
    Atributos:
        - cor

    Método Construtor(cor):
        Define o valor do atributo cor com o valor passado como parâmetro.

    Método CalcularArea():
        # Implementação genérica para cálculo de área, a ser sobrescrita pelas subclasses.

Resposta: 
```
class FormaGeometrica{
    
    calcularArea(){
        console.log("Calculando área")
    }

}

class Circulo extends FormaGeometrica{
    constructor(raio){
        super()
        this.raio = raio
    }

    calcularArea(){
        return 3.14*this.raio*this.raio
    }
}

class Retangulo extends FormaGeometrica{
    constructor(base, altura){
        super()
        this.base = base 
        this.altura = altura
    }

    calcularArea(){
        return this.base*this.altura
    }
}

```

9) Você foi contratado(a) como estagiário(a) da Tesla e está participando do desenvolvimento de um programa para simular o desempenho de um carro elétrico em uma corrida. Seu objetivo é determinar em quantos minutos o carro levará para completar uma determinada distância, levando em consideração uma velocidade inicial e uma taxa de aceleração constante. No entanto, você deseja garantir que o carro não exceda uma velocidade máxima nem que a corrida demore mais do que um tempo máximo. Implemente a lógica dessa simulação em pseudocódigo.

Considere a fórumla de atualização velocidade:

    velocidade = velocidadeInicial + aceleracao*tempo

 
	classe Tesla:
		Atributos:
			-velocidadeInicial
			-aceleracao

			-distancia
Respota:
```
class Tesla{
    constructor(velocidadeInicial, aceleracao, distancia, tempo, velocidadeMaxima, tempoMaximo, distanciaPercorrida){
        this.velocidadeInicial = velocidadeInicial,
        this.aceleracao = aceleracao,
        this.distancia = distancia,
        this.tempo = tempo
        this.velocidadeMaxima = velocidadeMaxima 
        this.tempoMaximo = tempoMaximo
        this.distanciaPercorrida = 0
    }

    calcularTempo(){
        while(this.distanciaPercorrida < this.distancia && this.tempo < this.tempoMaximo) //avalia a condição de distância e tempo
        {
            this.distanciaPercorrida += this.velocidadeInicial
            this.velocidadeInicial += this.aceleracao 
            this.tempo ++

            if(this.velocidadeInicial > this.velocidadeMaxima)
            {
                this.velocidadeInicial = this.velocidadeMaxima //não deixa ultrapassar a velocidade máxima
            }
        }
            return this.tempo

    }
}
```	
10) Uma matriz é uma coleção bidimensional de elementos, organizados em linhas e colunas. A seguir, é fornecida a implementação da função SomaDeMatrizes(matrizA, matrizB), que calcula a soma de duas matrizes. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação de duas matrizes.

Função SomaDeMatrizes(matrizA, matrizB):
    # Verifica se as duas matrizes têm o mesmo número de linhas e colunas
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."
    Senão:
        linhas <- tamanho(matrizA)
        colunas <- tamanho(matrizA[0]) # Considerando que todas as linhas têm o mesmo número de colunas
        matrizResultado <- novaMatriz(linhas, colunas)

        # Loop para percorrer cada elemento das matrizes e calcular a soma
        Para i de 0 até linhas-1 faça:
            Para j de 0 até colunas-1 faça:
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]

        Retornar matrizResultado

# Exemplo de uso da função
matrizA <- [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
matrizB <- [[9, 8, 7], [6, 5, 4], [3, 2, 1]]

matrizSoma <- SomaDeMatrizes(matrizA, matrizB)
Escrever("Soma das matrizes:")
ImprimirMatriz(matrizSoma)

Resposta:

```
function multiplicacaoDeMatrizes(matrizA, matrizB){

    var MatrizResultado

    if(matrizA[0].length == matrizB.length){
        for(let i = 0; i < matrizA.length; i++){
            for(let a = 0; a<matrizA.length; a++)
            {
                for(let j =0; j < matrizB.length; j++){
                    matrizResultado[i][a] = matrizA[i][j]*matrizB[j][a] //vai multiplicando  os valores e armazenado na nova matriz
                }
            }
        }
    }
    return matrizResultado
}
```
ps: não está funcionando o output mas acredito que a lógica esteja certa
