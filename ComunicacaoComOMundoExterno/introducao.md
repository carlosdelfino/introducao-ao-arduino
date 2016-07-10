
1.  Módulo

Comunicação Externa
Sensores
Memória Permanente.

*   1.  Capítulo

Comunicações Externas
Se Comunicando Com Outro Dispositivos

*   *   1.  Comunicações Seriais

Muitas vezes apenas controlar um motor ou ligar luzes e desligar geladeira não é suficiente para nosso projeto, precisamos muito mais além disto. As comunicações seriais nos permitem comunicar com outros dispositivos e até mesmo módulos de forma muito mais eficiente, talvez já tenhamos visto na aula prática algumas delas, e neste curso iremos ver de forma mais detalha e profunda cada protocolo de comunicação serial, seja de um fio, dói sou mais.

*   *   *   1.  Serial TTL e RS232

?????????

*   *   *   1.  SPI

?????????

*   *   *   1.  OneWire

?????????

*   *   *   1.  I2C ou TWI?

?????????

*   *   1.  Comunicações em Rede (via Ethernet, WiFi e outras Redes)
            1.  Ethernet

*   *   *   1.  WiFi (Wireless 2.4Ghz)

*   *   *   1.  ZigBee

*   *   *   1.  SubGiga

*   *   *   1.  GSM/GPRS (Celular)

*   1.  Capítulo

Armazenamento de Dados Definitivos

Há várias formas de se armazenar dados permanentemente no Arduino, neste módulo iremos ver especificamente o uso da Memória EEPROM interna do ATmega, já nos próximos módulos veremos o uso do SDCard que é um tipo de memória Flash usado em PenDrives e cartões de memória flash.

Há também memória EEPROM externa que pode ser instalada e acessada via comunicação serial, veremos este tipo de memória quando formos estudar o uso das comunicações via porta I2C.

Usando a Memória EEPROM

EEPROM (Eletrically Erasable Programmable Read-Only Memory, do Inglês) é um tipo de memória não volátil, ou seja, que não se apaga ao retirarmos energia de seu circuito, o que não acontece com a memória do tipo RAM, por exemplo. Alguns perguntam porque não usar a EEPROM como memória para manipular dados durante a execução do programa, porém a EEPROM tem uma durabilidade menor quando gravada na mesma frequência que os tipos de memória RAM, além de serem mais lentas.

O ATMega328, microcontrolador presente no Arduino UNO, possui um circuito EEPROM integrado de 1024 bytes (ou 1KiB) -- em outras versões do Arduino, como o Mega (que usa ATMega1280 ou ATMega 2560, dependendo do modelo), a EEPROM chega chegar até 4KiB.

Ter um circuito EEPROM integrado significa que nosso software pode armaenar 1KiB de dados que não serão perdidos (mesmo que desliguemos o Arduino da fonte de alimentação) -- funciona como se fosse um micro-pendrive. Para utilizar a EEPROM não precisamos de circuitos adicionais: precisamos apenas utilizar a biblioteca EEPROM.h. Porém, para nosso exemplo, vamos ligar um LED na porta 11 e utilizar o seguinte código:

| **_~~#include <EEPROM.h>~~_** |
| --- |
| **_~~Código_Fonte~~ _**11**_~~: Exemplo de uso da Memória EEPROM~~_** |

A diretiva #include diz ao compilador que queremos incluir a biblioteca EEPROM.h -- isso quer dizer que além do código que digitamos, utilizaremos um código já criado pela equipe do Arduíno e transformada em biblioteca para facilitar a utilização da EEPROM.

O exemplo nada mais faz que escrever 16 bytes na EEPROM (na função setup) caso o valor escrito seja inferior 1 (nada esteja escrito) e imprime um ponto a cada dado lido.

Em seguida lê a EEPROM escrevendo este dados na serial;

Agora vamos desligar o Arduíno e liga lo novamente, veja como o código se comporta e o que escreve na serial;

A possibilidade de se manipular os dados da EEPROM de uma forma mais interessante usando a biblioteca EEPROMex que pode ser encontrada no link:

http://playground.arduino.cc//Code/EEPROMex

e pode ser baixada pelo link:

http://thijs.e[lenbaas](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[.](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[net](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[/2012/07/](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[extended](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[-](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[eeprom](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[-](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[library](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[-](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[for](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[-](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[arduino](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)[/](http://thijs.elenbaas.net/2012/07/extended-eeprom-library-for-arduino/)

Identificando Variáveis para Armazenar na EEPROM

Há a possibilidade de se usar uma diretiva "EEMEM" para indicar que uma Variável seja armazenada na EEPROM ao invez de usarmos a memoria comum, com isto facilita o manuseio destes dados em seu programa.

