
 Módulo I
    1.  Conceitos Básicos

Apresentando o Arduino

*   *   1.  O Projeto Arduino

Arduino[^1] é um projeto que engloba _software_ e _hardware_ e tem como objetivo fornecer uma plataforma fácil para prototipação de projetos interativos, utilizando um microcontrolador. Ele faz parte do que chamamos de computação física: área da computação em que o _software_ interage **diretamente** com o _hardware_, tornando possível integração fácil com sensores, motores e outros dispositivos eletrônicos.

O nome Arduino é um substantivo próprio que deriva de uma palavra germânica composto por “Hardu” que significa “forte” ou mesmo num conceito de trabalho de trabalho “Árduo”, ea palavra “Wini”que tem o significa “amigo” formando assim a palavra “Harduwin” que deu nome ao Rei Italiano, que reinou entre 1002 a 1015, o que tornou o nome famoso na Itália. Conforme o Livro “Arduino em Ação” Arduino em Ação de

A parte de _hardware_ do projeto, uma placa que cabe na palma da mão, é um computador como qualquer outro: possui microprocessador, memória RAM, memória flash (para guardar o _software_), temporizadores, contadores, dentre outras funcionalidades. Atualmente, o projeto de placa mais utilizado está na versão Uno R3, que possui um _clock_ de 16Mhz, 2kB de memória RAM, 32kB de memória _flah_, 20 portas digitais e 6 entradas analógicas. Mas verá outros modelos que tem sido acrescido a família a cada momento.

Recentemente foi lançado o Arduino TRE[^2] e em breve será lançado o Arduino Intel Galileo[^3] que é um modelo certificado produzido pela Intel com o processador de mesmo nome, podendo assim rodar linux nativos de forma mais poderosa que o Arduino YUN[^4]. [^5]

Neste curso veremos algumas variações do Arduino Originais, seus clones ou similares.

|  |
| --- |
| **_~~Figura 1.1: Hardware de um Arduino UNO R3~~_** |

A principal diferença entre um Arduino e um computador convencional é que, além do primeiro ter um porte menor (tanto no tamanho quanto no poder de processamento), o Arduino utiliza dispositivos diferentes para entrada e saída em geral. Por exemplo: em um PC utilizamos teclado e mouse como dispositivos de entrada e monitores e impressoras como dispositivos de saída; já em projetos com o Arduino os dispositivos de entrada e saída são circuitos elétricos/eletrônicos.

Como a interface do Arduino com outros dispositivos está mais perto do meio físico que a de um PC, podemos ler dados de sensores (temperatura, luz, pressão etc.) e controlar outros circuitos (lâmpadas, motores, eletrodomésticos etc.), dentre outras coisas que não conseguiríamos diretamente com um PC. A grande, diferença com relação ao uso desses dispositivos, no caso do Arduino, é que, na maior parte das vezes, nós mesmos construímos os circuitos que são utilizados, ou seja, não estamos limitados apenas a produtos existentes no mercado: o limite é dado por nosso conhecimento e criatividade!

O melhor de tudo nesse projeto é que seu _software_, _hardware_ e documentação são abertos. O _software_ é livre (GNU GPL[^6]), o _hardware_ é totalmente documentado(basta entrar no site e baixar os esquemas) e a documentação está disponível em Creative Commons[^7] -- os usuários podem colaborar (seja escrevendo documentação, seja traduzindo) através da wiki!

*   *   1.  Instalação do Software

Como qualquer computador, o Arduino precisa de um software para funcionar e para desenvolvermos este software podemos usar a IDE que tem o mesmo nome. Esse software será desenvolvido utilizando a linguagem C++ ou no caso da IDE do Arduino o dialeto Wiring que facilita muito a programação, já que é um C/C++ simplificado com um framework, contribuindo com diversas funções e tipos de dados úteis para uso com o Arduino..

Após escrever o código, o compilaremos e então faremos o envio da versão compilada para a memória flash do Arduino, através da porta USB. A partir do momento que o _software_ é gravado no Arduino não precisamos mais do PC: O Arduino, como é um computador independente, conseguirá sozinho executar o software que criamos, desde que seja ligado a uma fonte de energia.

