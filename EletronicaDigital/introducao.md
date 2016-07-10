Dizemos que um circuito é digital quando suas entradas e saídas trabalham com sinais digitais, ou seja sinais com valores bem definidos. geralmente esse circuitos trabalham apenas com dois valores (0 e 1) e por isso, chamamos esses sistemas de digitais binários.

Quando estamos falando de circuitos digitais , estamos falando de transporte de informação. E como temos somente dois valores possíveis de tensão, teremos toda a informação codificada em binário - chamamos cada informação binária de bit (dígito binário ou **_b_**_inary dig_**_it_**, do Inglês) e o s representamos por 0 e 1.

Dessa forma, se nossos circuitos trabalham com tensões de 0V e 5V, dizemos que 0V equivale ao bit 0 e 5V equivale ao bit 1 -- agora passamos a falar de bits (informação) em vez de tensões, ou seja estamos pensando uma camada acima.

É importante observar que os Microcontroladores são feitos para terem uma certa tolerância as faixas de tensão que identifiquem os níveis 0 e 1, isto se faz necessário para evitar leituras erróneas, principalmente se a tensão de alimentação do MCU, estiver baixa, por exemplo o ATmega é capaz de funcionar com 2.8V mesmo o ideal sendo 5V. No caso do ATmega328 o valor 0 é obtido com uma tensão inferior a 0.3V e o valor 1 é obtido com uma tensão superior a 0.6V, mas o que acontece se for oferecido uma tenção de 0.4V por exemplo? neste caso a leitura poderá ser imprecisa.

*   *   1.  Convertendo Base numéricas

As conversões numéricas entre Decimal e Binário é muito simples e importante, já que nos tempos 10 possibilidades para apresentar um valor em um unico digito, já o computador somente tem 2 possibilidades.

Bem para fazermos a conversão de um número decimal para binário precisamos dividir o número decimal pela base desejada, no caso 2, portanto começando com um número simples:

| **_~~Divisão para conversão~~_** | **_~~Quociente na Calculadora~~_** | **_~~Quociente~~_** | **_~~Resto~~_** |
| --- | --- | --- | --- |
| **_~~437/2~~_** | **_~~218,5~~_** | **_~~218~~_** | **_~~1~~_** |
| **_~~218/2~~_** | **_~~109~~_** | **_~~109~~_** | **_~~0~~_** |
| **_~~109/2~~_** | **_~~54,5~~_** | **_~~54~~_** | **_~~1~~_** |
| **_~~54/2~~_** | **_~~27~~_** | **_~~27~~_** | **_~~0~~_** |
| **_~~27/2~~_** | **_~~13,5~~_** | **_~~13~~_** | **_~~1~~_** |
| **_~~13/2~~_** | **_~~6,5~~_** | **_~~6~~_** | **_~~1~~_** |
| **_~~6/2~~_** | **_~~3~~_** | **_~~3~~_** | **_~~0~~_** |
| **_~~3/2~~_** | **_~~1,5~~_** | **_~~1~~_** | **_~~1~~_** |
| **_~~1/1~~_** | **_~~,5~~_** | **_~~0~~_** | **_~~1~~_** |

Agora coloque os valores do resto organizados de baixo para cima, assim nosso número 437 em binário é representado como 1-1011-0101\. Usamos os traços para separar os grupos numéricos de 4 em 4, completando com zero as casas vazias. Finalmente temos 0001-1011-0101, bem, nos trabalhamos com agrupamentos em Bytes que representam 8 bits, cada bit é a menor unidade que o computador trata. finalmente nosso número ficará assim: 0000-0001-1011-0101.

O número 437 é um número que ocupa 2 Bytes, veremos mais detalhes sobre bytes, e seus múltiplos quando formos estudar a linguagem C/C++ e sua variante Wire.

Agora vamos pegar um número binário qualquer e vamos transforma lo em um número decimal, usaremos o número 0010-0001-0111-1101, montei uma tabela para ajudar a compreender o processo, observe que da direita para a esquerda temos uma sequência comum na primeira linha, estou inciando ali a potência representada pela casa onde se encontra o número 0 ou 1, na segunda linha mostro esta sequência sobre a base 2, e na terceira linha o total da potência calculada. Agora é simples basta multiplicar os 0 e 1's conforme sua posição e somar os valores obtidos. Teremos assim o valor 8573.

| **_~~15~~_** | **_~~14~~_** | **_~~13~~_** | **_~~12~~_** | **_~~11~~_** | **_~~10~~_** | **_~~9~~_** | **_~~8~~_** | **_~~7~~_** | **_~~6~~_** | **_~~5~~_** | **_~~4~~_** | **_~~3~~_** | **_~~2~~_** | **_~~1~~_** | **_~~0~~_** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **_~~32768~~_** | **_~~16384~~_** | **_~~8192~~_** | **_~~4096~~_** | **_~~2~~_** | **_~~1024~~_** | **_~~512~~_** | **_~~256~~_** | **_~~128~~_** | **_~~64~~_** | **_~~32~~_** | **_~~16~~_** | **_~~8~~_** | **_~~4~~_** | **_~~2~~_** | **_~~1~~_** |
|  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |  |
| **_~~0~~_** | **_~~0~~_** | **_~~1~~_** | **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~1~~_** | **_~~0~~_** | **_~~1~~_** | **_~~1~~_** | **_~~1~~_** | **_~~1~~_** | **_~~1~~_** | **_~~0~~_** | **_~~1~~_** |
| **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** | **_~~*~~_** |
| **_~~0~~_** | **_~~0~~_** | **_~~8192~~_** | **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~256~~_** | **_~~0~~_** | **_~~64~~_** | **_~~32~~_** | **_~~16~~_** | **_~~8~~_** | **_~~4~~_** | **_~~0~~_** | **_~~1~~_** |