Porém o Arduino ainda não permite que você preinicialize a EEPROM com a inicialização na declaração inicial da variável, apesar da ferramenta AVRDude permiti tal recurso fácilmente, já que o "Optiboot", codigo usado para efetuar a gravação de seu código na mémoria do Arduino.

Mesmo utilizando

Armazenamento em SD Card

??????

Cuidados no uso com SDCard[^76]

?????????

???????The SD library allows for reading from and writing to SD cards, e.g. on the Arduino Ethernet Shield. It is built on sdfatlib by William Greiman. The library supports FAT16 and FAT32 file systems on standard SD cards and SDHC cards. It uses short 8.3 names for files. The file names passed to the SD library functions can include paths separated by forward-slashes, /, e.g. "directory/filename.txt". Because the working directory is always the root of the SD card, a name refers to the same file whether or not it includes a leading slash (e.g. "/file.txt" is equivalent to "file.txt"). As of version 1.0, the library supports opening multiple files.???????

???????The communication between the microcontroller and the SD card uses SPI, which takes place on digital pins 11, 12, and 13 (on most Arduino boards) or 50, 51, and 52 (Arduino Mega). Additionally, another pin must be used to select the SD card. This can be the hardware SS pin - pin 10 (on most Arduino boards) or pin 53 (on the Mega) - or another pin specified in the call to SD.begin(). Note that even if you don't use the hardware SS pin, it must be left as an output or the SD library won't work.??????

*   1.  Capítulo

_Obtendo a Temperatura Externa_

*   *   1.  Obtendo a Temperatura com LM35 ou TMP35

Os sensores de temperatura como LM35 e TMP35 se diferem apenas na nomeclartura pois são de fabricantes diferentes, porém seu computador é bastante similar. A cada leitura é obtido um nível de tensão que equivale a temperatura que está sendo observada por eles.

No gráfico abaixo é apresentado três tipos de sensores da linha TMP que são fabricados pela “Analog Devices”, o gráfico é valido também para os LM35e LM36, iremos trabalhar com o gráfico do LM35, sendo que o LM36 é diferente por ser capaz de trabalhar com temperaturas inferiores a 0 ºC.

