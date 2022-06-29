![Flappy Bird](https://user-images.githubusercontent.com/57970582/176053345-b352b552-5702-46e2-93ac-16bbd98f5df5.png)

> Status: Em Progresso ⚠️

### Projeto Interdisciplinar IV - UniFasipe.
+ Acadêmico: Luiz Henrique Santos Nascimento.
+ 5º Semestre da UniFasipe - Turno: Noturno.

### Tema
+ Programa em JS que aprende a jogar Flappy Bird por aprendizado de máquina (Neuroevolution).
##

### 1.0 - Introdução

Sobre o jogo: Flappy Bird é um jogo de celular lançado em 2013 pelo desenvolvedor vietnamita Dong Nguyen. O jogo alcançou um rápido sucesso por ser incrivelmente simples e frustrante: sua única ação disponível é tocar na tela e fazer o passarinho subir um pouco enquanto ele está constantemente caindo e se movendo para direita. Com isso o jogador deve desviar de canos vindo em sua direção, a cada cano desviado o jogador aumenta sua pontuação.

Por conta de sua simplicidade o jogo "Flappy Bird" foi a minha escolha para dar inicio ao projeto.
##

### 2.0 Objetivo
Fazer com que a IA ([NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)) desenvolva o conhecimento para jogar o jogo eletrônico Flappy Bird utilizando o metodo "Tentativa e Erro". Filtrando os erros e salvando os dados até alcançar um ponto onde a mesma irá achar o método de como jogar Flappy Bird sem errar e acabar acertando os obstáculos.

##

### 3.0 Desenvolvimento 

A ([NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)) Funciona da seguinte maneira, captando os dados do ([Game.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/game.js)) como velocidade, gravidade e etc... Ela utiliza como parâmetros esses dados para iniciar o game. Ela começa crinando a "primeira Geração", a primeria geração é composta por 50 Birds que será seu ponto inicial para o decorrer da IA. Entao ela começa dando o comando para eles pularam enquanto o jogo está com os obstáculo em movimento. E quando o numero de vivos chega a zero(0) a IA pega e salva os dados dos melhores Birds nomeados como "elitism". Esses seres são os melhores Birds da geração em que eles foram criados e a IA utiliza os dados deles para criar a proxima geração e assim ir se aperfeirando até alcancar o ponto desejado que é a IA aprende como jogoo funciona e fica jogando para sempre.

Linguagem Utilizada:
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

### 3.1 Fluxograma do Algoritmo 
![Projeto Interdiciplinar](https://user-images.githubusercontent.com/57970582/176508140-4db59f7a-9759-4531-b03a-a376400a4e21.png)
##

### 4.0 Algoritmo
Segue agora alguns trechos do Algoritmo da [NeuroEvolution.js](https://github.com/LUIZHSN/ProjetoInterdisciplinarIV/blob/main/Neuroevolution.js)

+ NEURON
```js

```

<br>

+ LAYER
```js

```

<br>

+ NEURAL NETWORK
```js

```


##

### Demo do Projeto
<div align="center">
  <img src="https://user-images.githubusercontent.com/57970582/176513065-fc651a27-bcbf-4a27-821b-20b07f0e8ac2.gif" align="center">
  </div>

