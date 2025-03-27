# Instruções

- Faça uma cópia deste arquivo .md para um repositório próprio
- Resolva as 6 questões objetivas assinalando a alternativa correta
- Resolva as 4 questões dissertativas escrevendo no próprio arquivo .md
  - lembre-se de utilizar as estruturas de código como ``esta aqui com ` `` ou
```javascript
//esta aqui com ```
let a = "olá"
let b = 10
print(a)
```
- Resolva as questões com uso do Visual Studio Code ou ambiente similar.
- Teste seus códigos antes de trazer a resposta para cá.
- Cuidado com ChatGPT e afins: entregar algo só para ganhar nota não faz você aprender e ficar mais inteligente. Não seja dependente da máquina! (E não se envolva em plágio!)
- ao final, publique seu arquivo lista_02.md com as respostas em seu repositório, e envie o link pela Adalove. 

# Questões objetivas

**1)** Considere o seguinte código JavaScript:

```javascript
//EX01
let p = 10;
let q = 3;
let r = 6;

let resultado = (p % q === 1) && (r * 2 > p) || (q + r < p);
console.log(resultado);

const valores = [3, 6, 9, 12, 15];
let produto = 1;

for (let j = 0; j < valores.length; j++) {
  produto *= valores[j];
}

console.log("O produto dos valores é:", produto);


```
Qual das seguintes alternativas melhor descreve o que o código faz?

**A) O código avalia a expressão booleana, imprime `true`, calcula o produto dos números na lista e imprime o resultado no console.**

*o código avalia a expressão e imprime true pois ele cumpre os requisitos do resultado:
i) p % q === 1 significa que o mdc de p e q é 1. nesse caso, isso é verdade pois 10 e 3 são primos entre si;
ii) r * 2 > p significa que o dobro de r deve ser maior que o valor de p. nesse caso, isso é verdadeiro pois 6 * 2 > 10;
iii) q + r < p significa que a soma de q e r deve ser menor que p, o que também é verdade, já que 6 + 3 < 10
como as condições do resultado são o resultado verdadeiro para i) e ii) ou iii), e os três são verdadeiros, o código imprime true.
além disso, a estrutura posterior retorna o produto dos valores. o for diz que, à medida que o índice do array valores aumenta, o produto é atualizado para o produto de todos os números da lista.*

B) O código avalia a expressão booleana, imprime `false`, calcula o produto dos números na lista e imprime o resultado no console.

C) O código avalia a expressão booleana, imprime `true` e, em seguida, verifica se o número 6 está na lista.

D) O código avalia a expressão booleana, imprime `false` e ordena os valores em ordem crescente.


______

2) O código a seguir contém duas funções que calculam o limite de crédito de um cliente com base nos seus gastos e na renda mensal.

// Versão 1 da função de análise de crédito

```javascript
function analisarCredito1() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    do {
        totalCompras += compras[i];
        i++;
    } while (limite >= totalCompras && i < compras.length);

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```
// Versão 2 da função de análise de crédito
```javascript
function analisarCredito2() {
    var compras = [2500, 1200, 800, 100];
    var totalCompras = compras[0];
    var limite = 5000;
    var status = 'aprovado';
    var saldoDisponivel = 0;
    var i = 1;

    while (limite >= totalCompras && i < compras.length) {
        totalCompras += compras[i];
        i++;
    }

    saldoDisponivel = limite - totalCompras;

    if (saldoDisponivel < 0) {
        status = 'negado';
    }
    console.log(`Seu crédito foi ${status}. Saldo disponível: ${saldoDisponivel}.`);
}
```
Se ambas as funções forem executadas com os valores fornecidos, qual será a saída exibida no console?

**A) Ambas as funções exibirão: 'Seu crédito foi aprovado. Saldo disponível: 400.'**

**

B) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -600.', enquanto analisarCredito2() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.'

C) analisarCredito1() exibirá: 'Seu crédito foi negado. Saldo disponível: -200.', enquanto analisarCredito2() exibirá: 'Seu crédito foi aprovado. Saldo disponível: 100.'

D) Ambas as funções exibirão: 'Seu crédito foi aprovado Saldo disponível: 500.'
______

**3)** Considere o seguinte trecho de código em JavaScript:
```javascript
//EX03
const idade = 21;