Visite o link [http](http://arduino.cc/en/Main/Software)[://](http://arduino.cc/en/Main/Software)[arduino](http://arduino.cc/en/Main/Software)[.](http://arduino.cc/en/Main/Software)[cc](http://arduino.cc/en/Main/Software)[/](http://arduino.cc/en/Main/Software)[en](http://arduino.cc/en/Main/Software)[/](http://arduino.cc/en/Main/Software)[Main](http://arduino.cc/en/Main/Software)[/](http://arduino.cc/en/Main/Software)[Software](http://arduino.cc/en/Main/Software) para baixar o arquivo.

Antes de iniciar nosso projeto precisamos então instalar a IDE. Vamos lá:

*   **Ubuntu GNU/Linux 10.10 ou superior**: Basta executar em um terminal:

**sudo aptitude install arduino**

ou procurar pelo pacote “arduino” no Synaptic (menu Sistema -> Administração -> gerenciador de pacotes Synaptic).

abaixo segue algumas telas caso opte em instalar pela linha de comando:

|  |  |
| --- | --- |
|  |  |
| Instalando a IDE do Arduino no Ubuntu |

*   **Ubuntu GNU/Linux (anterior a 10.10)**: Consulte a página de instalação do Arduino em Ubuntu[^8]
*   **Outras distribuções GNU/Linux**: Consulte a página de instalação em outras distribuições GNU/Linux[^9].
*   **Microsoft Windows**: Consulte a página de instalação para as variadas versões do Microsoft Windows[^10].
*   **Apple MAC OS X**: Consulte a página de instalação para o Mac OS X[^11].

Obs: Em nosso curso em temos alguns módulos o ideal é utilizar a versão disponível em [http](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[://](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[www](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[.](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[carlosdelfino](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[.](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[eti](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[.](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[br](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[/](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[downloads](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[/](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[viewcategory](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[/11-](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos)[duinos](http://www.carlosdelfino.eti.br/downloads/viewcategory/11-duinos) .

Após a instalação, abra a IDE (no Ubuntu GNU/Linux ela estará disponível no menu _Aplicativos → Eletrônica → Arduino IDE)_. Uma tela similar à abaixo será mostrada:

|  |
| --- |
| **_~~Figura 1.2: Arduino IDE Versão 1.5.0 rodando no MAC OS X~~_** |

*   *   1.  O Software Fritzing

Fritzing é o melhor e mais fácil software para desenho auxiliado por computador especializado em Eletrônica. Com este software podemos desenhar nossos projetos com o Arduino como se tivéssemos montando o mesmo em uma protoboard, ou desenhar o projeto usando um esquema de componentes, e finalmente teremos em mãos a placa para pronta para enviar ao fabricante de PCB ou imprimirmos aqui mesmo. Aqueles que desejam fazer suas próprias PCB em casa, podem usar o seguinte artigo:

[http](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[://](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[www](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[.](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[carlosdelfino](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[.](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[eti](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[.](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[br](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[/](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[eletronica](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[/](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[item](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[/49-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[como](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[fazer](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[uma](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[pcb](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[placa](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[de](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[circuito](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[impresso](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[com](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[impressora](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[-](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)[laser](http://www.carlosdelfino.eti.br/eletronica/item/49-como-fazer-uma-pcb-placa-de-circuito-impresso-com-impressora-laser)

A instalação do Software Fritzing[^12] é bem simples, começamos baixando o software disponível nos links abaixo conforme o sistema operacional:

*   Windows:[http](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[://](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[fritzing](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[.](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[org](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[/](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[download](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[/0.7.12](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[b](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[/](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[windows](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[/](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[fritzing](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[.2013.02.25.](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[pc](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[.](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)[zip](http://fritzing.org/download/0.7.12b/windows/fritzing.2013.02.25.pc.zip)
*   MacOS 10.5:[http](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[://](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[fritzing](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[.](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[org](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[/](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[download](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[/0.7.12](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[b](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[/](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[mac](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[-](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[os](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[-](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[x](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[-105/](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[fritzing](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[.2013.02.25.](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[cocoa](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[.](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)[dmg](http://fritzing.org/download/0.7.12b/mac-os-x-105/fritzing.2013.02.25.cocoa.dmg)
*   Linux 64 Bits:[http](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[://](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[fritzing](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[org](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[download](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[/0.7.12](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[b](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[linux](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[-64](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[bit](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[fritzing](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[-0.7.12](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[b](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[linux](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[AMD](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[64.](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[tar](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[bz](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)[2](http://fritzing.org/download/0.7.12b/linux-64bit/fritzing-0.7.12b.linux.AMD64.tar.bz2)
*   Linux 32 Bits:[http](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[://](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[fritzing](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[org](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[download](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[/0.7.12](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[b](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[linux](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[-32](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[bit](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[/](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[fritzing](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[-0.7.12](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[b](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[linux](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[i](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[386.](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[tar](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[.](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[bz](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)[2](http://fritzing.org/download/0.7.12b/linux-32bit/fritzing-0.7.12b.linux.i386.tar.bz2)

Abaixo podemos ver uma janela do Fritzing em execução:

|  |
| --- |
| Fritizing em Execução |

Existem outros softwares para confecção de placas um dos melhores da atualidade é o Proteus, que inclusive tem o recurso de emulação, aqueles que quiserem experimentar o Proteus com o Arduino podem baixar a seguinte biblioteca:

Link: [http://www.carlosdelfino.eti.br/arduino/usando-o-arduino-em-seus-projetos-no-proteus](http://www.carlosdelfino.eti.br/arduino/usando-o-arduino-em-seus-projetos-no-proteus)

A Arquitetura do Arduino

A arquitetura do Arduino é influenciada diretamente pelo microcontrolador usado, há alguns itens de sua estrutura que são comuns entre cada modelo, apresentarei abaixo um sumário do Arduino UNO R3 e de seu microcontrolador.

Resumo da arquitetura Arduino Uno

Abaixo está o resumo da arquitetura para o Arduino UNO R3.

| **_~~Recurso~~_** | **_~~Descrição~~_** |
| --- | --- |
| **_~~Microcontrolador~~_** | **_~~ATmega328~~_** |
| **_~~Voltagem padrão de Operação~~_** | **_~~5V~~_** |
| **_~~Nível de voltagem de entrada recomendado~~_** | **_~~7 a 12V~~_** |
| **_~~Limites de Voltagem de entrada~~_** | **_~~6-20V~~_** |
| **_~~Pinos de Entrada e Saída Digital~~_** | **_~~14 (sendo 6 com saída PWM) + 6 compartilhadas com as entradas Analógicas.~~_** |
| **_~~Pinos de Entrada Analógica~~_** | **_~~6 (que também podem ser usadas como digital)~~_** |
| **_~~Limite de corrente por saída 5V~~_** | **_~~40mA~~_** |
| **_~~Limite de corrente por saída 3.3V~~_** | **_~~50mA~~_** |
| **_~~Memória Flash (Memória de programa)~~_** | **_~~32KB, sendo que 0.5KB é usado pelo Bootloader do Arduino.~~_** |
| **_~~SRAM (Memória de dados)~~_** | **_~~2KB~~_** |
| **_~~EEPROM~~_** | **_~~1KB~~_** |
| **_~~Clock~~_** | **_~~16Mhz~~_** |

|  |
| --- |
| **Illegal nested table :** Illustration 1: Arquitetura Geral do Arduino |

*   *   *   1.  Arquitetura do Arduino Leonardo

*   *   *   1.  Arquitetura Especifica do ATMega

Os chips da linha ATMega tem uma arquitetura padrão entre eles, principalmente no que se refere aos registradores, tipo e uso das memórias, e principalmente em relação a CPU, variando entre os modelos alguns detalhes, como o número de registradores, os registradores de portas de saída e entrada, os registradores de interrupção, e principalmente a quantidade de memória.

A arquitetura AVR que é usada por todos os chips da linha ATmega, ATtiny e ATXmega é uma variação da arquitetura Havard[^13] que é uma arquitetura que define a organização da comunicação da memória com a CPU, ALU (ULA) e os registrados.

Segue abaixo um gráfico da Arquitetura dos Chips ATMega em especial o ATmega328P usado no Arduino UNO, não se assuste, alguns em um primeiro instante pode se sentir confuso com tantos blocos, por isto logo em seguida apresento um diagrama mais simples.

|  |
| --- |
|  |

|  |
| --- |
|  |

|  |
| --- |
| **_~~Diagrama de Blocos Geral do ATMega328[^14]~~_** |

|  |
| --- |
| Figuras 1: Um outro Diagrama mais colorido, por funcionalidade das portas. |

Diferenças entre MicroControladores e Processadores

A diferença entre Microcontroladores e Processadores está principalmente no fato do Microcontrolador possuir periféricos construídos internamente ao chip, como memória RAM, conversores analógicos digitais, portas seriais de comunicação, dentre outros recursos, tudo fabricado em uma mesma pastilha do chip. Em contra partida os Processadores possuem tais periféricos agregados externamente, em chip extra, o que lhe oferece uma grande possibilidade de expansão.

Os Microcontroladores como o ATmega2560 permite a expansão de sua memória RAM externamente, o que lhe dá certa flexibilidade e possibilidade de ampliar sua capacidade de tratar com dados mais complexos.

Há também a possibilidade de uso de portas seriais como a TWI/I2C para instalar outros recursos porém reduzindo o desempenho do Microcontrolador, mas sem perder sua escalabilidade.

Os microcontroladores também possuem um conjunto de instruções assembler focadas no acesso e controle das portas e respectivos registradores, oferecendo assim uma maior facilidade para controlar os dispositivos.1.4.3 Tipos de Arduino

*   *   1.  Modelos do Arduino, Similares e Clones

Existem diversos modelos de Arduino, podendo cada um ser usado em situações bem especificas, os mais conhecidos são o Arduino Uno e o Arduino Mega, um bastante interessante e o Leonardo que permite o desenvolvimento de periféricos que se comportem como Teclado ou Mouse em relação ao Host (Computador), o Esplora que visa ser um controle tipo joystick que pode ser usado para desenvolver soluções de interatividade para games e movimento.

Os demais são variações com mais ou menos recursos, ou mudança em seu tamanho, com ou sem adaptadores USB já inclusos.

| [^15] | [^16] | [^17] | [^18] |
| --- | --- | --- | --- |
| **_~~Arduino Leonardo~~_** | **_~~Arduino Due~~_** | **_~~Arduino Esplora~~_** | **_~~Arduino Mega 2560~~_** |

| [^19] | [^20] | [^21] | [^22] |
| --- | --- | --- | --- |
| **_~~Arduino Mega SDK~~_** | **_~~Arduino Ethernet~~_** | **_~~Arduino Mini~~_** | **_~~Arduino Micro~~_** |

| [^23] | [^24] | [^25] |  |
| --- | --- | --- | --- |
| **_~~Arduino Uno~~_** | **_~~Arduino Pro Mini~~_** | **_~~Arduino Pro.~~_** |  |

| **_~~[^26]~~_** | [^27] |  |  |
| --- | --- | --- | --- |
| **_~~Arduino Fio~~_** | **_~~Arduino Nano~~_** |  |  |

Há dois que foram lançados recentemente e já estão a venda, o Arduino Robot para aprendizagem de robótica. e o Arduino Yun que vem integrado com um Roteador da linha Open WRT (roteadores wilress de tecnologia aberta baseado no Linux) e usa o mesmo microcontrolador adotado pelo Arduino Leonardo, este já vem com uma placa Wi-FI.

| [^28] |
| --- |
| **_~~Arduino Robot~~_** |

| [^29] |
| --- |
| **_~~Arduino YUN~~_** |

E como já foi comentado, a cada período há sempre novas propostas, e o que era novo, se torna padrão e surgem novas placas que tornam o Arduino insuperável, como o Arduino TRE e o Arduino Intel Galileo, este certificado pela Intel com um processador capaz de rodar o Linux mais um microcontrolador integrado similar ao usado no Arduino Leonardo.

O Arduino LIlyPad[^30] é um dispositivo interessante para uso no artesanato existindo inclusive uma loja feminina[^31] especializada em soluções para este mercado, conhecido como E-Textile[^32].

Além do LilyPad que é a opção mais conhecida, há outras soluções E-Textile como a "Flora**_~~[^33]~~_**", “Fabrick[^34]" e Seeeduino Clio**_~~[^35].~~_**

**_~~O Arduino LilyPad possui dois modelos, o Arduino LilyPad que precisa de um adaptador serial ttl para usb e o Arduino LilyPad USB que já vem com a porta USB integrada.~~_**

| [^36] | [^37] | **_~~[^38]~~_** | **_~~[^39]~~_** |
| --- | --- | --- | --- |
| Arduino LilyPad | Arduino LilyPad USB | Flora -Adafruit | Seeeduino Clio |

Da lista dos Arduino da Seeed Studio temos o Seeeduino Clio, uma versão artistica do Arduino.

E completando a linha E-Textile temos o Fabrick. E temos também o Seeeduino Filme, feito sobre um circuito flexivel.

| [^40] | [^41] |
| --- | --- |
| Fabrick | Arduino Filme |

*   *   *   1.  Versões de Arduinos Certificados

Agora é possível certificar sua placa de protótipos como sendo um produto compatível com o Arduino. Atualmente[^42] somente uma placa de protótipos está certificada, esta foi produzido pela Intel e é chamada de Intel Galileo

| [^43] |
| --- |
| Arduino Galileo |

*   *   *   1.  Alguns Clones e Plataformas compatíveis

Além dos tipos de Arduino diferentes, como Arduino Leonardo, Arduino Mega, e até mesmo de outros fabricantes como as propostas da SeeedStudio, variações da Adafruit, temos também outros clones e plataformas compatíveis, algumas que permite até mesmo o aproveitamento dos Shields, o que não é 100% garantido.

| **_~~[^44]~~_** | **_~~[^45]~~_** |
| --- | --- |
| **_~~Mapple da LeafLabs~~_** | **_~~Sanguino~~_** |
| **_~~[^46]~~_** |  |
| **_~~PICDuino~~_** |  |

Temos também o PC-Duino é uma proposta que soma os recursos de um PC baseado em ARM A8 a um Arduino, porém não é 100% compatível, tudo indica não ser nada compatível.

| **_~~[^47]~~_** |
| --- |
| **_~~PC-Duino~~_** |

Primeiro Projeto

Quando ensinamos linguagem de programação para iniciantes, geralmente o primeiro exemplo é um _hello word_. Como o Arduino não vem por padrão com um display, nosso primeiro exemplo será fazer um LED piscar -- e por isto será chamado _blink_. Nosso LED ficará acesso durante um segundo e apagado durante outro segundo e então recomeçará o ciclo. Abra o IDE e digite o seguinte código:

| **_~~void setup(){~~_** |
| --- |
| **_~~Código 1.1 - Blink~~_** |

Chamamos um código feito para Arduino de _sketch_ e o salvamos em um arquivo com a extensão **.ino**. Nas versões anteriores a **IDE 1.0** do Arduino a extensão era **.pde**, herdada da IDE do Processing/Wiring, um dialeto (ou seria um framework?) Java usado para interagir com o Arduino no PC, este tema faz parte de um dos cursos avançados do Arduino.

Com nosso _sketch_ pronto, bastará conectar o Arduino na porta USB e clicar no botão _upload/carregar_ (segundo da esquerda para a direita, uma seta apontando para a direita). Após o processo, será vista a mensagem “_Done uploading_”, na parte inferior da IDE e então o _sketch_ estará rodando no Arduino, ou seja, o LED acenderá e apagará, de 1 em 1 segundo.

O Arduino possui 14 portas digitais, que podemos utilizar como entrada ou saída. nesse caso, vamos utilizar a porta de número 13 como saída, dessa forma, podemos controlar quando a porta ficará com 5V ou quando ficará com 0V -- internamente o Arduino possui um LED conectado à porta 13 e , por isso, teremos como “ver” nosso _software_ funcionando.

Para que nosso _software_ funcione corretamente no Arduíno, precisamos criar duas funções especificas: setup e loop. A função setup é executada assim que o Arduíno dá boot, já a função loop fica sendo executada continuamente (em _loop_) até que o Arduíno seja desligado. como as portas digitais são de entrada ou saída, definimos então dentro da função setup que a nossa porta 13 é uma porta de saída -- fazemos isso através da chamada à função pinMode, que já vem na biblioteca padrão do Arduíno.

Depois de configurarmos corretamente a porta 13 como saída, precisamos acender e apagar o LED que está conectado a ela. para alterar a tensão na porta, utilizamos a função digitalWrite (que também está na biblioteca padrão do Arduíno); passamos para essa função a porta que queremos alterar a tensão e o novo valor de tenção (HIGH = 5V, LOW = 0V). Depois das chamadas para acender e apagar o LED, chamamos a função delay passando o parâmetro 1000 -- o que essa função faz é esperar um tempo em millisegundos para então executar a próxima instrução.

Deve-se ressaltar que a IDE Arduíno inclui automaticamente todas as bibliotecas que utilizamos. Se você está acostumado com C/C++, note que não precisamos digitar as diretivas include para arquivos como o stdlib.h, por exemplo. Tudo é feito de forma automática para facilitar o desenvolvimento do projeto!

Como o Arduíno já vem com um LED internamente conectado à porta 13, não precisaremos de circuitos externos para que esse projeto funcione, ou seja, bastará fazer _upload_ daquele código e já teremos o resultado esperado:

|  |  |
| --- | --- |
| **_~~LED 13 Apagado~~_** | **_~~LED 13 Acesso~~_** |
| **_~~Figura 1.3: Arduino UNO R3 rodando o exemplo Blink~~_** |

Porém, se quisermos acender um LED externo à placa, podemos conectá-lo diretamente à porta 13\. Podemos utilizar um LED de 5mm que acende com 2,5V e tem um consumo de 20mA. O problema, nesse caso, se dá por conta da porta digital: ela assume ou a tensão 0V, ou a tensão 5V -- e caso coloquemos 5V no LED ele irá queimar..

**_Obs. Você terá sucesso ao ligar os LEDs diretamente na porta do Arduíno, porém o risco é alto evite desafiar as Leis da Física, elas costumam ser implacáveis. A porta do Arduíno é capaz de atender 40mA de carga, a maioria dos LEDs precisam de apenas 20mA e podem se queimar também, mas há LEDs que demandam uma corrente maior e ai o risco é de queimar a porta do controlador do Arduino._**

Para solucionar esse problema precisamos ligar algum outro componente que seja responsável por dividir parte dessa tensão com o LED, para que ele não queime, então utilizaremos um resistor. Portando, ligamos um resistor de 120Ω (ohms) em série com o LED, o resistor à porta 13 e o LED à porta GND - _ground_ ou terra – como na Figura 1.4.

|  |
| --- |
| **_~~Figuras~~ _**2**_~~: Utilizando um LED Externo para o exemplo Blink~~_** |

Não precisamos fazer nenhuma alteração no software para que esse circuito funcione: basta ligar o Arduino na porta USB do computador, para que o computador dê energia ao circuito, e então veremos o LED externo piscar juntamente com o LED interno. Em vez do LED, poderíamos controlar outros componentes, como motores, eletrodomésticos etc.

Alimentação do Circuito

Internamente, o circuito do Arduíno funciona na versão UNO e Mega, com uma tensão de 5V. Quando ligamos o Arduíno em uma porta USB do PC, o próprio PC, através do cabo USB, alimenta o Arduíno. Porém, nem sempre tempos um PC por perto; para esses casos, podemos utilizar uma outra fonte de energia de 5V (a fonte deve ser ligada diretamente nos pinos “Vin” e GND do Arduino).

Como não possuímos pillhas/baterias em abundância no mercado com tensão de 5V, fica complicado alimentar um Arduíno dessa forma -- se tivermos uma tomada de 127/220VAC por perto, poderíamos ligar uma fonte AC/DC (essas sim, existem aos montes). para resolver esse problema, o Arduíno possui um regulador de tensão que aceita tensões de 7 a 12V (na verdade, ele consegue funcionar com tensões entre 6 e 20V, apesar de não recomendado). Com o regulador de tensão podemos combinar pilhas em série, ou utilizar uma bateria de 9V ou mesmo baterias de carros, motos e no-breask (12V).

|  |
| --- |
| **_~~Figuras~~ _**3**_~~: Arduino alimentado por uma bateria de 9V~~_** |

*   *   *   1.  Cálculos de resistência e LED

Continuando nossa parte introdutória do curso, para acendermos o LED precisamos de um Resistor que irá controlar a corrente, já que os LEDs tem esta limitação, vejamos a seguir algumas informações iniciais sobre resistência, potenciometros e LDR que serão usados na primeira fase de aprendizado.

*   *   *   *   1.  Visão rápida sobre Resistências, Potenciometros e LDR

Resistores

Resistores são componentes que oferecem como seu nome sugere resistência a tensão limitando assim a corrente que irá passar, os resistores podem ser usados para limitar a corrente e como divisores de tensão, permitindo assim obter frações da tensão fornecida, os potenciometros são uma forma de uso de divisores de tensão reguláveis.

Potenciometros

Potenciometros são Resistores variáveis, na figura ao lado é apresentado um potenciometro, há diversos modelos e alguns são chamados de Trimpot que tem origem no nome "Trimmer Potenciometer", os Trimpots são potenciometros miniaturas, e usados para ajustar a placa e não sofrer constante alterações..

|  |
| --- |
| **_~~Illustration~~ _**2**_~~: Desenho de um potenciometro desmontado~~_** |

Há Trimpots de precisão possuem uma dezena de voltas, permitindo assim uma grande gama de ajuste em seu valor.

LDR

Já os LDR da Sigla de Light Dependent Resistor, é um resistor que sofre interferência conforme a incidência da luz. São muito utilizados para controlar as luzes presentes nos postes, que acendem a luz da rua com a ausência da luz do dia. Claro nos postes são usados componentes maiores e adequados a tensão ali presente, no nosso caso usaremos pequenos LDRs que atendem perfeitamente a nossa necessidade de aprendizado.

|  |
| --- |
| **_~~Illustration~~ _**3**_~~: Desenho demonstrando um LDR~~_** |

*   *   *   *   1.  Visão rápida sobre LEDs

Os LEDs são componentes construídos sobre silício com as características equivalentes aos Diodos, ou seja conduzem energia somente em uma direção, porém emitem Luz quando atingem sua tensão limite, a utilização de LEDs demanda resistores para limitar a corrente, uma vez que ultrapassando o limite de corrente queimarão com o super aquecimento.

|  |
| --- |
| Figuras 4: Alguns tipos de LEDs facilmente encontrados no nosso mercado. |

Como pode ser visto na figura acima há LEDs de diversas cores, inclusive multicoloridos, ou seja, LEDs com as três cores padrões que combinadas pelo controle da corrente em cada pino pode se obter outras cores, estes LEDs são conhecidos como RGB.

Os LEDs tem o mesmo símbolo dos diodos porém acrescido de duas setas para fora, apontando que emitem Luz.

Como os diodos os LEDs são polarizados e normalmente tem seu Cátodo conectado ao Terra diretamente, e seu Anoto a um resistor especialmente calculado, que é ligado ao VCC de seu circuito ou a uma fonte de tensão compátivel.

Veja na próxima seção como calcular o resistor para uso com seu LED.

*   *   *   *   1.  Cálculo do Resistor

Para usar LEDs com Arduíno precisamos fazer algumas contas (e arredondamentos). Vamos aprender agora a calcular o valor dos resistores que precisamos utilizar. Se precisarmos acender um LED verde, que é alimentado com tensão de 2,2V e corrente de 20mA através do Arduíno, precisaremos de um resistor, como já vimos, já que o Arduíno consegue fornecer ou 0V ou 5V, colocaremos um resistor em série com o LED, e com isso podemos concluir que:

*   A tensão total (soma das tensões no resistor e no LED) será de 5V, ou seja:
*   A corrente total que passa pelo resistor e pelo LED é igual, ou seja, 20mA, ou seja:
*   Precisamos colocar uma tensão de 2,2V no LED, ou seja:

Sabendo desses detalhes, podemos concluir que a tensão no resistor será de: .

Como e , podemos calcular o valor da resistência R do resistor que iremos utilizar através da Lei de Ohm que pode ser vista no triangulo abaixo:

Como queremos saber o valor de R, usaremos a formula:

Assim, temos:

Depois de feito o cálculo, podemos generalizar com a seguinte fórmula:

Para o LED verde, precisamos de um resistor de 120, porém não existem resistores com esse valor para venda -- os valores são predefinidos[^48]. Data essa situação, temos duas alternativas

*   Utilizar um resistor de maior resistência e limitar mais a corrente (que fará com que o LED brilhe menos);
*   Associar dois ou mais resistores em série ou paralelo para conseguir o valor mais próximo possível.

Geralmente escolhemos um resistor de valor próximo, já que uma alteração pequena de corrente não causará danos ao dispositivo, porém em alguns casos precisaremos combinar resistores de valores diferentes para conseguir o valor equivalente -- esse tema será explicado em mais detalhes no próximo capítulo.

Bibliotecas e Shields

Assim como a IDE já vem com diversas funções pré-definidas, o Arduino possui outras bibliotecas para controle de servomotores, displays LCD, geração de áudio, recepção de sinais de sensores e outros dispositivos (como teclado PS/2), dentre muitas outras coisas! E quem pensa que essa extensibilidade toda se restringe à parte de _software_ está muito enganado: o Arduino possui o que chamamos de _shields_, que são placas que se acoplam à placa original, agregando funcionalidades à mesma.

Existem _shields_ dos mais variados tipos, para as mais diversas funções. Alguns servem como entrada, outros como saída, e ainda outros como entrada e saída. Com os _shields_ conseguimos, por exemplo, fazer o Arduino se comunicar numa rede Ethernet, ou ainda transmitir dados para qualquer dispositivo via Bluetooth, Wi-Fi ou ZigBee. Existem shields com circuitos integrados prontos para controlarmos motores sem que precisemos nos preocupar com complicações eletrônicas envolvidas, outros possuem leitor de cartão SD, acelerômetros, GPS e diversos outros sensores que podem gerar dados importantes para o _software_ que está rodando no microcontrolador.

|  |
| --- |
| **_~~Figuras~~ _**5**_~~: Arduino UNO R3 com um Shield GSM/GPRS~~_** |

Existem também outros _shields_ mais elaborados, que são sistemas completos. Um deles, por exemplo, cria uma plataforma para desenvolvimento de jogos no Arduino: o Video Game Shield[^49], que possui uma saída RCA e duas entradas para controles Numchuck do Nintendo Wii. Além do _hardware_, existe uma biblioteca para ser utilizada em conjunto, que já possui várias funções pré-programadas para fazermos desenhos na televisão e capturar os dados dos movimentos nos controles.

*   *   *   1.  Alguns Shields

| [^50] | [^51] | [^52] |
| --- | --- | --- |
| **_~~Arduino GSM Shield~~_** | **_~~Arduino Ethernet Shield~~_** | **_~~Arduino Wi-Fi Shield~~_** |
| [^53] | [^54] | [^55] |
| **_~~Arduino Wireless Shield~~_** | **_~~Arduino Motor Shield~~_** | **_~~Arduino Proto Shield~~_** |

Integração com o PC

Apesar de o Arduino ser um computador independente, em alguns casos podemos nos aproveitar de um PC por perto e explorar outra funcionalidade muito interessantes para alguns projetos: o Arduino consegue conversar com o computador através da porta USB. isso nos permite desenvolver um _software_ que roda no PC e se comunica com o _software_ que roda no Arduino, o que nos abre um mar de possibilidades! Podemos, por exemplo, criar um _software_ em Python[^56] que recebe os dados de um sensor (por exemplo: um sensor de umidade), via USB (através do Arduino), e envia para algum banco de dados na Internet (por exemplo: o Serviço Cosm[^57])-- assim teremos, de certa forma, nosso Arduino online, enviando dados para o mundo, através de um PC!

Existem inúmeros projetos interessantes que fazem interface entre linguagens de programação e o Arduino -- existem implementações para Python, Ruby, Java, C, dentre outras linguagens. E não para por aí: além de o _software_ que roda no PC para receber dados e processa-los, é possível também enviar dados, controlando o Arduino! Dessa forma podemos, por exemplo, receber dados da Web e enviar comandos ao Arduino, baseados nesses dados.

um exemplo de aplicação que utiliza a porta USB para comunicação do Arduino com o PC é o projeto Arduinoscope[^58], que tem como finalidade criar um osciloscópio, onde podemos ver em tempo real, no PC gráficos das tensões que estão ligadas as portas analógicas do Arduino. Outro exemplo é um projeto criado pelo autor original desta apostila Alvaro Justen onde se controla um carrinho através de Wi-Fi, o Turiquinhas[^59], ou outro projeto criado pelo editor atual desta apostila uma cadeira de Rodas Inteligente, que busca reduzir os impactos de manobras acidentais pro cadeirantes (Portadores de Deficiência como Semi Tetraplégicos).

**_Fica a dica:_** para quem quer começar um projeto Arduino assistido por computador de maneira fácil: vale a pena estudar um protocolo de comunicação e controle chamado Firmata[^60], cuja implementação está disponível para várias linguagens (e já vem por padrão um exemplo na IDE do Arduino). Ele facilita o processo de aquisição de dados e controle da placa.

Outra ferramenta interessante para pre-adolescentes e jovens, é o S4A[^61] que é um tipo de software que une os recursos do Scratch com o Arduino permitindo a programação através de símbolos.

Processing

O Processing[^62] é um Framework que é muito semelhante com o que utilizamos no Arduíno, que consegue se comunicar com o Arduíno via USB (ou porta serial) e é utilizada para criar imagens, animações e interações no PC, a partir dos dados vindos da comunicação com o Arduíno, incluindo a IDE é bem similar, se não a mesma.

O Processing é um projeto Aberto iniciado por Casey Reas e Ben Fry, ambos membros do Grupo de Estética e Computação no Laboratório de Midia do MIT.

Abaixo um projeto de medição de potência tendo sua interface desenvolvida com Processing:

|  |
| --- |
| **_~~Figuras~~ _**6**_~~: Osciloscópio com Processing~~_** |

Instalando o Processing

A instalação do Processing é bem simples, basta acessar o link: [http](http://processing.org/download/)[://](http://processing.org/download/)[processing](http://processing.org/download/)[.](http://processing.org/download/)[org](http://processing.org/download/)[/](http://processing.org/download/)[download](http://processing.org/download/)[/](http://processing.org/download/) e baixar o pacote para seu Sistema Operacional, procure baixar a versão 1.5.1, como a versão 2.0 ainda está em desenvolvimento é melhor aguardar a versão final.

A instalação no MAC OSX é bem simples bastando descompactar o pacote baixado e copiar o arquivo "Processing.app" para a pasta Applications.

Já no Windows, o processo é semelhante, descompacte o arquivo zip baixado e copie a pasta criada para o local que deseja instalar o Processing.

No Linux, o processo também é o mesmo para Windows, baixe o arquivo TGZ, descompacte e mova a pasta para um local que achar mais adequado para instalar os arquivos do Processing.

Coloque no PATH para facilitar a execução.

Portas analógicas e digitais

O Arduíno possui dois tipos de portas de entrada: analógicas e digitais. Além disso, as portas digitais também servem como portas de saída, funcionando com dois tipos básicos de saída: saída digital comum e saída PWM -- o PWM pode ser utilizado para simular uma saída analógica, dentre outras coisas.

Portas digitais

Utilizaremos as portas digitais quando precisarmos trabalhar com valores bem definidos de tensão. Apesar de nem sempre ser verdade, geralmente trabalharmos com valores digitais binários, ou seja, projetamos sistemas que utilizam apenas dois valores bem definidos de tensão. Existem sistemas ternários, quaternários, mas focaremos no binário, já que é esse o utilizado pelo Arduíno.

Como o sistema é binário, temos que ter apenas duas tensões. São elas: 0V e 5V. Dessa forma, as portas digitais do Arduino podem trabalhar apenas com essas duas tensões -- e o _software_ que desenvolveremos poderá requisitar ao microcontrolador do Arduino que:

*   Coloque uma determinada porta em 0V;
*   Coloque uma determinada porta em 5V;
*   leia o valor de uma terminada porta (terá 0V ou 5V como resposta).

O Arduíno UNO possui 14 portas digitais que estão destacadas na figura a seguir:

|  |
| --- |
| **_~~Figuras~~ _**7**_~~: Portas digitais do Arduino, de 13 a 0~~_** |

Apesar de ser possível, não é recomendável utilizar as portas 0 e 1 pois elas estão diretamente ligadas ao sistema de comunicação do Arduino (pinos RX e TX - recepção e transmissão, respectivamente) e, por isso, seu uso pode conflitar com o upload do _software_. Caso queira utiliza-las, certifique se de desconectar quaisquer circuitos conectados a ela no momento do _upload_.

Utilizaremos as funções digitalRead e digitalWrite para ler e escrever, respectivamente, nas portas digitais. A função digitalWrite já foi exemplicada em nosso exemplo _Blink_, onde acendemos e apagamos um LED ao alternar a tensão da porta 13 entre 5V e 0V, com intervalo de 1 segundo. Para exemplificar a função digitalRead utilizaremos um botão, como no digrama a seguir que amplia o diagrama anteriormente apresentado:

|  |
| --- |
| **_~~Figuras~~ _**8**_~~: Esquema elétrico ligando um botão ao Arduíno.~~_** |

Uma vez o circuito acima esteja montado, vamos programar o Arduíno com o seguinte código:

| **_~~#define BOTAO 7~~_** |
| --- |
| **_~~Código_Fonte~~ _**1**_~~: Código de controle de um Led pelo Botão~~_** |

A função digitalRead nos retorna o estádo da porta correspondente com referência à tensão que está na porta que passamos entre parenteses. Em nosso exemplo, utilizamos a porta BOTAO (que na verdade [e uma constante, definida através da diretiva #define), cujo valor é 2\. O valor retornado [e uma constante, mapeado da seguinte forma:

*   HIGH, caso a tensão na porta seja 5V;
*   LOW, caso a tensão na porta seja 0V;

O que o programa faz, então, e apagar o LED caso o botão esteja pressionado e acendê lo caso não esteja. Fica como exercício entender o código a seguir, que é uma otimização do anterior e possui mesma funcionalidade:

| **_~~#define BOTAO 2~~_** |
| --- |
| **_~~Código_Fonte~~ _**2**_~~: Fonte 1.3 - Outro Código de controle de um Led pelo Botão~~_** |

Dica: o caracter "!", em linguagem C, significa "_not"_ e tem como finalidade negar a expressão que segue à sua direita.

*   *   *   *   1.  Schmitt Trigger e portas digitais do Arduíno

O Schmitt-Trigger é um tipo de circuito que mantém seu valor de saída após a entrada atingir um certo nível de tensão, dai vem seu nome Trigger, mas ele tem uma característica extra que é chamada de Hysterese, que intencionalmente é adicionado de forma a gerar um certo retardo em sua reação evitando assim que ruídos provoquem o chaveamento do estado da saída.

|  |
| --- |
|  |

O valor mínimo para que a porta seja considerado o estado 0 (LOW) deve ser -0.5V (negativo) e o valor máximo para manter neste estado deve ser o valor 0.3V (positivo).

Já o valor mínimo para que a porta seja mantida no estado 1 (HIGH) é 0.6V (positivo) e o valor máximo será a tensão de alimentação do chip + 0.5V (positivo), ou seja considerando o fato que o chip ATmega328 ou ATmega2560 no Arduino é alimentado com 5.0V o limite será de 5.5V(positivos).

*   *   *   *   1.  PWM

PWM significa Modulação por Largura de Pulso (Pulse-Width Modulation, do Inglês) e consiste em manipularmos a razão cíclica de um sinal (conhecida do Inglês como _duty cycle)_ a fim de transportar informa;áo ou controlar a potência de algum outro circuito. Basicamente, teremos um sinal digital que oscila entre 0V e 5V com determinada frequência (o Arduíno trabalha com um padrão perto de 500Hz) -- funciona como se fosse um _clock_, porém os tempos em que o sinal permanece em 0V e 5V podem ser diferentes. "_Duty cycle"_ é a razão do tempo em que o sinal permanece em 5V sobre o tempo total de uma oscilação. A Figura 1.9 ilustra melhor esse conceito:

|  |
| --- |
| **_~~Figura 1.9: Sinal PWM com duty cycle de 25%~~_** |

Assim, temos:

O que controlamos através de _software_ é justamente a "_duty cycle"_, o percentual de tempo em que o sinal fica em 5V. Dessa forma, podemos utilizar essa técnica para limitar a potência de algum circuito. Por exemplo, considere que um LED L<sub>1</sub> seja alimentado o tempo inteiro por um sinal constante de 5V já o LED L<sub>2</sub> é alimentado pelo sinal PWM acima (_duty cycle_ de 25%). Através de um cálculo simples de potência podemos notar que o LED L<sub>2</sub> consumirá apenas 25% da potência do primeiro.

Infelizmente, por limitações de _hardware_, o Arduino UNO não possui PWM em todas as portas digitais: apenas as portas 3, 5, 6, 9, 10 e 11 são privilegiadas e podem utilizar esse recurso. Para exemplificar o uso de controle de potência de um circuito utilizando PWM vamos utilizar um LED em série com um resistor ligados à porta 11 (o circuito é o mesmo do experimento _Blink_, só vamos mudar a porta) e o seguinte código:

| **_~~#define LED 11~~_** |
| --- |
| **_~~Fonte 1.4 - Exemplo de código usando porta PWM~~_** |

Na função _loop_ acima temos um laço for, que conta de 0 a 255 (armazenando o valor do contator na variável i), chamando a função analogWrite (passando como parâmetro a porta do LED (11) e _i_) e esperando 30 milissegundos a cada interação.

A função analogWrite (apesar de estamos utilizando uma porta digital) é responsável pelo PWM e recebe como parâmetros a porta e um valor entre e 255 -- esse valor corresponde ao _duty cycle_, onde 0 responde a 0% e 255 a 100%. quando você rodar o código perceberá qe o LED acende de maneira mais suave -- cada etapa de luminosidade diferente corresponde a uma interação do for. Fica como exercício para o leitor modificar o programa para que o LED, além de acender, também apague suavemente. ;)

Portas analógicas

Além das portas digitais o Arduíno possui portas analógicas. Ao contrário das portas digitais que são de entrada e saída, as portas analógicas são apenas de entrada e nelas podemos ter como entrada infinitos valores de tensão (delimitados na faixa de 0V a 5V). Como os conversores analógico-digitais (ADC - _analog-digital converter_, do Inglês) do Arduíno possuem 10 bits de precisão, a precisão das medições de tensão no Arduíno é de por volta de 0,005V ou 5mV. Mais precisamente 5V/1024.

|  |
| --- |
| **_~~Figura 1.10: Portas analógicas do Arduino, de 0 a 5~~_** |

Como os nomes de funções no Arduíno são bastante intuitivos, utilizamos a função analogRead para ler valores analógicos -- ao chamar a função passamos como argumento o número da porta que desejamos ler (de 0 - A0 a 5 - A5). Como exemplo vamos regular a luminosidade de nosso LED (utilizando PWM) através da quantidade de luz detectada por um resistor dependente de luz (ou LDR - _light dependent resistor_, do Inglês). Monte o circuito segundo a figura 1.11.

|  |
| --- |
| **_~~Figura 1.1: Circuito com LDR e LED~~_** |

Como os conversores analógicos-digital possuem 10 bits de precisão, a função analogRead nos devolve um valor entre 0 e 1023, onde 0 corresponde a uma leitura de 0V na porta analógica e 1023 corresponde a 5V (para valores intermediários, basta fazer uma regra de três simples de maneira análoga com o PWM). Vamos carregar em nosso Arduíno o seguinte código:

| **_~~#define LED 11~~_** |
| --- |
|  |

Os valores 0.25 e 255 da linha que definem a variável valor PWM devem ser calibrados conforme iluminação do ambiente, resistores utilizados e luminosidade desejada. Para o código acima, teremos o seguinte comportamento do valor que colocamos na porta PWM a partir dos valores lidos na porta analógica:

|  |
| --- |
| **_~~Figura 1.12: Gráfico da função PWM versus leitura analógica~~_** |
