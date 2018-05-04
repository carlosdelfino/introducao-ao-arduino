# Fundamentos de Eletrônica

1. Fundamentos de Eletrônica

Alguns Componentes Eletrônicose suas fórmulas

Este conteúdo faz parte do curso “Basicão da Eletrônica”

* * 1. Tensão, Corrente e Potência
* * 1. Resistência e Capacitância

Veremos agora os dois conceitos mais aplicados na Eletrônica, sem eles nada é possível. Veremos também como usar o multímetro ferramenta fundamental e indispensável para todo hobbista e profissional ligado a eletrônica.

* * * 1. Usando o Multímetro

O multímetro é um equipamento amplamente usado para quem dá manutenção ou desenvolve circuitos, seu nome se dá pelo fato de ser capaz de fazer múltiplas \(multi\) medidas \(metro\). As mais comuns são Resistência \(Ohm\), Tensão \(V\), Corrente \(A\) e suas subdivisões principalmente \(mA\), Capacitância e suas subdivisões \(microFarad - uF, pico Farad - pF, nano Farad - nF\), alguns também mede hFe de transistores, diodos e continuidade de um fio, há os que até consegue medir temperatura e impedância de bobinas.

Abaixo apresento alguns multímetros, sendo da esquerda para direita um multímetro analógico bem simples porém bem útil para medir tensões com variação constante e alguns tipos de circuitos como amplificadores de áudio, no meio o multímetro amarelo é uma excelente opção para quem está começando tem diversas medidas, dentre as padrões, tem também medição **hFE** dos transistores, continuidade e teste de bateria e pilha e diodos. Já o terceiro dentro os semi-profissionais é o melhor custo beneficio, tendo inclusive medição de temperatura, uma excelente precisão, iluminação do display e um pequeno frequencimentro.

|  |  |  |
| --- | --- | --- |
| ~~_**sem marca**_~~ | ~~_**ET-2020 da MinipaouDT830B da UNI-T**_~~ | ~~_**ET-2082C da Minipa**_~~ |

Resistores e Lei de Ohm

Resistores são componentes utilizados com a finalidade de transformar energia elétrica em energia térmica e/ou limitar a corrente elétrica em um circuito. como o próprio nome sugere, eles têm como função oferecer uma resistência à passagem da corrente elétrica -- medimos essa resistência através da unidade \(ohm\).

Por consequência, eles causam uma queda de tensão na região do circuito onde se encontram -- muitas vezes acabamos utilizando esse efeito para conseguirmos tensões intermediárias, caso as fontes de tensão do circuito não consigam fornecê-las. Sabendo-se a tensão e corrente em um resistor, podemos calcular sua resistência através da fórmula:

Por sua vez, a resistência pode ser calculada através das características do material resistivo:

Onde é a resistividade do material, L é seu comprimento e A sua área, ou seja, a resistência é proporcional ao comprimento e indiretamente proporcional à área.

Se, para um determinado circuito, V e I têm uma relação linear, ou seja, R é constante para inúmeros valores de _V_ e _I_, então chamamos o material \(que possui resistência _R\) de ôhmico._

Além da medida \(ohm\), temos múltiplos que medidos em Kilo e Mega, ou seja Kilo ohm que pode ser indicado com K, KR ou mesmo 1k0, por exemplo um resistor de 1500, será representado com o valor 1K5, isto é valido para o mega também, porém para os valores padrões em o símbolo pode ser subistituído pela letra R para facilitar a escrita. Veremos mais a frente uma tabela de valores padrões para industria.

Resistores em série

Se possuirmos resistores em série em determinado circuito, podemos calcular a resistência equivalente do mesmo somando se as resistência, através da fórmula:

|  |
| --- |
| ~~_**Figuras**_~~_** **_9~~_**: Resistores em Série**_~~ |

Resistores em paralelo

Caso os resistores estejam em paralelo, a resistência equivalente será o inverso da soma dos inversos das resistências, como na fórmula a seguir:

|  |
| --- |
| ~~_**Figuras**_~~_** **_10~~_**: Resistores em paralelo**_~~ |

Código de cores

Os resistores possuem um código de cores que nos permite identificar qual sua resistência. Para isso, mapeamos as cores das diversas faixas do resistor e utilizamos a seguinte fórmula para resistores padrões acima de 5%:

Onde _a_, _b_ e _c_ são as primeiras faixas e _t_ a última faixa \(geralmente prata ou dourada\), que representa a tolerância.

Para resistores de precisão como os de 1% ou menos usamos esta formula:

Onde _a_, _b_, _c_ e _d_ são as primeiras faixas e _t_ a última faixa \(geralmente marron\), que representa a tolerância.

Abaixo segue um infograma que demonstra a utilização de cores:

|  |
| --- |
| ~~_**Figuras**_~~_** **_11~~_**: Código de Cores para Resistores**_~~ |

Veja a tabela de valores padrões comerciais:

[http](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[://](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[eletricamentefalando](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[blogspot](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[com](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[br](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[/2011/08/](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[valores](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[comerciais](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[de](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[resistores](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[html](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)

Divisor de Tensão

Como citado acima, resistores criam uma queda de tensão na região do circuito em que estão, Utilizando esse efeito, podemos criar o que chamamos de divisores de tensão: circuitos com resistores que, aplicada uma tensão, têm como saída uma fração \(daí o nome divisores\) dessa tensão de entrada.

É fundamental que compreenda bem o uso e funcionamento dos divisores de tensão, a forma mais comum que irá encontra-lo no contexto do Arduino é quando usar um potenciomentro.

|  |
| --- |
| ~~_**Figuras**_~~_** **_12~~_**: Circuito Divisor de Tensão**_~~ |

A partir do circuito acima, temos que:

Esse recurso é bastante útil quando precisamos medir uma tensão maior do que nosso circuitos conseguem. Por exemplo: se quisermos medir uma tensão que varia de 9 a 12V no Arduíno precisaremos colocá la na faixa de 0 a 5V, já que as portas analógicas do Arduíno trabalham nessa faixa menor. Para isso, poderíamos utilizar um divisor de tensão cujos valores de resistência resultassem em . Dessa forma, os valores lidos em seriam de 3 a 4V.

Porém, atenção: caso precisemos conectar resistores ou outros circuitos resistivo no pino , o cálculo das tensões muda e passa a depender das novas resistências do circuito.

Observe que para medir tensões inferiores a 5V o Arduino tem o pino _**Aref**_ que define o nível de tensão, use o somente para dar uma tensão de referência inferior a 5V permitindo assim que as leituras sejam proporcionais a esta nova tensão de referência.

* * 1. Capacitores e indutores

Apesar de não estudarmos a fundo esses dois elementos básicos de circuitos, eles podem ser importantes no desenvolvimento de futuros projetos. Basicamente, capacitores e indutores armazenam energia \(pense como uma bateria em que você carrega e descarrega de tempos em tempos, porém com capacidade bem limitada\) e são bastante utilizados em filtros de sinais, estabilizadores de tensão, circuitos ressonantes \(como transmissores e receptores de rádio\), dentre outros.

Capacitores

Os capacitores são componentes que armazenam energia em forma de campo elétrico. São formados por duas placas metálicas com um dielétrico \(isolante\) no meio. A unidade de medida é Farad \(F\), porém, 1 Farad é algo bem grande, comumente encontramos capacitores na casa dos

| mF | ~~_**mili Farad**_~~ |  | ~~_**0.0001**_~~ |
| --- | --- | --- | --- |
| ~~_**µF**_~~ | ~~_**micro Farad**_~~ |  | ~~_**0.000001**_~~ |
| nF | ~~_**nano Fard**_~~ |  | ~~_**0.000000001**_~~ |
| pF | ~~_**pico Farad**_~~ |  | ~~_**0.000000000001**_~~ |

Para uma tabela de conversão mais completa visite o site: [http](http://www.convertworld.com/pt/capacitancia/)[://](http://www.convertworld.com/pt/capacitancia/)[www](http://www.convertworld.com/pt/capacitancia/)[.](http://www.convertworld.com/pt/capacitancia/)[convertworld](http://www.convertworld.com/pt/capacitancia/)[.](http://www.convertworld.com/pt/capacitancia/)[com](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)[pt](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)[capacitancia](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)

Abaixo estão as imagens de alguns tipos de capacitores e seu símbolo:

|  |
| --- |
| ~~_**Figura 2.5: Capacitores de Poliester, Cerâmicos e Eletrôliticos**_~~ |

|  |
| --- |
| ~~_**Figura 2.6: Símbolo do Capacitor**_~~ |

* * * * 1. Como ler os valores dos capacitores

Alguns capacitores apresentam uma codificação que é um tanto estranha, mesmo para os técnicos experientes, e muito difícil de compreender para o técnico novato. Observemos o exemplo abaixo:

|  | ~~_**O valor do capacitor,"B", é de 3300 pF \(picofarad = 10**_~~_**-12 **_~~_**F\) ou 3,3 nF \(nanofarad = 10**_~~_**-9 **_~~_**F\) ou 0,0033 µF \(microfarad = 10**_~~_**-6 **_~~_**F\). No capacitor "A", devemos acrescentar mais 4 zeros após os dois primeiros algarismos. O valor do capacitor, que se lê 104, é de 100000 pF ou 100 nF ou 0,1µF.**_~~ |
| --- | --- |


Capacitores usando letras em seus valores

|  | ~~_**O desenho ao lado, mostra capacitores que tem os seus valores, impressos em nanofarad \(nF\) = 10**_~~_**-9**_~~_**F. Quando aparece no capacitor uma letra "n" minúscula, como um dos tipos apresentados ao lado por exemplo: 3n3, significa que este capacitor é de 3,3nF. No exemplo, o "n" minúsculo é colocado ao meio dos números, apenas para economizar uma vírgula e evitar erro de interpretação de seu valor.**_~~ |
| --- | --- |
|  |  |

Multiplicando-se 3,3 por 10-9 = \( 0,000.000.001 \), teremos 0,000.000.003.3 F. Para se transformar este valor em microfarad, devemos dividir por 10-6 = \( 0,000.001 \), que será igual a 0,0033µF. Para voltarmos ao valor em nF, devemos pegar 0,000.000.003.3F e dividir por 10-9 = \( 0,000.000.001 \), o resultado é 3,3nF ou 3n3F.

Para transformar em picofarad, pegamos 0,000.000.003.3F e dividimos por 10-12, resultando 3300pF. Alguns fabricantes fazem capacitores com formatos e valores impressos como os apresentados abaixo. O nosso exemplo, de 3300pF, é o primeiro da fila.

|  |
| --- |
|  |

Note nos capacitores seguintes, envolvidos com um círculo azul, o aparecimento de uma letra maiúscula ao lado dos números. Esta letra refere-se a tolerância do capacitor, ou seja, o quanto que o capacitor pode variar de seu valor em uma temperatura padrão de 25° C. A letra "J" significa que este capacitor pode variar até ±5% de seu valor, a letra "K" = ±10% ou "M" = ±20%. Segue na tabela abaixo, os códigos de tolerâncias de capacitância.

| ~~_**Até 10pF**_~~ | ~~_**Código**_~~ | ~~_**Acima de 10pF**_~~ |
| --- | --- | --- |
| ~~_**±0,1pF**_~~ | ~~_**B**_~~ | **\_\_** |
| ~~_**±0,25pF**_~~ | ~~_**C**_~~ | **\_\_** |
| ~~_**±0,5pF**_~~ | ~~_**D**_~~ | **\_\_** |
| ~~_**±1,0pF**_~~ | ~~_**F**_~~ | ~~_**±1%**_~~ |
| **\_\_** | ~~_**G**_~~ | ~~_**±2%**_~~ |
| **\_\_** | ~~_**H**_~~ | ~~_**±3%**_~~ |
| **\_\_** | ~~_**J**_~~ | ~~_**±5%**_~~ |
| **\_\_** | ~~_**K**_~~ | ~~_**±10%**_~~ |
| **\_\_** | ~~_**M**_~~ | ~~_**±20%**_~~ |
| **\_\_** | ~~_**S**_~~ | ~~_**-50% -20%**_~~ |
| **\_\_** | ~~_**Z**_~~ | ~~_**+80% -20%**_~~ |
| **\_\_** | ~~_**P**_~~ | ~~_**+100% -0%**_~~ |

Agora, um pouco sobre coeficiente de temperatura "TC", que define a variação da capacitância dentro de uma determinada faixa de temperatura. O "TC" é normalmente expresso em % ou ppm/°C \( partes por milhão / °C \). É usado uma seqüência de letras ou letras e números para representar os coeficientes. Observe o desenho abaixo.

|  | ~~_**Os capacitores ao lado são de coeficiente de temperatura linear e definido, com alta estabilidade de capacitância e perdas mínimas, sendo recomendados para aplicação em circuitos ressonantes, filtros, compensação de temperatura e acoplamento e filtragem em circuitos de RF.**_~~ |
| --- | --- |
|  |  |

Na tabela abaixo estão mais alguns coeficientes de temperatura e as tolerâncias que são muito utilizadas por diversos fabricantes de capacitores.

| ~~_**Código**_~~ | ~~_**Coeficiente de temperatura**_~~ |
| --- | --- |
| ~~_**NPO**_~~ | ~~_**-0± 30ppm/°C**_~~ |
| ~~_**N075**_~~ | ~~_**-75± 30ppm/°C**_~~ |
| ~~_**N150**_~~ | ~~_**-150± 30ppm/°C**_~~ |
| ~~_**N220**_~~ | ~~_**-220± 60ppm/°C**_~~ |
| ~~_**N330**_~~ | ~~_**-330± 60ppm/°C**_~~ |
| ~~_**N470**_~~ | ~~_**-470± 60ppm/°C**_~~ |
| ~~_**N750**_~~ | ~~_**-750± 120ppm/°C**_~~ |
| ~~_**N1500**_~~ | ~~_**-1500± 250ppm/°C**_~~ |
| ~~_**N2200**_~~ | ~~_**-2200± 500ppm/°C**_~~ |
| ~~_**N3300**_~~ | ~~_**-3300± 500ppm/°C**_~~ |
| ~~_**N4700**_~~ | ~~_**-4700± 1000ppm/°C**_~~ |
| ~~_**N5250**_~~ | ~~_**-5250± 1000ppm/°C**_~~ |
| ~~_**P100**_~~ | ~~_**+100± 30ppm/°C**_~~ |

Outra forma de representar coeficientes de temperatura é mostrado abaixo. É usada em capacitores que se caracterizam pela alta capacitância por unidade de volume \(dimensões reduzidas\) devido a alta constante dielétrica sendo recomendados para aplicação em desacoplamentos, acoplamentos e supressão de interferências em baixas tensões.

|  | ~~_**Os coeficientes são também representados exibindo seqüências de letras e números, como por exemplo: X7R, Y5F e Z5U. Para um capacitor Z5U, a faixa de operação é de +10°C que significa "Temperatura Mínima", seguido de +85°C que significa "Temperatura Máxima" e uma variação "Máxima de capacitância", dentro desses limites de temperatura, que não ultrapassa -56%, +22%.**_~~ |
| --- | --- |


Veja as três tabelas abaixo para compreender este exemplo e entender outros coeficientes.

| ~~_**Temperatura**_~~ | ~~_**Temperatura**_~~ | ~~_**Variação Máxima**_~~ |
| --- | --- | --- |
| **Illegal nested table :** X-55°CY-30°CZ+10°C | **Illegal nested table :** 2+45°C4+65°C5+85°C6+105°C7+125°C | **Illegal nested table :** A ±1.0%B±1.5%C±2.2%D±3.3%E±4.7%F±7.5%P±10%R±15%S±22%T-33%, +22% U-56%, +22%V-82%, +22% |

Capacitores de Cerâmica Multicamada

|  |
| --- |


Capacitores de Poliéster Metalizado usando código de cores

A tabela abaixo, mostra como interpretar o código de cores dos capacitores abaixo. No capacitor "A", as 3 primeiras cores são, laranja, laranja e laranja, correspondem a 33000, equivalendo a 33 nF. A cor branca, logo adiante, é referente a ±10% de tolerância. E o vermelho, representa a tensão nominal, que é de 250 volts.

|  |
| --- |


| **\_\_** | ~~_**1ª Algarismo**_~~ | ~~_**2ª Algarismo**_~~ | ~~_**3ª N° de zeros**_~~ | ~~_**4ª Tolerância**_~~ | ~~_**5ª Tensão**_~~ |
| --- | --- | --- | --- | --- | --- |
| ~~_**PRETO**_~~ | ~~_**0**_~~ | ~~_**0**_~~ | ~~_**-**_~~ | ~~_**± 20%**_~~ | ~~_**-**_~~ |
| ~~_**MARROM**_~~ | ~~_**1**_~~ | ~~_**1**_~~ | ~~_**0**_~~ | ~~_**-**_~~ | ~~_**-**_~~ |
| ~~_**VERMELHO**_~~ | ~~_**2**_~~ | ~~_**2**_~~ | ~~_**00**_~~ | ~~_**-**_~~ | ~~_**250V**_~~ |
| ~~_**LARANJA**_~~ | ~~_**3**_~~ | ~~_**3**_~~ | ~~_**000**_~~ | ~~_**-**_~~ | ~~_**-**_~~ |
| ~~_**AMARELO**_~~ | ~~_**4**_~~ | ~~_**4**_~~ | ~~_**0000**_~~ | ~~_**-**_~~ | ~~_**400V**_~~ |
| ~~_**VERDE**_~~ | ~~_**5**_~~ | ~~_**5**_~~ | ~~_**00000**_~~ | ~~_**-**_~~ | ~~_**-**_~~ |
| ~~_**AZUL**_~~ | ~~_**6**_~~ | ~~_**6**_~~ | ~~_**-**_~~ | ~~_**-**_~~ | ~~_**630V**_~~ |
| ~~_**VIOLETA**_~~ | ~~_**7**_~~ | ~~_**7**_~~ | ~~_**-**_~~ | ~~_**-**_~~ | ~~_**-**_~~ |
| ~~_**CINZA**_~~ | ~~_**8**_~~ | ~~_**8**_~~ | ~~_**-**_~~ | ~~_**-**_~~ | ~~_**-**_~~ |
| ~~_**BRANCO**_~~ | ~~_**9**_~~ | ~~_**9**_~~ | ~~_**-**_~~ | ~~_**± 10%**_~~ | ~~_**-**_~~ |

* * * * 1. Capacitores em Série

Quando vimos os resistores em série vimos que basta somar seus valores, porém, com os capacitores em Série, ocorre o inverso do que ocorre aos resistores, temos seu valor reduzido, portanto se temos dois capacitores de 1uF em serie teremos como resultado a medida de 0.5uF ou 500nF, ou seja sendo os capacitores do mesmo valor basta dividir pelo número de componentes em série, porém se você tiver valores diferentes aplique a seguinte fórmula:

* * * * 1. Capacitores em Paralelo

Observe que os capacitores em Paralelo somam seu valor, portanto dois capacitores sendo um de 1pF + outro de 500nF montados em serie, será equivalente a 1,5nF ou 1500pF

* * * 1. Indutores

Os indutores são componentes que armazenam energia em forma de campo magnético. Geralmente são formados por bobinas \(fio enrolado\) com um condutor no meio. A unidade medida é o Henry \(H\).

|  |
| --- |
| Figuras 13: Indutores de diversos tipos, comuns no mercado |

|  |
| --- |
| ~~_**Figuras**_~~_** **_14~~_**: Símbolo para Indutores**_~~ |

Não é comum usarmos mais de um Indutor em conjunto para obtermos novos valores, normalmente ajustamos as bobinas manualmente, portanto não iremos apresentar aqui nenhum tipo de informação para calcular valores de indutores em paralelo ou em serie.

Também não é nosso foco o desenvolvimento de indutores, portanto não iremos apresentar neste curso como fazer seus próprios indutores.

Diodos

Diodos são componentes que têm a capacidade de conduzir corrente elétrica em uma direção e bloqueá la em outra -- esse comportamento é chamado de retificação e pode ser utilizado para converter corrente alternada \(CA ou AC -- _alternating current_, do Inglês\) --, a energia que temos em nossa tomadas\) em corrente contínua \(CC ou DC -- _direct current_, do Inglês\) --, a forma como as baterias os fornecem energia\). Outros usos de diodo são proteção de circuitos \(contra corrente reversa\) e extração de modulação de sinais \(por exemplo, para uso em circuitos de comunicação sem fio\).

|  |
| --- |
| ~~_**Figura 2.9: Foto de dois tipos de díodo comuns no mercado, A faixa indica corresponde ao terminal negativo \(Catoto \(K\)\)**_~~ |

|  |
| --- |
| ~~_**Figura 2.10: Representação gráfica do diodo em um circuito**_~~ |

O diodo conduzirá corrente elétrica caso a tensão em seu terminal positivo \(+\) seja maior que a tensão em seu terminal negativo \(-\), ou seja, funcionará como um curto-circuito. Caso contrário, ele funcionará como um circuito aberto \(não conduzirá\). É importante notar que para diodos reais existe uma queda de tensão em torno de 0,7V em sua junção PN e, com isso a tensão do lado positivo precisa ser maior que a tensão negativa + 0,7V para que ele conduza.

Além dos diodos comuns como falamos, existem diodos especiais que atendem funções exclusivas, vejamos alguns deles:

LEDs

Já falamos um pouco dos LEDs anteriormente, e aqui irei complementar mais um pouco. Há vários tipos de LED, desde baixo brilho a alto brilho, além dos de baixa, média, e alta potência, e tais LEDs tem substituído com muito sucesso lampadas nas mais diversas aplicações.

Hoje lampadas de carro já tem sido substituídas por LEDs de alto brilho e baixo consumo, temos as antigas lampadas dicróicas usadas em vitrines que também estão sendo substituídas por LEDs de alto brilho, letreiros, TVs e por ai vai.

Além das diferenças dos modelos como mostrado acima temos diferentes cores, que na verdade são o comprimento da onda de luz que o LED é capaz de imitir e assim temos LEDs coloridos, azuis, verdes, vermelhos, brancos, alaranjados/amarelos e algumas cores como o Ultra violeta e o Infra vermelho, que não são visíveis aos olhos humanos, porém podem ser usados em casos especiais para Tratamento em diversas áreas.

Abaixo segue um gráfico que apresenta as cores e sua colocação no Espectro Eletro Magnético:

|  |
| --- |
|  |

Conforme o material utilizado no LED para produzir um comprimento de onda diferente, temos uma tensão de junção diferente, portanto em muitos casos para se ter um brilho homogêneo entre as cores, é preciso ajustar o resistor para se manter a corrente na faixa dos 20mA.

Abaixo apresento uma tabela para facilitar a encontrar a tensão de calculo mais adequada para seu LED.

| ~~_**Compr. de Onda \(NM\)**_~~ | ~~_**Cor**_~~ | ~~_**VF @ 20MA**_~~ | ~~_**MATERIAL**_~~ |
| --- | --- | --- | --- |
| ~~_**&lt; 400**_~~ | ~~_**Ultravioleta**_~~ | ~~_**3.1 - 4.4**_~~ | ~~_**Aluminium nitride \(AlN\)**_~~ |
| ~~_**400 - 450**_~~ | ~~_**Violeta**_~~ | ~~_**2.8 - 4.0**_~~ | ~~_**Indium gallium nitride \(InGaN\)**_~~ |
| ~~_**450 - 500**_~~ | ~~_**Azul**_~~ | ~~_**2.5 - 3.7**_~~ | ~~_**Indium gallium nitride \(InGaN\)**_~~ |
| ~~_**500 - 570**_~~ | ~~_**Verde**_~~ | ~~_**1.9 - 4.0**_~~ | ~~_**Gallium phosphide \(GaP\)**_~~ |
| ~~_**570 - 590**_~~ | ~~_**Amarelo**_~~ | ~~_**2.1 - 2.2**_~~ | ~~_**Gallium arsenide phosphide \(GaAsP\)**_~~ |
| ~~_**590 - 610**_~~ | ~~_**Laranjado / ambar**_~~ | ~~_**2.0 - 2.1**_~~ | ~~_**Gallium arsenide phosphide \(GaAsP\)**_~~ |
| ~~_**610 - 760**_~~ | ~~_**Vermelho**_~~ | ~~_**1.6 - 2.0**_~~ | ~~_**Aluminium gallium arsenide \(AlGaAs\)**_~~ |
| ~~_**&gt; 760**_~~ | ~~_**Infravermelho**_~~ | ~~_**&lt; 1.9**_~~ | ~~_**Gallium arsenide \(GaAs\)**_~~ |

Mais detalhes podem ser obtidos no link: [http](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[://](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[www](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[radio](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[electronics](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[com](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[info](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[data](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[semicond](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[leds](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[light](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[emitting](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[diodes](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[characteristics](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[php](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)

Diodos Zener

O diodo Zener é um componente muito interessante, e deve ser usado com muita cautela. E mais utilizado como um regulador de tensão e ao contrário do Diodo comum é deve ser usado no circuito com base na sua tenção reversa ou de ruptura, sendo aplicado em posição inversa ao diodo comum para surtir efeito.

É preciso ter cuidado no uso dos Diodos Zener, caso este se danifique ele perde seu efeito deixando passar a tensão total para o circuito, correndo o risco de queimar os demais componentes.

Vejamos na figura abaixo onde temos um circuito de analise:

|  | ~~_**Vs = Tensão da Fonte**_~~ |
| --- | --- |
|  |  |

|  | Vsmax é a tensão máxima que a fonte pode atingir. |
| --- | --- |
|  |  |

Transistores

Transistores são componentes semicondutores usados como amplificadores ou chaveadores. Sua entrada é uma corrente/tensão que altera a corrente/tensão de saída. Os transistores são a base de todos os circuitos integrados e placas modernos - alguns, como os microprocessadores, possuem milhões deles.

Para nossos estudos, iremos focar nos transistores de estrutura bipolar de junção \(ou BJT, _Bipolar Junction Transistor,_ do Inglês\) com polaridade **NPN** ou **PNP**, porém existem outros tipos, como os **FETs.**

|  |
| --- |
| ~~_**Figura 2.11: Símbolos de transistores BJT em circuito elétrico**_~~ |

Os transistores possuem três terminais: base, coletor e emissor. E suas principais equações caraterísticas são:

onde é uma constante \(também referida como \) característica do transistor, é seu fator de amplificação.

A segunda equação nos evidencia o poder de amplificação de um transistor: dependendo da corrente que colocarmos na base \(corrente \), ele permitirá maior ou menor corrente no coletor \(corrente \).

Há muitas outras constantes e formulas relacionadas aos Transistores, que não serão estudas aqui, porém iremos

O encapsulamento dos Transistores

No mercado encontramos transistores NPN e PNP com vários encapsulamentos diferentes. alguns são o 2N3904 \(NPN\) e 2N3906 \(PNP\).

Abaixo uma imagem com alguns transistores em seus diferentes encapsulamentos:

|  |
| --- |
| ~~_**Diversos tipos de transistores: TO-3, TO-218, TO-220, TO-126, TO-18, TO-92**_~~ |

|  |
| --- |
| ~~_**TO-3 em detalhes**_~~ |

Utilização de transistores como relês

Relés são componentes úteis quando precisamos isolar eletronicamente um circuito de controle de um circuito de potência, Se quisermos, por exemplo, acender uma lâmpada incandescente \(que utiliza corrente alternada\) através do Arduino, podemos utilizar um relé: o Arduino controlará o relé, que então fará a conexão \(ou não\) da lâmpada com a tomada. Existem relés mecânicos e de estado sólido \(SSR ou _Solid-state relay_, do Inglês\), porém iremos utilizar um relé mecânico em nosso exemplo, por ser mais barato e fácil de se encontrar no mercado.

Nas imagens abaixo são apresentados, um tipo de rele em estado solido com 7 chaves construídas sobre sobre transistores darlingtons,

|  |
| --- |
| ~~_**UNL 2003 - Rele de estado solido**_~~ |

Um relé comum de 5v,

|  |
| --- |
| ~~_**Rele**_~~ |

Abaixo está um MiniShield vendido na DealExtreame, uma loja chinesa que vende diversos acessórios inclusive para Arduino.

|  |
| --- |
| ~~_**Minishield Rele, Vendido na DealExtreme**_~~ |

Como relés possuem correntes de ativação maiores que as portas digitais do Arduino conseguem suprir, precisamos amplificar a corrente que sai das portas digitais do Arduino para que ela seja capaz de acionar o relé, o MiniShield apresentado acima já tem no seu circuito os componentes que fazem a compensação de corrente necessária, porém, nos faremos um circuito com um transistor NPN.

Com um relé acionado por 5V, um transistor NPN \(2N3904\) e dois resistores \(10Ω para o relé e 470Ω para a base do transistor\), podemos utilizar o circuito a seguir, para controlar qualquer carga de corrente alternada -- basta ligar a carga às saídas do relé, que não estão indicadas no diagrama:

|  |
| --- |
| ~~_**Figura 2.13: Circuito para ligar um relé \(controlado por transistor\) no Arduino**_~~ |

Fica como exercício para o leitor verificar como seria o uso de um transistor PNP.

Ponte-H

Para estudarmos a Ponte H, precisamos conhecer melhor o funcionamento de um motor, veja abaixo a construção de um Motor de Corrente Continua.

|  |  |  |
| --- |
|  |  |  |
| ~~_**Motor DC**_~~ |  |  |

Em alguns projetos precisamos inverter a tensão de entrada de determinado circuito. Por exemplo: os motores de corrente contínua girando para um lado caso apliquemos tensão positiva em seu terminal esquerdo e negativa em seu terminal direito. Porém, para fazê los girar em sentido contrário, precisamos aplicar tensão negativa em seu terminal esquerdo e positiva em seu terminal direito.

Podemos implementar circuitos que fazem essa inversão de tensão a partir de 4 transistores funcionando como chave. Esse tipo de circuito se chama ponte-H por conta da disposição dos transistores com relação ao motor, como pode ser visto no diagrama a seguir:

|  |
| --- |
| ~~_**Ponte H Conceitual**_~~ |

Quando fechamos a chave S1 e S3, o terminal esquerdo do motor recebe tensão positiva e o direito recebe tensão negativa. Já quando fechamos as chaves s4 e S2, o terminal esquerdo recebe tensão negativa e o direito recebe tensão positiva. O que precisamos agora substituir as chaves por transistores capazes de fornecer a corrente adequada, e assim conseguiremos controlar os motores com o Arduino.

A seguir temos um circuito simples, porem, suficiente para testarmos uma ponte H. Neste circuito nossa fonte de energia será externa ao Arduino para que possamos alimentar da melhor forma o motor usado, a fonte externa deverá fornecer a tensão limite do Motor, ou seja, sendo o motor de 12V deverá ser uma fonte de 12V. Isto vale também para o limite de trenagem de corrente.

Observe este circuito é construído com quatro transistores Darlingtons TIP 120, que tem um HFE maior quanto maior for a corrente, como precisamos economizar ao máximo a corrente drenada do Arduino, e fornecer uma corrente média de 300mA para o motor, o valor ideal do resistor pode ser calculado conforme a formula a seguir:

Usando os seguintes parâmetros:

Para termos em torno de 1A no coletor teremos um HFE em torno de 1200;

Assim basta termos uma corrente na base de 1mA para obtermos mais 1,2A no Coletor;

Teremos como tensão o valor de 5V e a tensão de fuga do transitor o valor de 0,7V;

Neste caso não precisamos nos preocupar com o valor, visto que conseguimos um valor comercial para o resistor. Portanto os resistores R1 e R2 devem ter o valor de 4,3K?

|  |
| --- |
| ~~_**Ponte H + Arduino**_~~ |

Abaixo segue o esquema de montagem no Protoboard

|  |
| --- |
| ~~_**Ponte H**_~~ |

Já abaixo segue o desenho da placa que pode ser usada como um Shield para Arduino UNO.

|  |
| --- |
| ~~_**Circuito feito no Fritzing para confecçionar a Placa**_~~ |

Esta ponte é um modelo simples para se iniciar no conceito, existem diversos modelos de circuitos com maior proteção contra surtos de corrente e combinação incorreta da sinalização.

No site [http](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[://](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[www](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[.](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[mcmanis](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[.](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[com](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[chuck](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[robotics](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[tutorial](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[h](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[-](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[bridge](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge) é apresentado um esquema amplamente conhecido e utlizado na comunidade.

Outra opção é a compra de circuitos prontos para quem não quer montar seu proprio circuito, há opções de Shields como o mostrado abaixo e também circuitos integrados como o L293D

|  |
| --- |
| [https://www.sparkfun.com/products/10018](https://www.sparkfun.com/products/10018) |

* * * * 1. PWM e Ponte-H para controle de velocidade

Como com PWM conseguimos controlar a quantidade de potência que será entregue a um circuito, caso utilizemos PWM como controle de uma ponte-H, podemos limitar a quantidade de potência entregue ao motor e, com isso, controlar sua velocidade.