if (idade >= 18 && idade < 60) {
  console.log("Você é um adulto!");
} else if (idade < 18) {
  console.log("Você é menor de idade!");
} else {
  console.log("Você está na melhor idade!");
}
```
Qual das seguintes alternativas melhor descreve o comportamento do código?

A) O código verifica se a idade indica um adulto ou um idoso e exibe a mensagem correspondente.

**B) O código verifica se a idade pertence à faixa adulta. Se for, exibe "Você é um adulto!". Caso contrário, verifica se é menor de idade e exibe "Você é menor de idade!". Se nenhuma das condições anteriores for verdadeira, exibe "Você está na melhor idade!".**

*primeiro analisa se a idade é maior ou igual a 18 e menor que 60, no primeiro if. se sim, imprime "você é um adulto!". se a idade não se encaixar nessa faixa, segue para a próxima verificação, que verifica se a idade é menor que 18. se sim, imprime "você é menor de idade!". se nenhuma dessas duas condições for atendidas, segue para o else, que imprime "você está na melhor idade!". nesse caso, quando o código é rodado, imprime "você é um adulto!".*

C) O código verifica se a idade está entre 18 e 60 anos e, se for, imprime "Você é um adulto!". Se não estiver nesse intervalo, imprime "Você está na melhor idade!".

D) O código verifica se a idade é menor de 18, entre 18 e 60 ou acima de 60, imprimindo uma mensagem específica para cada caso.
______

**4)** Qual será o resultado impresso no console após a execução do seguinte código?
```javascript
//EX04
var energiaDisponivel = 1200;
var bateriaExtra = 400;
var consumoDispositivos = [300, 600, 500, 200, 400];

for (var i = 0; i < consumoDispositivos.length; i++) {
    var consumo = consumoDispositivos[i];

    if (consumo <= energiaDisponivel) {
        console.log("Dispositivo " + (i+1) + " ligado. Energia restante: " + (energiaDisponivel - consumo));
        energiaDisponivel -= consumo;
    } else if (consumo <= energiaDisponivel + bateriaExtra) {
        console.log("Dispositivo " + (i+1) + " ligado com bateria extra. Energia restante: " + ((energiaDisponivel + bateriaExtra) - consumo));
        energiaDisponivel = 0;
        bateriaExtra -= (consumo - energiaDisponivel);
    } else {
        console.log("Dispositivo " + (i+1) + " não pode ser ligado. Energia insuficiente.");
    }
}
```

Escolha a opção que responde corretamente:

A)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 ligado com bateria extra. Energia restante: 0

Dispositivo 5 ligado. Energia restante: -200

B)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 200

Dispositivo 4 não pode ser ligado. Energia insuficiente.

Dispositivo 5 não pode ser ligado. Energia insuficiente.

C)
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado com bateria extra. Energia restante: 700

Dispositivo 3 ligado. Energia restante: 400

Dispositivo 4 não pode ser ligado. Energia insuficiente.

**D)**
Dispositivo 1 ligado. Energia restante: 900

Dispositivo 2 ligado. Energia restante: 300

Dispositivo 3 ligado com bateria extra. Energia restante: 200

Dispositivo 4 não pode ser ligado. Energia insuficiente.

Dispositivo 5 não pode ser ligado. Energia insuficiente.

**


______

**5)** Qual é a principal função do método update() em um jogo desenvolvido com Phaser.js?

Escolha a opção que melhor descreve seu propósito:

A) O método update() é responsável por carregar os assets do jogo antes da cena ser exibida.

**B) O método update() é chamado continuamente a cada quadro (frame) do jogo, sendo usado para atualizar a lógica, movimentação e interações dos objetos na cena.**

*o método update é atualizado continuamente, e é muito utilizado para movimentações, por exemplo, pois estas são ações que geralmente funcionarão continuamente (em loop) no jogo.*

C) O método update() renderiza todos os sprites na tela e garante que a física do jogo seja processada corretamente.

D) O método update() é chamado apenas uma vez após a criação da cena, sendo utilizado para configurar variáveis iniciais do jogo.
______

**6)** Qual é o principal objetivo do módulo Matter.js Physics em Phaser.js?

Escolha a opção que responde corretamente:

**A) Simular física avançada, incluindo corpos rígidos, colisões complexas e interação entre objetos com gravidade e forças.**

*O Matter.js é uma biblioteca de física 2D para JavaScript. Ele é usado para simular interações físicas realistas em aplicações web e jogos, e pode ser aplicado em detecção de colisão, corpos rígidos, gravidade e forças, restrições e juntas e motores e animações.*

B) Gerenciar eventos de entrada do usuário, como cliques e toques na tela, permitindo movimentação de personagens.

C) Renderizar gráficos otimizados para jogos 2D e garantir uma taxa de quadros estável.

D) Criar animações automáticas para sprites e objetos interativos sem necessidade de programação de movimentação.

______

# Questões dissertativas

**7)** Uma loja online deseja implementar um sistema de classificação de pedidos com base no valor total da compra. O sistema deve determinar a categoria de um pedido com as seguintes regras:

```