Agora peque o resultado da ultima linha da tabela acima e some todos os números:

8192+256+64+32+16+8+4+1= 8573

Prática

Faça um teste com um potenciometro de 10K, ligando um pino ao negativo (GND) e outro ao positivo (VCC) e o pino central ligue na porta digital, e faça a leitura desta porta periodicamente e vá ajustando o potenciometro, use o multímetro para ver as tensões que oferecidas conforme gira o potenciometro.

Converta mais números da base 10 para 2 e vice versa, use os números abaixo como sugestão:

64000 =

0101-1110-0110-1111 =

6-2111 =

12211 =

1111 =

11111

*   *   1.  Portas Lógicas

Assim como na Matemática, possuímos operações básicas como soma, subtração, multiplicação e divisão, na aritmética binária temos operações que podemos fazer com nossos bits. Para simplificar, vamos tratar as operações com uma ou duas entradas, apenas uma saída, tratar o bit 0 como sinônimo de falso e o bit 1 como sinônimo de verdadeiro. Dessa forma, temos as seguintes operações:

*   **AND**: Operação que resulta em bit 1 somente quando os dois bits de entrada são 1 (ou seja, só resulta em “verdadeiro” se somente o primeiro **e** o segundo bit forem “verdadeiros”.);
*   **OR:** Operação que resulta em 1 quando pelo menos uma das entradas é 1 (ou seja, resulta em “verdadeiro” quando o primeiro **ou** o segundo bit, **ou** ambos forem “verdadeiros”;
*   **NOT**: Operação que resulta na inversão do bit de entrada;
*   **XOR:** Também chamado de _exclusive or_ (“ou exclusive”), essa operação só resulta em bit 1 quando somente um dos bits de entrada é 1.

O circuito abaixo exemplifica a criação de uma porta do tipo **AND:**

|  |
| --- |
| **_~~Porta AND criada com diodo e resistor.~~_** |

3.2.1 Tabela-Verdade

Para um número finito de entradas podemos aplicar as operações lógicas em todos os possíveis valores dessa entrada e obter todos os possíveis resultados da operação/função lógica. Chama se tabela-verdade a tabela que lista todas essa possibilidades.

Para as funções lógicas acima, quando temos duas entradas temos um total de 4 possíveis combinações de entrada diferentes (o número de combinações binárias é sempre , onde “entradas” são o número de portas de entrada) e as seguintes tabelas:

| **_~~A~~_** | **_~~B~~_** | **_~~A OR B~~_** | **_~~A AND B~~_** | **_~~NOT A~~_** | **_~~A XOR B~~_** |
| --- | --- | --- | --- | --- | --- |
| **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~0~~_** | **_~~1~~_** | **_~~0~~_** |
| **_~~0~~_** | **_~~1~~_** | **_~~1~~_** | **_~~0~~_** | **_~~1~~_** | **_~~1~~_** |
| **_~~1~~_** | **_~~0~~_** | **_~~1~~_** | **_~~0~~_** | **_~~0~~_** | **_~~1~~_** |
| **_~~1~~_** | **_~~1~~_** | **_~~1~~_** | **_~~1~~_** | **_~~0~~_** | **_~~0~~_** |

Além das operações básicas, temos as negações nas mesmas, como NAND, NOR e XNOR. Para saber a tabela-vedade dessa, basta negar a saída da tabela verdade das outras operações (AND, OR, XOR, respectivamente).

3.2.2 Representação das operações

As operações lógicas citadas acima podem ser representadas em circuitos pelos seguintes símbolos:

|  |
| --- |
| **_~~Figura 3.3: Símbolos das operações lógicas~~_** |

Além disso, podem ser escritas por extenso:

| **Illegal nested table :** OperaçãoRepresentaçãoNOT AA AND BA NAND BA OR BA NOR BA XOR BA XNOR B |
| --- |
| **_~~Tabela de operações e seus simbolos~~_** |

Funções lógicas compostas

Assim como na Matemática, podemos fazer composições das funções lógicas básicas para obter novas funções (compostas). A função XOR, por exemplo, pode ser obtida através da composição das funções NOT, AND, OR:

|  |
| --- |
| **_~~Figura 3.4: Diagrama da função composta XOR~~_** |

A partir de funções lógicas compostas e técnicas como realimentação conseguimos criar dispositivos mais complexos como _latches_[^72], _flip-flops_[^73]_, coders/decoders, mux/demux_[^74]_,_ dentre outros. Esses dispositivos são a base para criar circuitos lógicos de alto nível, por exemplo: com alguns _flip-flops_ conseguimos criar registradores, que podem evoluir para memórias e fazer parte do circuito de um microprocessador.


