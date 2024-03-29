﻿# Projeto Unidade 3

## Solucionador de Circuitos Lógicos

O projeto tem a função de construir uma tabela-verdade a
partir da leitura de um arquivo em formato de texto contendo 
as especificações do circuito, ou seja, o número de entradas 
e de saídas, a quantidade e os tipos das portas lógicas, e as 
conexões de entradas e saídas, tanto do circuito como das portas
lógicas.

### Manual 

Para download do código clique [aqui](https://github.com/LuanDHenrique/DCA_Projeto/blob/master/projeto_final.c).

#### Formato do arquivo
O arquivo com a representação do circuito deverá ser criado com 
várias linhas, onde cada linha contém uma instrução sobre uma 
entrada ou saída do circuito, ou uma porta lógica.
No começo da linha deverá ter um identificador, esse 
identificador precisa estar seguido de informações referentes
ao mesmo.

|Identificador                     |Descrição                                 |
|----------------------------------|:----------------------------------------:|
|CIRCUIT id                        |Descritor do circuito com nome id(literal)| 
|PORTA LÓGICA N1 N2 N3             |Tipo da porta (AND, OR, NAND, NOR, XOR), os dois primeiros números são referentes aos nós que as entradas estão ligadas, e o ultimo número ao nó da saída |
|PORTA LÓGICA N1 N2                |Porta NOT, primeiro número é referente ao nó de entrada, e o segundo ao nó de saída |
|INPUT N1 id                       |Entrada do circuito, número referente ao nó de entrada e id(literal) |
|OUTPUT N1 id                      |Saída do circuito, número referente ao nó de saída e id(literal) |


_**OBS:** Para o arquivo ser lido corretamente, os identificadores devem estar escritos com letra maiúscula, 
seguindo exatamente como o modelo dado._    

Para compilar e executar o código foi utilizado o GCC, antes
de tudo, verifique se você está no diretório na qual os arquivos
estão localizados, caso não, se direcione ao diretório, os
comandos utilizados foram os seguintes:

#### Windows:
1. `gcc nome_do_arquivo.c -o nome_do_arquivo`
2. `.\nome_do_arquivo`

#### Linux:
1. `gcc nome_do_arquivo.c -lm -o nome_do_arquivo`
2. `./nome_do_arquivo`

Após executar o arquivo com o código, o programa solicitará que
você insira o local na qual o arquivo com as especificações do
circuito está localizado.

Depois de adicionado o arquivo, ele será lido pelo programa que 
em sequida imprimi na tela a tabela-verdade com a solução para 
cada uma das possibilidades.

### Exemplo:
1. **Arquivo**

|CIRCUIT Exemplo|
|---------------|
|INPUT 1 A|
|INPUT 2 B|
|INPUT 3 C|
|AND 1 2 4|
|OR 2 3 5|
|XOR 4 5 6|
|AND 5 6 7|
|OUTPUT 7 S|

2.**Circuito Exemplo**

A figura a seguir mostra o circuito utilizado como exemplo para teste do projeto.

<img src="https://github.com/LuanDHenrique/DCA_Projeto/blob/master/Circuito.jpeg" alt="Exemplo">


3.**Compilando e executando o código:**

A figura a seguir mostra o passo a passo para compilar e executar o código.


<img src="https://github.com/LuanDHenrique/DCA_Projeto/blob/master/compilando.PNG" alt="compilando">

Após inserir o diretório do arquivo teste, o programa imprimi na tela a tabela-verdade do circuito,
com todas as combinações possíveis para o número de entradas e os resultados das saídas.

<img src="https://github.com/LuanDHenrique/DCA_Projeto/blob/master/executando.PNG" alt="executando">