Pedidos abaixo de R$50,00 → "Frete não disponível!"

Pedidos entre R$50,00 e R$199,99 (inclusive) → "Frete com custo adicional!"

Pedidos de R$200,00 ou mais → "Frete grátis!"
```
Implemente um pseudocódigo que receba o valor total da compra e exiba a classificação correta do frete para o cliente.

```javascript
//criando a função para analisar o valor do pedido
function analisarPedido (pedido) {
//se o valor for menor que 50,
if (pedido < 50) {
console.log("Frete não disponível!")
//se o valor for entre 50 e 199.99 (inclusive),
} else if (pedido >= 50 && pedido <= 199.99) {
console.log("Frete com custo adicional!")
//se o pedido for maior que 199.99,
} else {
console.log ("Frete grátis!")
}
}
analisarPedido(600);
//imprime "frete grátis!"
```
______

**8)** Considere a implementação da classe base Veiculo em um sistema de modelagem de veículos. Sua tarefa é implementar, utilizando pseudocódigo, as classes derivadas Carro e Moto, que herdam da classe Veiculo, adicionando atributos específicos e métodos para calcular o consumo de combustível de um carro e de uma moto, respectivamente.

```
Classe Veiculo:
Atributos:

modelo
ano
Método Construtor(modelo, ano):

Define os valores dos atributos modelo e ano com os valores passados como parâmetro.
Método CalcularConsumo():
```
Implementação genérica para cálculo de consumo, a ser sobrescrita pelas subclasses.
Agora, implemente as classes Carro e Moto, garantindo que ambas herdem de Veiculo e possuam métodos específicos para calcular o consumo de combustível com base na quilometragem e eficiência do veículo.

o código seria:
```javascript
//criando a classe veículo
class Veiculo {
    constructor (modelo, ano, precoGasolina, eficienciaEnergetica) {
        //definindo os parâmetros ano, modelo, preço da gasolina e eficiência energética
       this.modelo = modelo;
       this.ano = ano;
       this.precoGasolina = precoGasolina
       this.eficienciaEnergetica = eficienciaEnergetica
    }

    //o consumo do veículo será o produto de todos os parâmetros acima
    calcularConsumo(){
        this.consumo = this.precoGasolina * this.volumeVeiculo * this.quilometrosRodados * this.eficienciaEnergetica
    };

}

//criando a classe carro que herda de veículo
class Carro extends Veiculo {
    //os parâmetros são os mesmos, então o super é utilizado para herdar
    constructor (modelo, ano, precoGasolina, eficienciaEnergetica) {
        super (modelo, ano, precoGasolina, eficienciaEnergetica);
    }

    //definindo os parâmetros específicos para carro
    calcularConsumo() {
        this.precoGasolina = 6 //em reais/litro
        this.volumeVeiculo = 20 // em litros
        this.quilometrosRodados = 10000 // em km, por ano
        this.eficienciaEnergetica = 0.5 // parâmetro de 0 a 1, 1 sendo pior e 0 sendo melhor (hipotético)
        super.calcularConsumo(); //o super utiliza o cálculo do constructor do Veículo
        
        //imprime as características do veículo e seu consumo
        console.log("Seu carro é um: " + this.modelo + " " + this.ano)
        console.log ("O consumo deste carro será R$ " + this.consumo + " por ano")
    };

}

