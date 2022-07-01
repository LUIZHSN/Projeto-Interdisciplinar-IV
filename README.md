![Flappy Bird](https://user-images.githubusercontent.com/57970582/176053345-b352b552-5702-46e2-93ac-16bbd98f5df5.png)

> Status: Em Progresso ⚠️

### Projeto Interdisciplinar IV - UniFasipe.
+ Acadêmico: Luiz Henrique Santos Nascimento.
+ 5º Semestre da UniFasipe - Turno: Noturno.

### Tema
+ Programa em JS que aprende a jogar Flappy Bird por aprendizado de máquina (Neuroevolution).
##

# APRESENTAÇÃO

### 1.0 - Introdução

Sobre o jogo: Flappy Bird é um jogo de celular lançado em 2013 pelo desenvolvedor vietnamita Dong Nguyen. O jogo alcançou um rápido sucesso por ser incrivelmente simples e frustrante: sua única ação disponível é tocar na tela e fazer o passarinho subir um pouco enquanto ele está constantemente caindo e se movendo para direita. Com isso o jogador deve desviar de canos vindo em sua direção, a cada cano desviado o jogador aumenta sua pontuação. 

Por conta de sua simplicidade, o jogo "Flappy Bird" foi a minha escolha para dar início ao projeto.

##

### 2.0 Objetivo

Fazer com que a IA ([NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)) desenvolva o conhecimento para jogar o jogo eletrônico Flappy Bird utilizando o método "Tentativa e Erro". Filtrando os erros e salvando os dados dos acertos até alcançar um ponto onde a mesma irá achar o método de como jogar Flappy Bird sem errar e acabar passando pelos obstáculos

##

### 3.0 Desenvolvimento 

A ([NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)) Funciona da seguinte maneira, captando os dados do ([Game.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/game.js)) como velocidade, gravidade e etc... Ela utiliza como parâmetros esses dados para iniciar o game.js Ela começa criando a "primeira Geração", a primeira geração é composta por 50 “Birds” que será seu ponto inicial para o decorrer da IA. Então ela começa dando o comando para eles pularam enquanto o jogo está com os obstáculos em movimento. E quando o número de vivos chega a zero(0) a IA pega e salva os dados dos melhores “Birds” nomeados como "elitism". Esses seres são os melhores “Birds” da geração em que eles foram criados e a IA utiliza os dados deles para criar a próxima geração e assim ir se aperfeiçoando até alcançar o ponto desejado que é a IA aprenda como jogo funciona e fica jogando para sempre. 

##

### 4.0 Algoritmo
+ 4.1 Fluxograma do Algoritmo

![Projeto Interdiciplinar](https://user-images.githubusercontent.com/57970582/176508140-4db59f7a-9759-4531-b03a-a376400a4e21.png)

Este é o fluxograma do algoritmo de como se comporta perante às atividades em jogo. Nota-se que o ponto chave do algoritmo é quando todos os seres vivos no ambiente da máquina morrem, pois é nesse momento onde ela se pergunta hipoteticamente “O número de vivos da geração atual é igual a zero ?” E nesse ponto onde a máquina salva os melhores pássaros e cria a nova geração com esses novos dados e fica nesse “looping” de aprendizagem até criar um Birds com os dados certos para que esse consiga passar pelos obstáculos do game e não ser atingido e assim então sair do “looping” de aprendizagem.

+ 4.2 Linguagem Utilizada

<table>
  <tr>
    <td>HTML</td>
    <td>JavaScript</td>
  </tr>
  <tr>
    <td>3.0%</td>
    <td>97.0%</td>
  </tr>
</table>

Toda a NeuroEvolution quanto o jogo foram desenvolvidos em JavaScript, uma linguagem de programação interpretada estruturada, de script em alto nível com tipagem dinâmica fraca e multiparadigma, juntamente com HTML.


##

### 4.0 Código
Segue agora alguns trechos do código da [NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)

+ NEURON

```js
var Neuron = function () {
		this.valor = 0;
		this.weights = [];
	}
  //Inicialize o número de pesos de neurônios para valores fixos aleatórios.
  Neuron.prototype.populate = function (nb) {
		this.weights = [];
		for (var i = 0; i < nb; i++) {
			this.weights.push(self.options.randomClamped());
		}
	}
```
<br>

+ LAYER

Classe de camada de rede neural.
```js
var Layer = function (index) {
		this.id = index || 0;
		this.neurons = [];
	}
  //Preencha a camada com um conjunto de neurônios ponderados aleatoriamente.
  //Cada Neurônio deve ser inicializado com entradas nbInputs com um random clamped.
  Layer.prototype.populate = function (nbNeurons, nbInputs) {
		this.neurons = [];
		for (var i = 0; i < nbNeurons; i++) {
			var n = new Neuron();
			n.populate(nbInputs);
			this.neurons.push(n);
		}
	}
```
<br>

+ GENOME

Classe do genoma.
Composto por uma partitura e uma Rede Neural.
```js
var Genome = function (score, network) {
		this.score = score || 0;
		this.network = network || null;
	}
```
<br>

+ GENERATION
```js
var Generation = function () {
		this.genomes = [];
	}
 //Adicionar um genoma à geração.
 	Generation.prototype.addGenome = function (genome) {
		// Localize a posição para inserir o Genoma.
		// Os gnomos devem permanecer ordenados.
		for (var i = 0; i < this.genomes.length; i++) {
			// Classificar em ordem decrescente.
			if (self.options.scoreSort < 0) {
				if (genome.score > this.genomes[i].score) {
					break;
				}
				// Classificar em ordem crescente.
			} else {
				if (genome.score < this.genomes[i].score) {
					break;
				}
			}

		}

		// Insira o genoma na posição correta.
		this.genomes.splice(i, 0, genome);
	}

  
```
<br>

##

#  REFERÊNCIAS BIBLIOGRÁFICAS
Rede neural artificial
https://www.scielo.br/j/rbeaa/a/rSxZNs36XgFcVNKCzJJ63XQ/abstract/?lang=pt

Montage: A Neural Network Language Model-Guided JavaScript Engine Fuzzer
https://www.usenix.org/conference/usenixsecurity20/presentation/lee-suyoung

ESTUDO PARA O DESENVOLVIMENTO DE APLICATIVO BASEADO EM INTELIGÊNCIA ARTIFICIAL PARA CAPTAÇÃO DE VOLUNTÁRIOS PARA ATUAÇÃO NO 3° SETOR COM DISPONIBILIZAÇÃO DE AÇÕES NO 2° SETOR
http://revistas.ung.br/index.php/computacaoaplicada/article/view/3510

CLASSIFICAÇÃO DE COMPONENTES ELETRÔNICOS EM PLACA DE CIRCUITO IMPRESSO UTILIZANDO MACHINE LEARNING.
https://periodicos.ufam.edu.br/index.php/BIUS/article/view/10682

Artificial Intelligence
https://hdsr.mitpress.mit.edu/pub/0aytgrau/release/3?readingCollection=72befc2a

Artificial Intelligence for Games
https://www.taylorfrancis.com/books/mono/10.1201/9781315375229/artificial-intelligence-games-ian-millington-john-funge

Artificial Intelligence and Games
https://link.springer.com/book/10.1007/978-3-319-63519-4?noAccess=true

##

### Demo do Projeto
<div align="center">
  <img src="https://user-images.githubusercontent.com/57970582/176513065-fc651a27-bcbf-4a27-821b-20b07f0e8ac2.gif" align="center">
  </div>

