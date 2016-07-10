Neste capítulo iremos aprender um pouco de lógica, para quem nunca ou tem pouco conhecimento de programação este capítulo será a uma introdução fundamental para ser capaz de produzir pequenos códigos e dar vida as ideias com o Arduino.

Neste curso não veremos ferramentas de diagramação para construção de algoritimos, como Diagramas de fluxo ou UML, porém poderemos usa los aqui para apresentar alguma proposta de algorítimo ou exemplo de ação/script.

Portanto para facilitar o entendimento entre nós apresentarei alguns elementos usados em diagrama de fluxos, usem o fórum do curso para debater e ampliarem seus conhecimentos: [http](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[://](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[www](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[.](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[carlosdelfino](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[.](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[eti](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[.](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[br](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[/](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[cbasem](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[-1/](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[links](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[?](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[task](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[=](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[weblink](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[.](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[go](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[&](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[id](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1)[=1](http://www.carlosdelfino.eti.br/cbasem-1/links?task=weblink.go&id=1).

Diagrama de Fluxo - Fluxograma

Fluxo grama é um tipo de gráfico que permite ao programador desenhar o desenrolar de seu código representando as instruções ou grupos delas por blocos, tendo símbolos para indicar o inicio de um conjunto de instrução e seu fim, entrada e saída, tomadas de decisões e finalmente os blocos de processamento.

Abaixo seguem os símbolos mais usados para representar um Fluxograma:

|  | **_~~O Circulo preenchido indica o inicio de uma sequência de códigos, esta sequência representa todo o programa ou detalhe de um processo.~~_** |
| --- | --- |
|  | **_~~O Circulo preenchido contido em outro circulo indica o fim de uma sequência, seja todo o programa ou o detalhe de um processo.~~_** |
|  | **_~~O Retângulo representa um processo, ou seja uma sequência de comandos, um processo pode ser apenas um comando ou a chamada a uma função que será apresentada em outro fluxo grama.~~_** |
|  | **_~~O Prisma representa um processo de entrada ou saída de dados, por exemplo você pode enviar dados para seu computador ou receber dele via porta serial. Você pode usar também para representar a Leitura na EEPROM (veremos mais adiante) ou a leitura de um sensor (neste caso vc não precisa desenhar o processo de acesso aos dados do sensor, apenas indicando "obter dados do sensor X"~~_** |
|  | **_~~Em uma sequência de comandos ou processo pode haver um momento que deseje tomar uma decisão, como por exemplo ao solicitar o dado ao computador, este enviar uma informação X então executar o processo X1, se enviar a informação Y ele irá executar o processo Y1~~_** |
|  | **_~~Já este simbolo representa algum tipo de tela, como estamos usando microcontroladores que terão apenas LEDs ou em casos mais avançados um simples Display LCD/TFT usaremos este simbolo para indicar a comunicação com o usuário através destes dispositivos, a escolha do dispositivo será a critério do responsável pela especificação do Hardware, conforme o tipo de informação a ser exibida.~~_** |
|  | **_~~O Circulo com uma letra ou número dentro são conectores, muitas vezes nosso código não cabe em apenas uma página então usamos os conectores para indicar que naquele ponto o código será conectado a uma sequência em outro local, tendo portando que indicar cada par de conectores com os mesmos números ou letras.~~_** |
|  | **_~~O bonequinho é usado para representar uma interação com o usuário, quando por exemplo esperamos que uma entrada de dados seja feita por um usuário, outros equipamentos ou dispositivos podem ser representados também como atores que interagem com o sistema.~~_** |

Variáveis e Constantes

Um dos conceitos mais importantes na programação é o de variável e constante. Variáveis é um espaço de memoria que será reservado para armazenar dados que são utilizados em seu aplicativo, as variáveis podem conter um valor binário ou número como também uma representação que será um texto ou seja uma String.

Veremos quando estivermos estudando a Linguagem Wiring e C alguns tipos de variáveis e como usa las, mas por enquanto veremos apenas as variáveis como sendo um espaço na memória que pode guardar um Byte.

Veja abaixo a tabela que representa nosso espaço de memória, observe que no Arduino como usamos a arquitetura Havard temos um espaço de memória que armazena dados e outro que que contem o aplicativo que irá usar tais dados.

Como pode ver na tabela os endereços de memória são identificados internamente no processador por números hexadecimal, mas nas linguagens como a que iremos utilizar são representadas facilmente por nomes. Uma variável é uma forma elegante e fácil de identificar tal espaço da memória que está armazenando seu dado, portanto conforme o tipo de dado ele irá ocupar um espaço ou mais da memória.

| **_~~Endereço~~_** | **_~~Valor~~_** |
| --- | --- |
| **_~~0x0000~~_** |  |
| **_~~0x0001~~_** | **_~~45~~_** |
| **_~~0x0002~~_** |  |
| **_~~0x0003~~_** | **_~~234~~_** |
| **_~~0x0004~~_** | **_~~A~~_** |
| **_~~0x0005~~_** |  |

4.1.2.1 Constantes

Já a constante é um tipo de variável que armazena de forma definitiva um determinado valor. Não podendo ser alterada durante a execução do programa.

Alguns diriam que uma constante não pode ser alterada de forma alguma, porém em se tratando de programação tão baixo nível (tão próxima a linguagem do controlador ou microcontrolador) isto pode ser questionável.

Vou deixar uma dica aqui que lhe será muito útil no futuro se você se dedicar a desenvolver para microcontroladores (desenvolvimento de Firmware).

Os microcontroladores fazem muito uso de registradores e espaço de memória especiais para obter ou enviar informações para o mundo externo a ele, e neste momento o uso de constante pode tornar seu programa mais rápido já que ao compilar seu firmware ele não terá que administrar a escrita em tal espaço de memoria.

Suponha que você tenha um endereço de memória 0x50 que representa um endereço de um registrador que conterá sempre a informação de leitura de uma determinada porta do processador, uma porta de leitura do resultado de conversão analógica por exemplo. Este endereço é escrito apenas pelo Hardware do microcontrolador, então você pode definir que este endereço tem um nome "Leitura_X" e que ele é uma constante, assim sempre que fizer referência a esta variável você estará lendo o conteúdo do registrador 0x50, de uma forma bem amigável.

Estruturas de Dados (Básico)

Não iremos aprofundar no conceito "Estrutura de Dados", porém devemos ter uma conhecimento superficial de listas encadeadas, sejam sequenciais ou arvores de dados, que serão muito úteis.

Uma lista encadeada muito utilizada no Arduino é uma sequência de bytes em Array que é chamada de Ring (Anel), abaixo está uma figura que representa tal estrutura.

| **_~~A estrutura ao lado é representada pelo código abaixo:~~_** |  |
| --- | --- |
| Table 1: Demostração de uma estrutura de dados em Anel |

4.1.4 Classes e Objetos

Nas modernas técnicas de programação é usado o conceito de Classes e Objetos onde cada código desenvolvido tenta replicar o código estruturado de forma a representar os objetos da vida real.

Não iremos aprofundar neste conceito, porém usaremos diversas classes que representaram dispositivos e permitiram armazenar e controlar seu estado.

4.1.5 Operadores

Na programação, não importa a linguagem sempre estaremos excutando algumas operações matemáticas ou lógicas, e sempre atribuindo ou utilizando uma área de memoria para isto, com o auxílio de variáveis e constantes. Vamos ver na tabela abaixo os principais operadores e seu conceito geral, quando estudarmos a linguagem C/C++ iremos rever tais operadores e alguns outros específicos da linguagem.

| **_~~Operador~~_** | **_~~Uso~~_** | **_~~Descrição~~_** |
| --- | --- | --- |
| **_~~=~~_** | **_~~x = yx = x + y~~_** | **_~~Operador de Atribuição, utilizado com variáveis e na declaração de constantes;~~_** |
| **_~~+~~_** | **_~~x = z + y~~_** | **_~~Operador de soma, soma dois operandos, usado com constantes e variáveis;~~_** |
| **_~~-~~_** | **_~~y = r - 22~~_** | **_~~Operador de subtração, subtrai dois valores sejam de constantes ou variáveis; Também pode ser usado para inverter o sinal da variável, se for negativa passa a ser positiva ou vice versa.~~_** |
| **_~~*~~_** | **_~~z = y * x~~_** | **_~~Operador de multiplicação, multiplica dois valores sejam constantes ou variáveis;~~_** |
| **_~~/~~_** | **_~~z = y / 2~~_** | **_~~Operador de multiplicação, Divide dois valores sejam constantes ou variáveis;~~_** |
| **_~~%~~_** | **_~~y % x~~_** | **_~~Operador de modulo, gera o resto da divisão entre constantes ou variáveis;~~_** |
| **_~~<~~_** | **_~~x < y~~_** | **_~~Operador lógico menor que, avalia se o valor da esquerda é menor que o valor da direita retornando verdadeiro ou falso;~~_** |
| **_~~>~~_** | **_~~x < y~~_** | **_~~Operador lógico maior que, avalia se o valor da esquerda é maior que o valor da direita retornando vardadeiro ou falso;~~_** |
| **_~~==~~_** | **_~~x == y~~_** | **_~~Operador lógico de igualdade, avalia se os valores são iguais, retornando verdadeiro ou falso.~~_** |
| **_~~>=~~_** | **_~~x >= y~~_** | Operador lógico que compara se o valor da esquerda é maior que o valor da direita retornando verdadeiro ou falso; |
| **_~~<=~~_** | **_~~x <= y~~_** | Operador lógico que compara se o valor da esquerda é menor que o valor da direita retornando verdadeiro ou falso; |
| **_~~!~~_** | **_~~! (x == y)~~_** | **_~~Operador lógico de negação, retorna o operando lógico inverso da operação que o segue, se verdadeiro retorna falso e vice versa.~~_** |
| **_~~!=~~_** |  | **_~~Operador lógico de desigualdade, avalia se os dois valores são diferentes, retornando verdadeiro ou falso.~~_** |
| **_~~&&~~_** |  | **_~~Operador lógico "And" (E), avalia se os dois valores são verdadeiros~~_** |
| **_~~||~~_** |  | **_~~Lógico "Or" (ou), avalia se os dois valores são verdadeiros, ou um deles.~~_** |

Estruturas de Controle

Há 4 tipos de estruturas de controle muito importantes que precisam ser bem utilizadas quado estamos programando. E programar é tomar decisão sobre o que fazer em determinadas condições, á condições que nos exigem executar um conjunto de comandos, outras condições nos levam a repetir este conjunto até que se estabeleça uma nova condição, e outras que precisamos escolher dentre diversas opções.

4.1.6.1 Estrutura "Enquanto"

A estrutura de controle "Enquanto" é bastante utilizada quando se precisa por exemplo monitorar e esperar uma determinada condição, um exemplo dentro de nosso contexto é processar uma informação "Enquanto" ouver dados chegando em uma determinada porta de comunicação.

Entenda a porta de comunicação como um Escaninho de documentos onde ali é colocado documentos para serem processados, e "enquanto" ouver documentos neste escaninho o administrador (no nosso caso o microcontrolador) não deve fazer nada a não ser o bloco de instruções indicado.

4.1.6.2 Estrutura "Para"

Já a estrutura "para" pode ser um pouco parecida com a estrutura "Enquanto", mas é mais indicada quando se tem uma previsão ou índice para interagir no o processo a ser executado.

Vamos supor que tenhamos uma estante no qual cabe 20 livros por prateleira, e queremos pegar cada livro anotar seu título e colocar de volta no local, portanto "para" cada livro, contanto de 0 a 19, iremos pegar o livro em sua posição e colocar no local de volta.

4.1.6.3 Estrutura de decisão lógica "Se"

Vejamos agora a estruturada "Se" é uma estrutura simples e muito utilizada na programação em qualquer linguagem. Um exemplo prático é o seu dia a dia andando na rua ou dirigindo seu veículo, quando olha para o sinal vermelho, "se" ele estiver Verde você mantém a aceleração, "se não, se"ele estiver amarelo você analisa se deve seguir ou parar, reduzindo a velocidade, "se não, se" ele estiver vermelho você para e finalmente "se nenhuma" das alternativas anteriores você diminui a velocidade olha para os lados e "se" viável continua seu trajeto.

4.1.6.4 Estrutura de decisão logica "Caso"

A estrutura "Caso" não é muito bem vista por alguns programadores, é muito fácil cometer erros com ela, porém é um tipo de estrutura muito poderosa e interessante.

É muito utilizada em situações que precisa analisar muitas opções possíveis, e até mesmo situações que se sobrepõem.

Vejamos uma coleção de situações adaptando o uso da estrutura "Se".

"Caso" o sinal esteja verde vá em frente, "caso" o sinal esteja amarelo, e "caso" esteja vermelho "pare", e se nenhum dos casos anteriores reduza, avalie se deve prosseguir seu trajeto.

Porém o uso mais indicado da estrutura lógica "Caso", é quando o nosso parâmetro lógico é do mesmo tipo, vejamos outro exemplo.

"Caso" você tenha 10 reais você toma um sorvete, "caso" tenha 100 reais você pega um cineminha com uma pipoquinha, "caso" tenha 1000 reais compra uma bike e vai passear, se nenhuma das opções anteriores ocorrer, ligue para seu melhor amigo.

Mais a frente iremos estudar estas estruturas com base no formato adotado pela linguagem.

Arranhando a Tecnologia

Com o objetivo de aprendermos (para quem precisa) e praticarmos um pouco de lógica de programação, iremos usar o Scratch, um aplicativo gratuito criado pelo MIT (Massachusetts Institute of Technology) para facilitar o processo de aprendizado em programação e muito utilizado em projetos educacionais com crianças nas mais diversas idades.

Hoje há diversas aplicações para ferramentas baseadas em linguagens de Blocos, o próprio Android possui uma ferramenta que permite ao desenvolver de aplicações para celular desenvolver soluções usando blocos da mesma forma que o Scratch permite.

Dentro do universo que o Arduíno está incluso temos algumas ferramentas como:

1.  [http](http://home.teleport.com/~brettn/babuinobot_about/index.html)[://](http://home.teleport.com/~brettn/babuinobot_about/index.html)[home](http://home.teleport.com/~brettn/babuinobot_about/index.html)[.](http://home.teleport.com/~brettn/babuinobot_about/index.html)[teleport](http://home.teleport.com/~brettn/babuinobot_about/index.html)[.](http://home.teleport.com/~brettn/babuinobot_about/index.html)[com](http://home.teleport.com/~brettn/babuinobot_about/index.html)[/~](http://home.teleport.com/~brettn/babuinobot_about/index.html)[brettn](http://home.teleport.com/~brettn/babuinobot_about/index.html)[/](http://home.teleport.com/~brettn/babuinobot_about/index.html)[babuinobot](http://home.teleport.com/~brettn/babuinobot_about/index.html)[_](http://home.teleport.com/~brettn/babuinobot_about/index.html)[about](http://home.teleport.com/~brettn/babuinobot_about/index.html)[/](http://home.teleport.com/~brettn/babuinobot_about/index.html)[index](http://home.teleport.com/~brettn/babuinobot_about/index.html)[.](http://home.teleport.com/~brettn/babuinobot_about/index.html)[html](http://home.teleport.com/~brettn/babuinobot_about/index.html)
2.  [http](http://scratch.mit.edu/projects/CatenaryProjects/257547)[://](http://scratch.mit.edu/projects/CatenaryProjects/257547)[scratch](http://scratch.mit.edu/projects/CatenaryProjects/257547)[.](http://scratch.mit.edu/projects/CatenaryProjects/257547)[mit](http://scratch.mit.edu/projects/CatenaryProjects/257547)[.](http://scratch.mit.edu/projects/CatenaryProjects/257547)[edu](http://scratch.mit.edu/projects/CatenaryProjects/257547)[/](http://scratch.mit.edu/projects/CatenaryProjects/257547)[projects](http://scratch.mit.edu/projects/CatenaryProjects/257547)[/](http://scratch.mit.edu/projects/CatenaryProjects/257547)[CatenaryProjects](http://scratch.mit.edu/projects/CatenaryProjects/257547)[/257547](http://scratch.mit.edu/projects/CatenaryProjects/257547)
3.  [http](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[://](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[arduino](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[.](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[cc](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[/](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[blog](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[/2010/10/05/](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[visual](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[programming](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[arduino](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[modkit](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[and](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[the](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[-](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[others](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)[/](http://arduino.cc/blog/2010/10/05/visual-programming-arduino-modkit-and-the-others/)
4.  [http](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[://](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[dimeb](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[.](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[informatik](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[.](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[uni](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[-](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[bremen](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[.](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[de](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[/](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[eduwear](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[/](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[about](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)[-2/](http://dimeb.informatik.uni-bremen.de/eduwear/about-2/)
5.  Há também o Ardublock, porém o site está fora do ar, mas no GitHub está ainda no ar em: [https](https://github.com/taweili/ardublock)[://](https://github.com/taweili/ardublock)[github](https://github.com/taweili/ardublock)[.](https://github.com/taweili/ardublock)[com](https://github.com/taweili/ardublock)[/](https://github.com/taweili/ardublock)[taweili](https://github.com/taweili/ardublock)[/](https://github.com/taweili/ardublock)[ardublock](https://github.com/taweili/ardublock)
    *   *   1.  O Arduino 4 Scratch

Poderemos usar também o A4S que é uma versão adaptada do Scratch para comunicar diretamente com o Arduino e assim facilitar ainda mais o entendimento da metodologia de programação do Arduino.

O processo de instalação apresentado a seguir para o Scratch é similar para o A4S, portanto todo o aprendizado para Scratch servirá para A4S.

Instalando o Scratch

A instalação do Scratch é tão simples quanto qualquer outro programa que nos pede para ler um contrato de uso, indicar uma pasta para guardar os arquivos do programa e um local para criar o icone de atalho para acessar o aplicativo.

Veja na tela abaixo o que você irá encontrar quando baixar o programa pelo Link [http](http://info.scratch.mit.edu/Scratch_1.4_Download)[://](http://info.scratch.mit.edu/Scratch_1.4_Download)[info](http://info.scratch.mit.edu/Scratch_1.4_Download)[.](http://info.scratch.mit.edu/Scratch_1.4_Download)[scratch](http://info.scratch.mit.edu/Scratch_1.4_Download)[.](http://info.scratch.mit.edu/Scratch_1.4_Download)[mit](http://info.scratch.mit.edu/Scratch_1.4_Download)[.](http://info.scratch.mit.edu/Scratch_1.4_Download)[edu](http://info.scratch.mit.edu/Scratch_1.4_Download)[/](http://info.scratch.mit.edu/Scratch_1.4_Download)[Scratch](http://info.scratch.mit.edu/Scratch_1.4_Download)[_1.4_](http://info.scratch.mit.edu/Scratch_1.4_Download)[Download](http://info.scratch.mit.edu/Scratch_1.4_Download), e escolha o pacote a ser baixado conforme o sistema operacional que está usando.

|  |  |
| --- | --- |
|  |  |
|  |

|  |
| --- |
|  |

|  |
| --- |
|  |

**4**.2.2 Meu primeiro Programa

Vamos então brincar com o gatinho.

Do lado esquerdo há da janela do Scratch, no canto superior esquerdo há algumas etiquetas com os cantos coloridos, selecione a primeira etiqueta da segunda coluna, intitulada "Controle". Clicando nesta etiqueta, você verá os blocos de controle e eventos que você pode programar no Scratch, abaixo estão alguns apresentados, durante a aula iremos fazer uma pequena prática.

|  |  |  |  |
| --- | --- | --- | --- |
|  |  |  |  |

Há também outras estruturas de comando que são dependentes de eventos, no nosso contexto iremos lidar com interrupções, externas e internas para lidar com a ocorrencia de eventos. Veja abaixo como o Scratch lida com isto.

|  |  |  |  |
| --- | --- | --- | --- |
|  |  |  |  |

*   1.  Capítulo

**_Programação no Arduíno_**

*   *   1.  A História do Wiring

Wiring na verdade não é uma linguagem mas sim um framework que vem composto por uma IDE já preparada para trabalhar com diversos microcontroladores e placas de prototipação e gravação.

O Wiring tem inicio em 2003 por Hernando Barragán, atuante no Instituto de Ivrea e atualmente na Escola de Arquitetura e Design na Universidade de Los Antes em Bogotá, Colômbia.

O Framework Wiring foi construído sobre o Processing, um Framework baseado no Java e que nos permite modelar graficamente dados obtidos com o Arduíno e outros similares e também facilitar a interação com seu computador.

Atualmente o Arduíno se desmembrou do Wiring e tem sua própria Interface de desenvolvimento e todo o Framework adaptado para os microcontroladores usados no Arduíno.

Quando estamos desenvolvendo para o Arduíno usando o Wiring estamos desenvolvendo um Sketch para o Arduíno do inglês (sketching with hardware).

Antes de aprendermos a trabalhar com o Arduino e sua linguagem ou melhor seu framework precisamos aprender a programar em uma linguagem que muitos acham a linguagem mais avançada e complexa do mundo dos computadores, será?

Bem isto ficará a cargo de seu envolvimento e estudo da linguagem, mas posso lhe garantir que com o uso do Wiring a programação do Arduino se torna muito simples rápida.

Na próxima seção deste capítulo apresentarei primeiramente alguns conceitos da linguagem C e C++, quando necessário apresentarei as diferenças usando os recursos inseridos pelo Wiring.

História da Linguagem C e C++

Muitos de nos já estudou a linguagem C pelo livro C Completo e Total de Herbert Schildt, e irei basear em seu primeiro capítulo para resumir a historia do C que é intimamente ligada com a historia moderna dos computadores, principalmente os Desktops. Já a historia do C++ estarei baseando o conteúdo do site [http](http://www.cplusplus.com/info/history/)[://](http://www.cplusplus.com/info/history/)[www](http://www.cplusplus.com/info/history/)[.](http://www.cplusplus.com/info/history/)[cplusplus](http://www.cplusplus.com/info/history/)[.](http://www.cplusplus.com/info/history/)[com](http://www.cplusplus.com/info/history/)[/](http://www.cplusplus.com/info/history/)[info](http://www.cplusplus.com/info/history/)[/](http://www.cplusplus.com/info/history/)[history](http://www.cplusplus.com/info/history/)[/](http://www.cplusplus.com/info/history/)

A Linguagem C foi inventada e implementada principalmente por Dennis Ritchie em um DEC PDP-11 que utilizava o sistema operacional UNIX hoje tão bem representado pelo Linux. C é o resultado de um processo de desenvolvimento que começou com uma linguagem mais antiga, chamada BCPL, que foi usada, em sua forma original, por muito tempo na Europa. BCPL foi desenvolvida por Martin Richards e influenciou a criação da linguagem chamada B, inventada por Ken Thompson. Já na década de 1970, B levou ao deesenvolvimento de C.

A linguagem C por muito tempo tinha diversas variantes conforme cada empresa que disponibilizava seus compiladores, porém mesmo com tantas variações era possível a portabilidade entre os compiladores e plataformas com um alguns ajustes.

No verão de 1983 o ANSI (American National Standards Institute) estabeleceu um comitê para criar um padrão que definiria de uma vez por todas a linguagem C.

A Linguagem C é uma linguagem Estruturada e de médio nível, ou seja, está um nível acima do nível do processador que é ocupado pelas linguagens Macro-assembler e Assembler.

É importante deixarmos claro que C é uma linguagem para programadores, ou seja para profissionais que lidam diretamente com o computador. Há linguagens como o Cobo, Basic (e suas variações) que foram criadas para profissionais de outros setores que tem necessidade de desenvolverem seus próprios aplicativos.

C foi criada e testada em campo influenciada por programadores, danto portanto o que o programador precisa realmente, poucas restrições, poucas reclamações, estruturas de bloco, funções isoladas e um conjunto compacto de palavras-chaves. Usando C, um programador pode conseguir aproximadamente a eficiência de código assembly combinada com a estrutura de ALGOL.

Em 1979 a linguagem de programação C++ deve inicio com base no trabalho de doutorado de Bjarne Stroustrup, trabalhando com na epoca com a linguagem Simula 67 que já tinha na época o paradgma da orientação para objetos, ou seja Programação Orientado a Objetos (OOP), porém era uma linguagem lenta (será dai que vem o paradgma que linguagens OO são lentas?), diante disto Stroustrup criou a linguagem "C com Classes" ou seja um super conjunto que inclui os recursos da linguagem C mais o conceito de programação com Classes .

O primeiro compilador "C com Classes" foi o Cfront derivado do Cpre, que era responsável por converter o "C com Classes" em C comum.

Em 1983 a linguagem passou a se chamar C++, em 1985 se tornou uma linguagem comercial, e em 1989 foi adicionado novos recursos como múltiplas heranças, membros protegidos e estáticos. Em 1990 foi adicionado uma grande quantidade de bibliotecas através do novo compilador Turbo C++ que teve o último release em 2006\. Em 2011 o padrão atual do C++ foi liberado com o nome C++11, ampliando sua biblioteca, adicionando expressões regulares, melhorias na randomização, uma nova biblioteca para lidar com tempo, suporte para atomics, e uma biblioteca padrão para threads, um novo loop "for" similar ao "foreach", nova palavra chave "auto", novo container de classes, melhor suporte a unions e inicialização de arrays e variadic templates.

Em 1997 o compilador GCC foi criado para atender o projeto GNU e foi escrito pelo Richard Stallman e é amplamente usado no universo Linux e OpenSource. Em 1999 o GCC tem adicionado um ToolChain especifico para o AVR chamado AVR-GCC que tem a biblioteca AVR-LibC para uso no Runtime C/C++, e desde então tem sido acrescentado novos recursos e microcontroladores da linha AVR.

Tipo Básicos de Dados

O primeiro recurso a ser aprendido na programação em Wiring é o tipo de dados que iremos usar nos Microcontroladores AVR e um paralelo com os tipos definidos no C/C++ a serem usados com o Arduíno. Abaixo estará uma tabela

| **_~~Tipo C/C++~~_** | **_~~Wiring/Arduino~~_** | **_~~Bits~~_** | **_~~Faixa mínima~~_** |
| --- | --- | --- | --- |
| **_~~void~~_** | **_~~void~~_** | **_~~*~~_** | **_~~Tipo curinga ou nenhum valor em retorno de funções.~~_** |
| **_~~char~~_** | **_~~char~~_** | **_~~8~~_** | **_~~-127 a 127~~_** |
| **_~~unsigned char~~_** | **_~~unsigned char~~_** | **_~~8~~_** | **_~~0 a 255~~_** |
| **_~~signed Char~~_** | **_~~signed Char~~_** | **_~~8~~_** | **_~~-127 a 127~~_** |
|  | **_~~byte~~_** | **_~~8~~_** | **_~~0 a 255~~_** |
|  | **_~~boolean~~_** | **_~~8~~_** | **_~~False ou (outro valor maior que zero)~~_** |
| **_~~int~~_** | **_~~int~~_** | **_~~ARM 32AVR 16~~_** | **_~~ARM -2147483648 a 2147483647AVR -32767 a 32767~~_** |
| **_~~unsigned int~~_** | **_~~unsigned int~~_** | **_~~ARM 32AVR 16~~_** | **_~~ARM 0 a 4294967295AVR 0 a 65535~~_** |
| **_~~signed int~~_** | **_~~signed int~~_** | **_~~ARM 32AVR 16~~_** | **_~~ARM -2147483648 a 2147483647AVR -32767 a 32767~~_** |
| **_~~short int~~_** | **_~~short~~_** | **_~~16~~_** | **_~~-32767 a 32767~~_** |
| **_~~unsigned short int~~_** | **_~~unsigned short~~_** | **_~~16~~_** | **_~~0 a 65535~~_** |
| **_~~signed short int~~_** | **_~~signed short~~_** | **_~~16~~_** | **_~~-32767 a 32767~~_** |
| **_~~long int~~_** | **_~~long~~_** | **_~~32~~_** | **_~~-2147483647 a 2147483647~~_** |
| **_~~signed long int~~_** | **_~~signed long~~_** | **_~~32~~_** | **_~~-2147483647 a 2147483647~~_** |
| **_~~unsigned long int~~_** | **_~~unsigned long~~_** | **_~~32~~_** | **_~~0 a 4294967295~~_** |
| **_~~float~~_** | **_~~float~~_** | **_~~32~~_** | **_~~3.4028234E+38 a 3.4028234E+38~~_** |
| **_~~double~~_** | **_~~double~~_** | **_~~AVR 32ARM 64~~_** | **_~~o mesmo que float no Arduíno (todos os AVRs), no Arduíno DUE é 64 bits~~_** |
| **_~~long double~~_** | **_~~Não Existe~~_** | **_~~80~~_** | **_~~Dez dígitos de precisão, porém não existe no Arduíno~~_** |
| Table 2 Tipos de dados e seus valores máximos e mínimos. |

Os tipos de dados são padrões até o float, já o double nos modelos de Arduino que são baseados nos microcontroladores AVR 8 bits são equivalentes ao float, porém o Arduino DUE que é baseado na Arquitetura ARM tem o double da mesma tamanho que o C/C++ padrão.

Já o tipo de dado "long double" não existe no mundo AVR nem ARM para o Arduíno.

O tipo Void é um tipo bem interessante, e útil, já que pode ser usado com um tipo curinga em circunstâncias bem especiais, ou mais normalmente deve ser usado para informar que uma função não retorna nenhum valor, ou quando usado nos parametros que não recebe parâmetro algum.

Abaixo segue outro mapa de tipos de dados onde os nomes usados á direita são apelidos criados para facilitar o uso.

| **_~~Arduino ou Wiring~~_** | **_~~Apelido no C/C++~~_** |
| --- | --- |
| **_~~unsigned char~~_** | **_~~uint8_t~~_** |
| **_~~signed char~~_** | **_~~int8_t~~_** |
| **_~~unsigned int~~_** | **_~~uint16_t~~_** |
| **_~~signed int~~_** | **_~~int16_t~~_** |
| **_~~unsigned long~~_** | **_~~uint32_t~~_** |
| **_~~signed long~~_** | **_~~int32_t~~_** |

Modificadores de Tipo

Você deve ter observado na tabela anterior onde os tipos estão listados que estes são repetidos com alguns modificadores, tais modificadores são usados apenas com os tipos básicos e estão listados a seguir:

*   signed
*   unsigned
*   long
*   short

Os modificadores signed e unsigned interferem nos tipos para definir que estes serão com ou sem sinal respectivamente.

Os tipos double não deve receber modificadores de sinal já que isto não é um padrão do Ansi C e não é utilizado no Arduíno.

Constantes

Acima aprendemos um pouco sobre Tipos no Wiring, veremos agora, uma lista de constantes que estão disponíveis para uso em nossos códigos, tais constantes, são formas práticas e fáceis de se lembrar, por exemplo o que é melhor usar o número 3.1415926535897932384626433832795 ou a palavra PI?

Como já explicamos as constantes são espaços de mémoria alocados e com valores que são imutáveis. As constantes podem ser declaradas da mesma forma que variáveis como veremos na próxima seção ou então usando a diretiva de compilação #define.

Veja a tabela a seguir as constantes que já temos definidas no Wiring/Arduino.

| **_~~Nome~~_** | **_~~Valor~~_** |
| --- | --- |
| **_~~PI~~_** | **_~~3.1415926535897932384626433832795~~_** |
| **_~~HALF_PI~~_** | **_~~1.5707963267948966192313216916398~~_** |
| **_~~TWO_PI~~_** | **_~~6.283185307179586476925286766559~~_** |
| **_~~DEG_TO_RAD~~_** | **_~~0.017453292519943295769236907684886~~_** |
| **_~~RAD_TO_DEG~~_** | **_~~57.295779513082320876798154814105~~_** |

Constantes Binárias

Abaixo segue algumas constantes que ajudam a trabalhar com números Binários. Observe que as constantes tem o prefixo B, portanto B00000010 é uma constante para o valor 2 em decimal, na tabela não está apresentado, mas há variações como B10 que também é uma constante para o valor 2.

| **_~~B00000000~~_** | **_~~0~~_** |
| --- | --- |
| **_~~B00000001~~_** | **_~~1~~_** |
| **_~~B00000010~~_** | **_~~2~~_** |
| **_~~B00000011~~_** | **_~~3~~_** |
| **_~~….~~_** | **_~~….~~_** |
| **_~~B1000000~~_** | **_~~64~~_** |
| **_~~B1000001~~_** | **_~~65~~_** |
| **_~~….~~_** | **_~~...~~_** |
| **_~~B11111110~~_** | **_~~254~~_** |
| **_~~B11111111~~_** | **_~~255~~_** |

Verdadeiro ou Falso?

No Wiring/C/C++ zero sempre é falso e qualquer valor diferente de 0 é verdadeiro, portanto para facilitar o uso do verdade/falso existem as constantes "True" que é o valor 0x01 e "False" que é o valor 0x00.

Declarando as variáveis e constantes.

Abaixo iremos aprender como declarar uma variável ou constante, iremos sempre nos referir a ambas como variáveis somente no momento especifico é que iremos fazer a diferenciação.

Sempre que trabalhamos com uma variável ou constante no Wiring/C/C++ precisamos declara com antecedência, o Wiring/C/C++ não admite usarmos uma variável sem que ela exista. Portanto, o mais indicado é fazermos a declaração das nossas variáveis sempre no inicio de seu arquivo que contem o código.

Um tipo de variável ou constante importante que aprenderemos mais a frente são os parâmetros que são utilizados para transferir valores para dentro ou fora de um bloco de código definido como função. Veremos mais detalhes na seção Parâmetros em 3.3.2 - Funções, que está na página 132.

*   *   *   *   1.  Declarando Constantes

Já citamos constantes e mostramos algumas das que já são declaradas, mas como criarmos novas constantes? e porque?

Bem muitas vezes precisamos de novos parâmetros como valores que serão usados de forma fixa em formulas, ou endereços de pinos/portas, neste caso devemos usar a diretiva "const" para declaramos que a variável será do tipo constante.

Além da diretiva "const" podemos também em cenários muito especiais, sugerir que a variável seja armazenada na memória de programa, o que a torna um tipo especial de variável e precisa ser acessada de uma forma especial, veremos isto mais adiante. Por enquanto veja um exemplo de declaração de constantes.

| **_~~const int PORTA_PIR = 10;~~_** |
| --- |
| **_~~Declarando Constante~~_** |

*   *   *   *   1.  Declarando Variáveis

Para declarar variáveis basta apenas remover a declaração "const", usando as demais diretivas apresentadas para definir o tipo de área de memória.

As variáveis são espaços de memórias que podem ter seus dados manipulados em qualquer parte do seu programa, podendo receber novos valores ou ter seus valores alterados por operadores matemáticos ou binários. Veremos mais a frente além do contexto uma diretiva muito importante que auxilia a tratar variáveis que tem seu valores manipulados de forma inesperada.

Lembre-se, usar a diretiva “const” não é sempre a melhor opção para microcontroladores.

*   *   *   *   1.  Variáveis Voláteis.

Há um tipo de variável muito importante chamada "volatile", as variáveis voláteis são usadas normalmente quando uma variável é usada em blocos de códigos comuns e também em blocos de códigos para tratamento de interrupções. A diretiva "volatile" faz com que o compilador dê um tratamento diferenciado a estas variáveis. Permitindo que estas sejam alteradas de forma imprevisíveis. Variáveis voláteis podem também ser usadas para apontar constantes

Veremos a seguir a limitação do scopo ou contexto da variável ou constante, limitando assim sua visibilidade em locais desnecessários, evitando conflitos de nomes e também economizando o uso da memória.

*   *   *   *   1.  Contexto das variáveis

As variáveis são sensíveis ao contexto no qual são declaradas, portanto declarando uma variável em seu arquivo de fora de uma classe, função ou bloco de controle ela terá visibilidade diferente e limitada naquele contexto ao mais interno. Mais a frente iremos estudar blocos de códigos, e veremos que uma variável declarada em um bloco de código que foi declarado dentro de outro bloco, não tem visibilidade no anterior.

Por exemplo uma variável declarada dentro de um bloco de controle como o "for" ou "while" será visível somente dentro do bloco é chamada de variável local.

Já declarando uma variável dentro da função, esta será visível internamente a função e todos os seu blocos, mas não será visível fora dela, nem mesmo as funções que elea chamar. Este tipo de variável também é uma variável local.

Globais

Já as funções declaradas no arquivo serão acessadas em todo o arquivo e se este arquivo for um cabeçalho (arquivo com extensão ".h") quando incluso em outro arquivo dará visibilidade a estas variáveis. Para evitar que isto aconteça, declare as variáveis de seu arquivo como sendo estáticas.

Locais Estáticas

Um recurso interessante a função privadas, estas que são declaradas internamente a uma bloco ou função é quando você as declara como "static", variáveis estáticas quando dentro de funções ou blocos são inicializadas apenas uma vez, tendo um armazenamento similar a uma variável global, porém, inicializadas a primeira vez que são referenciadas, no segundo instante que o bloco ou função é acessado a variável estática irá recuperar seu último valor, mas lembre-se elas não são visíveis externamente ao bloco nem a função onde foi declarada, portanto você não poderá alterar seu valor externamente.

| **_~~#define PORTA_1 = 2;~~_** |
| --- |
| Código_Fonte 3: Exemplo de código sobre declaração de variáveis |

*   *   *   1.  Apelidos para valores máximos e Mínimos

O GCC compilador C/C++ que usaremos fornece alguns apelidos para os limites do tipo que iremos usar, veja a tabela abaixo.

| Tipo | Limite | Apelido | Hexa |
| --- | --- | --- | --- |
| **_~~signed char/byte~~_** | Máximo | **_~~INT8_MAX~~_** | **_~~0x7f~~_** |
| **_~~signed char/byte~~_** | Minimo | **_~~INT8_MIN~~_** | **_~~(-INT8_MAX – 1)~~_** |
| **_~~unsigned char/byte~~_** | Maximo | **_~~UINT8_MAX~~_** | **_~~(__CONCAT(INT8_MAX, U) * 2U + 1U)~~_** |
| **_~~signed int~~_** | Máximo | **_~~INT16_MAX~~_** | **_~~0x7fff~~_** |
| **_~~signed int~~_** | Minimo | **_~~INT16_MIN~~_** | **_~~(-INT16_MAX - 1)~~_** |
| **_~~unsigned int~~_** | Máximo | **_~~UINT16_MAX~~_** | **_~~(__CONCAT(INT16_MAX, U) * 2U + 1U)~~_** |
| **_~~signed long~~_** | Máximo | **_~~INT32_MAX~~_** | **_~~0x7fffffffL~~_** |
| **_~~signed long~~_** | Minimo | **_~~INT32_MIN~~_** | **_~~(-INT32_MAX - 1L)~~_** |
| **_~~unsigned long~~_** | Máximo | **_~~UINT32_MAX~~_** | **_~~(__CONCAT(INT32_MAX, U) * 2UL + 1UL)~~_** |
| Table 3: Valores máximo e mínimo para tipos de dados |

As letras após os números serão descritas quando estivermos vendo sobre "Casting" ou conversão de tipos.

*   *   1.  Conversões de tipos

Muitas vezes temos uma variável ou constante de um tipo e precisamos lidar com ela em tipos diferentes, há diversos tipos de conversões “cast” que podemos usar, mas iremos apenas lidar com as que são aplicadas a números.

Conversão Implícita

As conversões implícitas ocorrem quando se utiliza uma atribuição de determinado tipo em outro sem nenhum tipo de declaração para provocar a conversão de tipos, ou em operações matemáticas onde os valores são de tipos diferentes, levando a conversão do resultado ao tipo necessário, por exemplo divisão de um “float” por um “int”, assim o resultado será “float”.

Porém se houver a divisão de dois inteiros o resultado será um “int”, mesmo que gere um valor fracionado, neste caso o resto será descartado, precisando para isto usar o operador “%” para obter o resto. Veja na conversão explicita como obter um “float” neste tipo de operação.

No exemplo Código_Fonte ( Código_Fonte), mostro o calculo de temperatura, mesmo usando constantes do tipo float (0.5) o resultado será inteiro; Neste calculo a precisão do resultado é perdida devido ao resultado do calculo ser do tipo float mas mesmo assim ter sido atribuído à um tipo “int”.

| void loop(){ |
| --- |
| Código_Fonte 4: Exemplo de conversões implícitas (Implicit Type Casting) |

Conversão Explicita

Na conversão explicita, você informa que tipo deseja forçar o “casting” assim você pode converter qualquer tipo para outro, por exemplo numa divisão de inteiros onde deseja obter o resultado no formato “float” você deve fazer o “casting” de forma explicita do dividendo, veja o exemplo

| void loop(){ |
| --- |
| Código Fonte 5: Exemplo de Conversão Explicita (Explicity Type Casting) |

*   *   1.  Estruturas de Controle
            1.  Blocos de Código

Para programarmos em C ou C++ é importante compreender o que é um bloco de código e como identifica-lo. Tais blocos são delimitados usando os símbolos de chaves “{“ e “}” agrupando assim as instruções em blocos de controle e chamadas de funções., ou mesmo apenas contextualizando um grupo de instruções e variáveis

Os blocos de código podem ser nomeadas como uma função ou acessíveis em determinadas condições como nos blocos de controle.

Dentro de blocos de código na linguagem C/C++ não podemos declarar funções, conhecidas como Inner-Functions;

Uma característica interessante em blocos de código é uso de blocos encadeados, organizando as instruções conforme interesses específicos e além disto delimitando mais ainda a visibilidade variáveis locais. Já que uma variável declarada dentro de um bloco, não importando se foi declarado dentro de outro, não pode ser vista fora do bloco.

Porém, uma variável declarada no bloco principal, poderá ser acessada internamente no bloco secundário e sucessivamente. Veja que isto não se aplica a chamadas de funções, sendo portanto necessário passar a variável por valor ou por referência como veremos mais a frente.

*   *   *   1.  Funções

Funções são de alta importância em uma linguagem de programação estruturada, as funções são blocos de códigos nomeados que podem receber ou não parâmetros, e que podem ser reutilizadas em todo o código conforme a visibilidade dada a elas.

No Arduino o esqueleto padrão do código exige duas funções, ambas sem parâmetros e do tipo “void”, ou seja elas não retornam nenhum valor.

Parâmetros

Parâmetros são um conceito muito importante em se tratando de funções. Quando se deseja passar algum tipo de função de um bloco de código para dentro de uma função ou retornar de uma função para o bloco de código chamador, os parâmetros são os meios mais eficientes para isto, e não consomem memória, já que normalmente são usados registradores para esta atividade.

Parâmetros funcionam de forma bastante similar a variáveis, porém seu contexto serão sempre local ao bloco da função. Podem ser variáveis ou constantes, e podem ser inicializadas com um valor padrão para o caso de não serem obrigatória e poderem portanto serem omitidos na chamada da função. Observe que neste caso de parâmetros opcionais é fundamental que os parâmetros sejam organizados por ordem de prioridade, não colocando parâmetros opcionais no inicio da lista.

Parâmetros podem adotar qualquer tipo de dado, e não podem ser declarados estáticos.

Veremos no exemplo das funções exemplos de uso dos parâmetros.

O Bloco de Código da Função e sua Assinatura

Os blocos de códigos que declaram função possuem uma assinatura que pode ser declarada no inicio do código quando a função está em outro arquivo ou inserida através de um arquivo de cabeçalho, não iremos entrar agora nesta questão, mas sempre que ver uma função sem bloco de código saiba que está vendo a assinatura da função, isto é feito para que o código possa ser compilado sem erro e assim quando a função com seu bloco de código for declarado este seja chamado corretamente.

Veja Código_Fonte, no fonte Código_Fonte, o código de exemplo que mostra como declarar uma função e como declarar sua assinatura. A função abaixo não recebe nenhum parâmetro, no segundo exemplo mostramos como declarar usando parâmetros;

| // includes de suas bibliotecas |
| --- |
| Código Fonte 6: Exemplo de uma Função declarada e também de sua assinatura |

Já no exemplo Código_Fonte, Código_Fonte, adotamos o uso de parâmetros e um valor de retorno, veja que no exemplo também mos primeiramente a assinatura e no final a função com seu bloco de código.

Na assinatura sugerida o segundo parâmetro é do tipo “int” e tem por valor padrão a constante numérica “10”, sendo assim se ele não for informado, será considerado que o parâmetro terá este valor.

Lembre-se parâmetros opcionais devem vir no final da lista de parâmetros, e devem ser definidos principalmente na assinatura da função.

| // includes de suas bibliotecas |
| --- |
| Código Fonte 7: Exemplo de claração de uma função com parametros |

*   *   *   1.  Estruturas de Controle em C/C++

Toda linguagem de programação possui estruturas de controle, e cada uma delas tem sua peculiaridades que a tornam singulares e lhe dão poder, o C/C++ tem três estruturas de controle, e duas instruções de apoio, sendo que uma delas o comando “continue” somente pode ser usado na estrutura de controle do tipo interação.

Vejamos a segui cada tipo de estrutura e como usa-la.

*   *   *   *   1.  Estrutura Condicional

Como o nome diz, esta estrutura é para tomada de decisão com base em condições apresentadas, sempre que for usa-la procure montar uma tabela de opções avaliando as condições necessárias e fazendo as combinações de forma optimizada., procure na internet sobre mapas de karnaugh[^75]. Para facilitar sua vida à na internet sites que oferecem calculadoras em Java e JavaScript

A estrutura Condicional é identificada usando as diretivas “if”, “else” e “if else”, sendo somente a diretiva “if” obrigatória., abaixo segue três exemplos de uso das estruturas condicionais.

| if (condicao_logica){ |
| --- |
| Código_Fonte 8: Exemplo de Estrutura Condicional com apenas o "if" |

Observe no exemplo do código fonte Código_Fonte, Código_Fonte, a instrução “if” vem seguida por parênteses que envolve a condição lógica que irá dar a condição de execução do bloco de código que vem a seguir, esta condição lógica deve ser verdadeira, já que se for falsa o bloco de código não será executado.

| if(condicao_logica){ |
| --- |
| Código Fonte 9: Exemplo de Estrutura Condicional com o "if" e "else" |

Já no código fonte de exemplo Código_Fonte, Código_Fonte, neste código além do “if” como no exemplo anterior, possui agora a diretiva “else” que permite inserir um bloco de código que somente será executado se o if for falso, sendo assim o primeiro bloco logo após o “if” é executado e a condição é verdadeira, já o segundo somente se a condição lógica for falsa.

Observe que somente um “else” pode ser inserido, veja no próximo exemplo como utilizar mais condições.

| if(condicao_logica){ |
| --- |
| Código_Fonte 10: Exemplo de Estrutura Condicional com o "if", "else if" e "else" |

No exemplo Código_Fonte, Código_Fonte, já temos o uso da estrutura completa, sendo que você pode repetir quantos “else if” desejar, observando apenas o bom senso e a complexidade de seu código. O “else”'opcional e pode ser omitido.

É importante ficar bem entendido que cada bloco de código somente será executado se somente sua condição for verdadeira, e na ordem ou seja, se uma das condições for verdadeira, os blocos de código seguintes não serão executados de forma alguma.

*   *   *   *   1.  Estrutura de interação

??????

*   *   *   *   1.  Estrutura de Seleção

Bibliotecas em C/C++

???????

??????

Transferindo Dados por Valor ou Referência

???????

Ponteiros de Dados

???????

Ponteiros de Função

???????