//criando a classe moto que herda de veículo
class Moto extends Veiculo {
    //da mesma forma, os parâmetros são os mesmos, então o super é utilizado para herdar
    constructor (modelo, ano, precoGasolina, eficienciaEnergetica) {
        super (modelo, ano, precoGasolina, eficienciaEnergetica);
    }

    //definindo os parâmetros específicos para moto
    calcularConsumo () {
        this.precoGasolina = 4
        this.volumeVeiculo = 10
        this.quilometrosRodados = 10000
        this.eficienciaEnergetica = 1
        super.calcularConsumo();

        //imprime as características do veículo e seu consumo
        console.log("Sua moto é uma: " + this.modelo + " " + this.ano)
        console.log ("O consumo desta moto será R$ " + this.consumo + " por ano")
    };
}

//exemplos: moto1 é uma Yamaha 2006
const moto1 = new Moto ("Yamaha", 2006)
moto1.calcularConsumo();
//imprime: "Sua moto é uma: Yamaha 2006
//O consumo desta moto será R$ 200000 por ano"

//exemplo: carro1 é um Corsa 2015
const carro1 = new Carro ("Corsa", 2015)
carro1.calcularConsumo();
// imprime: "Seu carro é um: Corsa 2015
// O consumo deste carro será R$ 1200000 por ano"
```
______

**9)** Você é um cientista da NASA e está ajudando no desenvolvimento de um sistema de pouso para sondas espaciais em Marte. Seu objetivo é calcular o tempo necessário para que a sonda reduza sua velocidade até um nível seguro para pouso, considerando uma velocidade inicial de entrada na atmosfera marciana e uma taxa de desaceleração constante causada pelo atrito atmosférico e retrofoguetes.

Entretanto, a sonda não pode ultrapassar um tempo máximo de descida para evitar desvios orbitais, nem pode desacelerar além de um limite mínimo, pois isso poderia causar instabilidade no pouso.

Implemente a lógica dessa simulação em pseudocódigo, considerando a seguinte equação para atualização da velocidade:

Considere a fórumla de atualização velocidade:
```
    velocidade = velocidadeInicial - desaceleracao * tempo
```
Seu programa deve determinar quanto tempo será necessário para que a sonda atinja uma velocidade segura de pouso, sem ultrapassar os limites estabelecidos.

```javascript
//parâmetros iniciais
var tempoMax = 50; //segundos
var velocidadeInicial = 100; //metros/segundos
var aceleracaoMax = 5; //metros/segundos^2
var velocidadeMinima = 5; //metros/segundos
var tempo;
var aceleracao = 4; //metros/segundos^2
var velocidade = 80; //metros/segundos

function calcularTempo (velocidade, aceleracao) {
    return tempo = (velocidadeInicial - velocidade)/(aceleracao)
}

//nesse if, são colocadas as condições de erro 
if(aceleracao > aceleracaoMax || velocidade < velocidadeMinima || velocidade > velocidadeInicial || tempo > tempoMax || tempo <= 0) {
    console.log("parâmetros inválidos");
} else {
//calcula o tempo
    console.log("tempo: " + calcularTempo(velocidade, aceleracao) + " segundos");
}

//nesse código, atribuí valores de velocidadeMinima, aceleracao e velocidade condizentes com as condições físicas do problema. para testar
//outros valores, pode-se alterar estas variáveis.

```
______

**10)** Em um sistema de análise financeira, as operações de investimento de uma empresa podem ser representadas por matrizes, onde cada linha representa um tipo de investimento e cada coluna representa um período de tempo.

A seguir, é fornecida a implementação da função SomarMatrizesInvestimento(matrizA, matrizB), que soma os valores de duas matrizes de investimento. Sua tarefa é implementar uma função semelhante, porém que realize a multiplicação das matrizes de investimento, determinando como os investimentos afetam os resultados ao longo do tempo.

```
Função SomarMatrizesInvestimento(matrizA, matrizB):  
    # Verifica se as matrizes têm o mesmo número de linhas e colunas  
    Se tamanho(matrizA) ≠ tamanho(matrizB) então:  
        Retornar "As matrizes não podem ser somadas. Elas têm dimensões diferentes."  
    Senão:  
        linhas <- tamanho(matrizA)  
        colunas <- tamanho(matrizA[0])  
        matrizResultado <- novaMatriz(linhas, colunas)  

        # Loop para percorrer cada elemento das matrizes e calcular a soma  
        Para i de 0 até linhas-1 faça:  
            Para j de 0 até colunas-1 faça:  
                matrizResultado[i][j] <- matrizA[i][j] + matrizB[i][j]  

        Retornar matrizResultado  