Temp in °C = [(Vout in mV) - 500] / 10 (Formula para o LM36

Temp em ºC = [(Vout in mV) - 100] / 10 (Formula para o LM35

So for example, if the voltage out is 1V that means that the temperature is ((1000 mV - 500) / 10) = 50 °C

If you're using a LM35 or similar, use line 'a' in the image above and the formula: Temp in °C = (Vout in mV) / 10

|  |
| --- |
| Figuras 15: Gráfico da Leitura de temperatura LM35, LM34 e LM36 |

| // o Código Abaixo é para o TMP36 |
| --- |
|  |

*   *   1.  Apresentando a Temperatura no PC Graficamente

Prática

Ajustar o código do Processing para que a barra apresente os valores em Graus Centígrados.

1.  Modulo 5

Arduino Na Prática

A seguir uma coléção de propostas de pequenos projetos que podem ter sido já desenvolvidos durante o curso, porém aqui ficam descritos deforma que o aluno possa rever seu conteudo e analisar melhor os conhecimento necessários antes de fazer a prática.

Esta seção somente deve ser seguida quando o aluno já estiver praparado com o conhecimento básico

*   *   1.  Fazendo Barulho

Para quem gosta de fazer música, o Arduino possui uma função pronta para criar uma onda quadrada na frequência e no tempo desejados, Apesar de serem notas simples e a onda ser quadrada, adicionando circuitos extras (para filtros e distorções) e um pouco de criatividade, conseguimos criar sons legais para nossos projetos.

A função que faz esse trabalho é chamada tone. Vamos criar um projeto-exemplo ligando um _buzzer_ componente que reproduz sons de acordo com as variações de tensão em seus terminais - para tocar nosso som da seguinte forma:

|  |
| --- |
| **_~~Figura 4.1: Circuito com buzzer~~_** |

Utilizaremos o seguinte código:

| **_~~#define BUZZER 9~~_** |
| --- |
| **_~~Fonte~~_** |

Além do laço for, utilizamos também um vetor de inteiros chamados notas. Um vetor nada mais é que um local onde armazenamos várias variáveis de mesmo tipo. Os vetores são indexados e para acessar cada item guardado neles utilizamos índices que variam de 0 a n - 1, onde _n_, é o número de total de elementos. No exemplo acima, utilizamos a variável i para percorrer o vetor e, por isso, para acessar os elementos utilizamos i.

Os segredos do código acima são:

*   Saber a frequência das notas[^77] e
*   Saber utilizar a função tone. A função tone recebe três parâmetros, respectivamente: pino (precisa ser um pino que teha suporte a PWM), frequência da nota e duração do som em milissegundos.

Ouvindo com o Arduino

Da mesma forma que podemos escrever valores analogicos no Arduino, podemos ler, e como vimos anteriormente o Arduino tem uma função especial para isto, analogRead, esta função retorna um valor entre 0 e 1023 que é uma amostragem do valor analogico apresentado nas portas A0 até A5 do Arduino UNO.

Com este conversor analogico do Arduino podemos desenvolver um pequeno multímetro ou um VU para medir o nível de sinal.

Veremos aqui como usar o Arduino para Atuar como VU

Podemos usar um circuito pronto como o apresentado na imagem abaixo:

|  |
| --- |
| **_~~Figura : Microfone piezoeletrico pre montado com Amplificador LM386~~_** |

Este circuito já é preparado para uso com Arduino, possui além dos pinos de alimentação, mais dois pinos um que retorna o sinal analógico do microfone amplificado e outro digital que indica a presença de ruído. Há dois LED, um indica que o circuito está alimentado e outro indica o nível de sinal analogico, observe que o Potenciometro permite o controle de ganho do circuito.

Já o circuito abaixo mostra como construir um circuito similar ao anterior porém com componentes discretos.

|  |
| --- |
| **_~~Figura : Esquema do Circuito amplificador para microfone piezoeletríco.~~_** |

Agora vamos ver como este circuito fica no Protoboard:

|  |
| --- |
|  |

*   *   1.  Sistema de Segurança

Um Sistema de segurança composto por um sensor de presença e o disparo de alarme, caso a senha não seja digitada.

*   *   1.  Construindo seu Primeiro Joystick

Um Joystick simples que pode comunicar com o computador ou controlar um Servo Motor ou mesmo um Carrinho com um motor DC controlado por Ponte H.

*   *   1.  Seu primeiro Carrinho Seguidor de Linha

O principio do carrinho seguidor de linha é muito utilizado para veículos não tripulados que podem ser usados por exemplo para guiar um aspirador de pó pela casa, ou um sistema de entrega de insumos em uma industria.

*   *   1.  Um sistema de gestão ambiental

Um sistema de monitoramento do ambiente, como temperatura e humidade, que informa no display suas medições e pode alertar com um sons determinadas situações.

*   *   1.  WebServer

O WebServer pode ser usado nos mais diversos campos, discutiremos como aplicar um WebServer em um sistema de monitoramento ambiental e em um sistema de segurança.

1.  Despedida

Qual seu plano para o futuro? o que você tirou deste curso além de componentes eletrônicos alguns amigos novos? Ideias para trabalho e empreendedorismo?

Vamos alçar voo e olhar por cima de tudo e de todos, mas de forma cautelosa e descobrir quanto vasto é este mundo a nossa volta.

Bibliography

Arduino0001: Martin Evans, Joshua Noble, Jordan Hochenbaum , Arduino em Ação,

[^1]: 

[^2]: 

[^3]: 

[^4]: 

[^5]: - Atualizado em 24 de Outubro de 2013

[^6]: 

[^7]: 

[^8]: 

[^9]: 

[^10]: 

[^11]: 

[^12]: 

[^13]: 

[^14]: 

[^15]: 

[^16]: 

[^17]: 

[^18]: 

[^19]: 

[^20]: 

[^21]: 

[^22]: 

[^23]: Tema de nosso estudo, veja sugestões de links pela apostila.

[^24]: 

[^25]: 

[^26]: 

[^27]: 

[^28]: 

[^29]: 

[^30]: 

[^31]: 

[^32]: 

[^33]: 

[^34]: 

[^35]: 

[^36]: 

[^37]: 

[^38]: 

[^39]: 

[^40]: 

[^41]: 

[^42]: - Atualizado em 03 de Outubro de 2013

[^43]: 

[^44]: 

[^45]: 

[^46]: 

[^47]: 

[^48]: Saiba mais em

[^49]: 

[^50]: 

[^51]: 

[^52]: 

[^53]: 

[^54]: 

[^55]: 

[^56]: 

[^57]: 

[^58]: 

[^59]: 

[^60]: 

[^61]: 

[^62]: 

[^63]: http://www.ti.com/lit/ds/symlink/lm35.pdf.

[^64]: 

[^65]: 

[^66]: http://pt.wikipedia.org/wiki/Dicro%C3%ADsmo

[^67]: 

[^68]: 

[^69]: 

[^70]: 

[^71]: http://www2.eletronica.org/hack-s-dicas/valores-comerciais-para-resistores-capacitores-e-indutores/

[^72]: http://en.wikipedia.org/wiki/Latch_(electronics)

[^73]: http://pt.wikipedia.org/wiki/Flip-flop

[^74]: http://en.wikipedia.org/wiki/Multiplexer

[^75]: https://pt.wikipedia.org/wiki/Mapa_de_Karnaugh

[^76]: http://arduino.cc/en/Reference/SDCardNotes

[^77]: Saiba mais sobre séries harmônicas em http://pt.wikipedia.org/wiki/Série_harmônica_(música)