# Exemplo de uso da função  
investimentosAno1 <- [[1000, 2000], [1500, 2500]]  
investimentosAno2 <- [[1200, 1800], [1300, 2700]]  

totalInvestimentos <- SomarMatrizesInvestimento(investimentosAno1, investimentosAno2)  
Escrever("Total de investimentos acumulados:")  
ImprimirMatriz(totalInvestimentos)  
```
Agora, implemente a função MultiplicarMatrizesInvestimento(matrizA, matrizB), que multiplica as duas matrizes, simulando o efeito de diferentes fatores de crescimento e impacto financeiro nos investimentos ao longo do tempo.

o códgo para a função acima seria:
```javascript
function somarMatrizesInvestimento(matrizA, matrizB) {
//se as matrizes tiverem tamanhos diferentes (linha e coluna), elas não podem ser somadas
    if (matrizA.length != matrizB.length || matrizA[0].length != matrizB[0].length) {
        console.log("As matrizes não podem ser somadas. Elas têm dimensões diferentes.")
        return null;
    } else {
      //senão, definem-se as linhas e colunas
        var linhas = matrizA.length;
        var colunas = matrizA[0].length;
        //a matriz resultado inicialmente é um array vazio, pois será atualizada depois
        var matrizResultado = [];

        //completude da matrizResultado
        for (i = 0; i <= linhas-1; i++) {
            matrizResultado[i] = [];
            for (j = 0; j <= colunas-1; j++) {
                //soma as linhas e colunas de cada matriz
                matrizResultado[i][j] = matrizA[i][j] + matrizB[i][j]
            }
        } 
        return matrizResultado;
    }
}

let investimentosAno1 = [[1000, 2000], [1500, 2500]]  
let investimentosAno2 = [[1200, 1800], [1300, 2700]]  

//retorna a soma
let totalInvestimentos = somarMatrizesInvestimento(investimentosAno1, investimentosAno2);
console.log("Total de investimentos acumulados: ", totalInvestimentos);

//imprime: 'Total de investimentos acumulados:  [ [ 2200, 3800 ], [ 2800, 5200 ] ]'

```
o código da função MultiplicarMatrizesInvestimento será, então, 
```javascript
function multiplicarMatrizesInvestimento (matrizA, matrizB) {
//nesse caso, para multiplicá-las, elas podem ser de tamanhos diferentes, contanto que o número de colunas de A seja igual ao número de linhas de B
    if (matrizA[0].length != matrizB.length) {
        console.log("As matrizes não podem ser multiplicadas.")
        return null;

    } else { 
        //definindo igual a outra função
        var linhas = matrizA.length;
        var colunas = matrizA[0].length;
        var matrizResultado = [];

        for (i = 0; i <= linhas-1; i++) {
            matrizResultado[i] = [];
            for (j = 0; j <= colunas-1; j++) {
            //inicializa a soma = 0
                let soma = 0;
                for (let k = 0; k < matrizA[0].length; k++) {
                    //multiplica o elemento i de cada linha de A pelo elemento j de cada coluna de B, até prosseguir com todas as linhas e colunas, somando
                    //continuamente
                    soma += matrizA[i][k] * matrizB[k][j];
                }
                //essa soma será a matrizResultado
                matrizResultado[i][j] = soma;
            }
        } 
        return matrizResultado;
    }
}

let investimentosAno1 = [[1000, 2000], [1500, 2500]]  
let investimentosAno2 = [[1200, 1800], [1300, 2700]]  

//retorna o produto das matrizes
let totalInvestimentos = multiplicarMatrizesInvestimento(investimentosAno1, investimentosAno2);
console.log("Total de investimentos acumulados via produto: ", totalInvestimentos);

//imprime: 'Total de investimentos acumulados via produto:  [ [ 3800000, 7200000 ], [ 5050000, 9450000 ] ]'
```
