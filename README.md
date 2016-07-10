# Introdução ao Arduino {#introdu-o-ao-arduino}

Curso BásicodeArduino

Basicão da Eletronica eConstruindo protótipos com Arduino

Autor:Carlos Delfino

10 de jul de 2016

Versão: 0.2.1

Conteúdo



Código Fonte

Código_Fonte 1: Código de controle de um Led pelo Botão 34

Código_Fonte 2: Fonte 1.3 - Outro Código de controle de um Led pelo Botão 35

Índice de Imagens

1.  Módulo I
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

Práticas Para Casa

1.  Aprenda a utilizar um potenciometro e o utilize para regular o brilho do LED, em vez do LDR;
2.  volte o LDR para o seu lugar anterior e utilize o potenciometro para configurar os valores 0.25 e 255;
3.  Leia o datasheet do circuito integrado LM35[^63] e monte um circuito parecido com o anterior, porém sensível a temperatura (e não a luz).
4.  Traga os esquemas desenhado no Fritizing de cada protótipo montado.
5.  Desenvolva uma Luminária de LEDs sensível a luz ambiente. (Campeonato melhor projeto)
6.  Módulo II
    1.  Fundamentos de Eletrônica

Alguns Componentes Eletrônicose suas fórmulas

Este conteúdo faz parte do curso “Basicão da Eletrônica”

*   *   1.  Tensão, Corrente e Potência

*   *   1.  Resistência e Capacitância

Veremos agora os dois conceitos mais aplicados na Eletrônica, sem eles nada é possível. Veremos também como usar o multímetro ferramenta fundamental e indispensável para todo hobbista e profissional ligado a eletrônica.

*   *   *   1.  Usando o Multímetro

O multímetro é um equipamento amplamente usado para quem dá manutenção ou desenvolve circuitos, seu nome se dá pelo fato de ser capaz de fazer múltiplas (multi) medidas (metro). As mais comuns são Resistência (Ohm), Tensão (V), Corrente (A) e suas subdivisões principalmente (mA), Capacitância e suas subdivisões (microFarad - uF, pico Farad - pF, nano Farad - nF), alguns também mede hFe de transistores, diodos e continuidade de um fio, há os que até consegue medir temperatura e impedância de bobinas.

Abaixo apresento alguns multímetros, sendo da esquerda para direita um multímetro analógico bem simples porém bem útil para medir tensões com variação constante e alguns tipos de circuitos como amplificadores de áudio, no meio o multímetro amarelo é uma excelente opção para quem está começando tem diversas medidas, dentre as padrões, tem também medição **hFE** dos transistores, continuidade e teste de bateria e pilha e diodos. Já o terceiro dentro os semi-profissionais é o melhor custo beneficio, tendo inclusive medição de temperatura, uma excelente precisão, iluminação do display e um pequeno frequencimentro.

|  |  |  |
| --- | --- | --- |
| **_~~sem marca~~_** | **_~~ET-2020 da MinipaouDT830B da UNI-T~~_** | **_~~ET-2082C da Minipa~~_** |

Resistores e Lei de Ohm

Resistores são componentes utilizados com a finalidade de transformar energia elétrica em energia térmica e/ou limitar a corrente elétrica em um circuito. como o próprio nome sugere, eles têm como função oferecer uma resistência à passagem da corrente elétrica -- medimos essa resistência através da unidade (ohm).

Por consequência, eles causam uma queda de tensão na região do circuito onde se encontram -- muitas vezes acabamos utilizando esse efeito para conseguirmos tensões intermediárias, caso as fontes de tensão do circuito não consigam fornecê-las. Sabendo-se a tensão e corrente em um resistor, podemos calcular sua resistência através da fórmula:

Por sua vez, a resistência pode ser calculada através das características do material resistivo:

Onde é a resistividade do material, L é seu comprimento e A sua área, ou seja, a resistência é proporcional ao comprimento e indiretamente proporcional à área.

Se, para um determinado circuito, V e I têm uma relação linear, ou seja, R é constante para inúmeros valores de _V_ e _I_, então chamamos o material (que possui resistência _R) de ôhmico._

Além da medida (ohm), temos múltiplos que medidos em Kilo e Mega, ou seja Kilo ohm que pode ser indicado com K, KR ou mesmo 1k0, por exemplo um resistor de 1500, será representado com o valor 1K5, isto é valido para o mega também, porém para os valores padrões em o símbolo pode ser subistituído pela letra R para facilitar a escrita. Veremos mais a frente uma tabela de valores padrões para industria.

Resistores em série

Se possuirmos resistores em série em determinado circuito, podemos calcular a resistência equivalente do mesmo somando se as resistência, através da fórmula:

|  |
| --- |
| **_~~Figuras~~ _**9**_~~: Resistores em Série~~_** |

Resistores em paralelo

Caso os resistores estejam em paralelo, a resistência equivalente será o inverso da soma dos inversos das resistências, como na fórmula a seguir:

|  |
| --- |
| **_~~Figuras~~ _**10**_~~: Resistores em paralelo~~_** |

Código de cores

Os resistores possuem um código de cores que nos permite identificar qual sua resistência. Para isso, mapeamos as cores das diversas faixas do resistor e utilizamos a seguinte fórmula para resistores padrões acima de 5%:

Onde _a_, _b_ e _c_ são as primeiras faixas e _t_ a última faixa (geralmente prata ou dourada), que representa a tolerância.

Para resistores de precisão como os de 1% ou menos usamos esta formula:

Onde _a_, _b_, _c_ e _d_ são as primeiras faixas e _t_ a última faixa (geralmente marron), que representa a tolerância.

Abaixo segue um infograma que demonstra a utilização de cores:

|  |
| --- |
| **_~~Figuras~~ _**11**_~~: Código de Cores para Resistores~~_** |

Veja a tabela de valores padrões comerciais:

[http](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[://](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[eletricamentefalando](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[blogspot](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[com](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[br](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[/2011/08/](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[valores](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[comerciais](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[de](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[-](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[resistores](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[.](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)[html](http://eletricamentefalando.blogspot.com.br/2011/08/valores-comerciais-de-resistores.html)

Divisor de Tensão

Como citado acima, resistores criam uma queda de tensão na região do circuito em que estão, Utilizando esse efeito, podemos criar o que chamamos de divisores de tensão[^64]: circuitos com resistores que, aplicada uma tensão, têm como saída uma fração (daí o nome divisores) dessa tensão de entrada.

É fundamental que compreenda bem o uso e funcionamento dos divisores de tensão, a forma mais comum que irá encontra-lo no contexto do Arduino é quando usar um potenciomentro.

|  |
| --- |
| **_~~Figuras~~ _**12**_~~: Circuito Divisor de Tensão~~_** |

A partir do circuito acima, temos que:

Esse recurso é bastante útil quando precisamos medir uma tensão maior do que nosso circuitos conseguem. Por exemplo: se quisermos medir uma tensão que varia de 9 a 12V no Arduíno precisaremos colocá la na faixa de 0 a 5V, já que as portas analógicas do Arduíno trabalham nessa faixa menor. Para isso, poderíamos utilizar um divisor de tensão cujos valores de resistência resultassem em . Dessa forma, os valores lidos em seriam de 3 a 4V.

Porém, atenção: caso precisemos conectar resistores ou outros circuitos resistivo no pino , o cálculo das tensões muda e passa a depender das novas resistências do circuito.

Observe que para medir tensões inferiores a 5V o Arduino tem o pino **_Aref_** que define o nível de tensão, use o somente para dar uma tensão de referência inferior a 5V permitindo assim que as leituras sejam proporcionais a esta nova tensão de referência.

*   *   1.  Capacitores e indutores

Apesar de não estudarmos a fundo esses dois elementos básicos de circuitos, eles podem ser importantes no desenvolvimento de futuros projetos. Basicamente, capacitores e indutores armazenam energia (pense como uma bateria em que você carrega e descarrega de tempos em tempos, porém com capacidade bem limitada) e são bastante utilizados em filtros de sinais, estabilizadores de tensão, circuitos ressonantes (como transmissores e receptores de rádio), dentre outros.

Capacitores

Os capacitores são componentes que armazenam energia em forma de campo elétrico. São formados por duas placas metálicas com um dielétrico (isolante) no meio. A unidade de medida é Farad (F), porém, 1 Farad é algo bem grande, comumente encontramos capacitores na casa dos

| mF | **_~~mili Farad~~_** |  | **_~~0.0001~~_** |
| --- | --- | --- | --- |
| **_~~µF~~_** | **_~~micro Farad~~_** |  | **_~~0.000001~~_** |
| nF | **_~~nano Fard~~_** |  | **_~~0.000000001~~_** |
| pF | **_~~pico Farad~~_** |  | **_~~0.000000000001~~_** |

Para uma tabela de conversão mais completa visite o site: [http](http://www.convertworld.com/pt/capacitancia/)[://](http://www.convertworld.com/pt/capacitancia/)[www](http://www.convertworld.com/pt/capacitancia/)[.](http://www.convertworld.com/pt/capacitancia/)[convertworld](http://www.convertworld.com/pt/capacitancia/)[.](http://www.convertworld.com/pt/capacitancia/)[com](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)[pt](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)[capacitancia](http://www.convertworld.com/pt/capacitancia/)[/](http://www.convertworld.com/pt/capacitancia/)

Abaixo estão as imagens de alguns tipos de capacitores e seu símbolo:

|  |
| --- |
| **_~~Figura 2.5: Capacitores de Poliester, Cerâmicos e Eletrôliticos~~_** |

|  |
| --- |
| **_~~Figura 2.6: Símbolo do Capacitor~~_** |

*   *   *   *   1.  Como ler os valores dos capacitores[^65]

Alguns capacitores apresentam uma codificação que é um tanto estranha, mesmo para os técnicos experientes, e muito difícil de compreender para o técnico novato. Observemos o exemplo abaixo:

|  | **_~~O valor do capacitor,"B", é de 3300 pF (picofarad = 10~~<sup><s>-12</s></sup> ~~F) ou 3,3 nF (nanofarad = 10~~<sup><s>-9</s></sup> ~~F) ou 0,0033 µF (microfarad = 10~~<sup><s>-6</s></sup> ~~F). No capacitor "A", devemos acrescentar mais 4 zeros após os dois primeiros algarismos. O valor do capacitor, que se lê 104, é de 100000 pF ou 100 nF ou 0,1µF.~~_** |
| --- | --- |

Capacitores usando letras em seus valores

|  | **_~~O desenho ao lado, mostra capacitores que tem os seus valores, impressos em nanofarad (nF) = 10~~<sup><s>-9</s></sup>~~F. Quando aparece no capacitor uma letra "n" minúscula, como um dos tipos apresentados ao lado por exemplo: 3n3, significa que este capacitor é de 3,3nF. No exemplo, o "n" minúsculo é colocado ao meio dos números, apenas para economizar uma vírgula e evitar erro de interpretação de seu valor.~~_** |
| --- | --- |
|  |

Multiplicando-se 3,3 por 10<sup>-9</sup> = ( 0,000.000.001 ), teremos 0,000.000.003.3 F. Para se transformar este valor em microfarad, devemos dividir por 10<sup>-6</sup> = ( 0,000.001 ), que será igual a 0,0033µF. Para voltarmos ao valor em nF, devemos pegar 0,000.000.003.3F e dividir por 10<sup>-9</sup> = ( 0,000.000.001 ), o resultado é 3,3nF ou 3n3F.

Para transformar em picofarad, pegamos 0,000.000.003.3F e dividimos por 10<sup>-12</sup>, resultando 3300pF. Alguns fabricantes fazem capacitores com formatos e valores impressos como os apresentados abaixo. O nosso exemplo, de 3300pF, é o primeiro da fila.

|  |
| --- |
|  |

Note nos capacitores seguintes, envolvidos com um círculo azul, o aparecimento de uma letra maiúscula ao lado dos números. Esta letra refere-se a tolerância do capacitor, ou seja, o quanto que o capacitor pode variar de seu valor em uma temperatura padrão de 25° C. A letra "J" significa que este capacitor pode variar até ±5% de seu valor, a letra "K" = ±10% ou "M" = ±20%. Segue na tabela abaixo, os códigos de tolerâncias de capacitância.

| **_~~Até 10pF~~_** | **_~~Código~~_** | **_~~Acima de 10pF~~_** |
| --- | --- | --- |
| **_~~±0,1pF~~_** | **_~~B~~_** | **__** |
| **_~~±0,25pF~~_** | **_~~C~~_** | **__** |
| **_~~±0,5pF~~_** | **_~~D~~_** | **__** |
| **_~~±1,0pF~~_** | **_~~F~~_** | **_~~±1%~~_** |
| **__** | **_~~G~~_** | **_~~±2%~~_** |
| **__** | **_~~H~~_** | **_~~±3%~~_** |
| **__** | **_~~J~~_** | **_~~±5%~~_** |
| **__** | **_~~K~~_** | **_~~±10%~~_** |
| **__** | **_~~M~~_** | **_~~±20%~~_** |
| **__** | **_~~S~~_** | **_~~-50% -20%~~_** |
| **__** | **_~~Z~~_** | **_~~+80% -20%~~_** |
| **__** | **_~~P~~_** | **_~~+100% -0%~~_** |

Agora, um pouco sobre coeficiente de temperatura "TC", que define a variação da capacitância dentro de uma determinada faixa de temperatura. O "TC" é normalmente expresso em % ou ppm/°C ( partes por milhão / °C ). É usado uma seqüência de letras ou letras e números para representar os coeficientes. Observe o desenho abaixo.

|  | **_~~Os capacitores ao lado são de coeficiente de temperatura linear e definido, com alta estabilidade de capacitância e perdas mínimas, sendo recomendados para aplicação em circuitos ressonantes, filtros, compensação de temperatura e acoplamento e filtragem em circuitos de RF.~~_** |
| --- | --- |
|  |

Na tabela abaixo estão mais alguns coeficientes de temperatura e as tolerâncias que são muito utilizadas por diversos fabricantes de capacitores.

| **_~~Código~~_** | **_~~Coeficiente de temperatura~~_** |
| --- | --- |
| **_~~NPO~~_** | **_~~-0± 30ppm/°C~~_** |
| **_~~N075~~_** | **_~~-75± 30ppm/°C~~_** |
| **_~~N150~~_** | **_~~-150± 30ppm/°C~~_** |
| **_~~N220~~_** | **_~~-220± 60ppm/°C~~_** |
| **_~~N330~~_** | **_~~-330± 60ppm/°C~~_** |
| **_~~N470~~_** | **_~~-470± 60ppm/°C~~_** |
| **_~~N750~~_** | **_~~-750± 120ppm/°C~~_** |
| **_~~N1500~~_** | **_~~-1500± 250ppm/°C~~_** |
| **_~~N2200~~_** | **_~~-2200± 500ppm/°C~~_** |
| **_~~N3300~~_** | **_~~-3300± 500ppm/°C~~_** |
| **_~~N4700~~_** | **_~~-4700± 1000ppm/°C~~_** |
| **_~~N5250~~_** | **_~~-5250± 1000ppm/°C~~_** |
| **_~~P100~~_** | **_~~+100± 30ppm/°C~~_** |

Outra forma de representar coeficientes de temperatura é mostrado abaixo. É usada em capacitores que se caracterizam pela alta capacitância por unidade de volume (dimensões reduzidas) devido a alta constante dielétrica sendo recomendados para aplicação em desacoplamentos, acoplamentos e supressão de interferências em baixas tensões.

|  | **_~~Os coeficientes são também representados exibindo seqüências de letras e números, como por exemplo: X7R, Y5F e Z5U. Para um capacitor Z5U, a faixa de operação é de +10°C que significa "Temperatura Mínima", seguido de +85°C que significa "Temperatura Máxima" e uma variação "Máxima de capacitância", dentro desses limites de temperatura, que não ultrapassa -56%, +22%.~~_** |
| --- | --- |

Veja as três tabelas abaixo para compreender este exemplo e entender outros coeficientes.

| **_~~Temperatura~~_** | **_~~Temperatura~~_** | **_~~Variação Máxima~~_** |
| --- | --- | --- |
| **Illegal nested table :** X-55°CY-30°CZ+10°C | **Illegal nested table :** 2+45°C4+65°C5+85°C6+105°C7+125°C | **Illegal nested table :** A ±1.0%B±1.5%C±2.2%D±3.3%E±4.7%F±7.5%P±10%R±15%S±22%T-33%, +22% U-56%, +22%V-82%, +22% |

Capacitores de Cerâmica Multicamada

|  |
| --- |

Capacitores de Poliéster Metalizado usando código de cores

A tabela abaixo, mostra como interpretar o código de cores dos capacitores abaixo. No capacitor "A", as 3 primeiras cores são, laranja, laranja e laranja, correspondem a 33000, equivalendo a 33 nF. A cor branca, logo adiante, é referente a ±10% de tolerância. E o vermelho, representa a tensão nominal, que é de 250 volts.

|  |
| --- |

| **__** | **_~~1ª Algarismo~~_** | **_~~2ª Algarismo~~_** | **_~~3ª N° de zeros~~_** | **_~~4ª Tolerância~~_** | **_~~5ª Tensão~~_** |
| --- | --- | --- | --- | --- | --- |
| **_~~PRETO~~_** | **_~~0~~_** | **_~~0~~_** | **_~~-~~_** | **_~~± 20%~~_** | **_~~-~~_** |
| **_~~MARROM~~_** | **_~~1~~_** | **_~~1~~_** | **_~~0~~_** | **_~~-~~_** | **_~~-~~_** |
| **_~~VERMELHO~~_** | **_~~2~~_** | **_~~2~~_** | **_~~00~~_** | **_~~-~~_** | **_~~250V~~_** |
| **_~~LARANJA~~_** | **_~~3~~_** | **_~~3~~_** | **_~~000~~_** | **_~~-~~_** | **_~~-~~_** |
| **_~~AMARELO~~_** | **_~~4~~_** | **_~~4~~_** | **_~~0000~~_** | **_~~-~~_** | **_~~400V~~_** |
| **_~~VERDE~~_** | **_~~5~~_** | **_~~5~~_** | **_~~00000~~_** | **_~~-~~_** | **_~~-~~_** |
| **_~~AZUL~~_** | **_~~6~~_** | **_~~6~~_** | **_~~-~~_** | **_~~-~~_** | **_~~630V~~_** |
| **_~~VIOLETA~~_** | **_~~7~~_** | **_~~7~~_** | **_~~-~~_** | **_~~-~~_** | **_~~-~~_** |
| **_~~CINZA~~_** | **_~~8~~_** | **_~~8~~_** | **_~~-~~_** | **_~~-~~_** | **_~~-~~_** |
| **_~~BRANCO~~_** | **_~~9~~_** | **_~~9~~_** | **_~~-~~_** | **_~~± 10%~~_** | **_~~-~~_** |

*   *   *   *   1.  Capacitores em Série

Quando vimos os resistores em série vimos que basta somar seus valores, porém, com os capacitores em Série, ocorre o inverso do que ocorre aos resistores, temos seu valor reduzido, portanto se temos dois capacitores de 1uF em serie teremos como resultado a medida de 0.5uF ou 500nF, ou seja sendo os capacitores do mesmo valor basta dividir pelo número de componentes em série, porém se você tiver valores diferentes aplique a seguinte fórmula:

*   *   *   *   1.  Capacitores em Paralelo

Observe que os capacitores em Paralelo somam seu valor, portanto dois capacitores sendo um de 1pF + outro de 500nF montados em serie, será equivalente a 1,5nF ou 1500pF

*   *   *   1.  Indutores

Os indutores são componentes que armazenam energia em forma de campo magnético. Geralmente são formados por bobinas (fio enrolado) com um condutor no meio. A unidade medida é o Henry (H).

|  |
| --- |
| Figuras 13: Indutores de diversos tipos, comuns no mercado |

|  |
| --- |
| **_~~Figuras~~ _**14**_~~: Símbolo para Indutores~~_** |

Não é comum usarmos mais de um Indutor em conjunto para obtermos novos valores, normalmente ajustamos as bobinas manualmente, portanto não iremos apresentar aqui nenhum tipo de informação para calcular valores de indutores em paralelo ou em serie.

Também não é nosso foco o desenvolvimento de indutores, portanto não iremos apresentar neste curso como fazer seus próprios indutores.

Diodos

Diodos são componentes que têm a capacidade de conduzir corrente elétrica em uma direção e bloqueá la em outra -- esse comportamento é chamado de retificação e pode ser utilizado para converter corrente alternada (CA ou AC -- _alternating current_, do Inglês) --, a energia que temos em nossa tomadas) em corrente contínua (CC ou DC -- _direct current_, do Inglês) --, a forma como as baterias os fornecem energia). Outros usos de diodo são proteção de circuitos (contra corrente reversa) e extração de modulação de sinais (por exemplo, para uso em circuitos de comunicação sem fio).

|  |
| --- |
| **_~~Figura 2.9: Foto de dois tipos de díodo comuns no mercado, A faixa indica corresponde ao terminal negativo (Catoto (K))~~_** |

|  |
| --- |
| **_~~Figura 2.10: Representação gráfica do diodo em um circuito~~_** |

O diodo conduzirá corrente elétrica caso a tensão em seu terminal positivo (+) seja maior que a tensão em seu terminal negativo (-), ou seja, funcionará como um curto-circuito. Caso contrário, ele funcionará como um circuito aberto (não conduzirá). É importante notar que para diodos reais existe uma queda de tensão em torno de 0,7V em sua junção PN e, com isso a tensão do lado positivo precisa ser maior que a tensão negativa + 0,7V para que ele conduza.

Além dos diodos comuns como falamos, existem diodos especiais que atendem funções exclusivas, vejamos alguns deles:

LEDs

Já falamos um pouco dos LEDs anteriormente, e aqui irei complementar mais um pouco. Há vários tipos de LED, desde baixo brilho a alto brilho, além dos de baixa, média, e alta potência, e tais LEDs tem substituído com muito sucesso lampadas nas mais diversas aplicações.

Hoje lampadas de carro já tem sido substituídas por LEDs de alto brilho e baixo consumo, temos as antigas lampadas dicróicas[^66] usadas em vitrines que também estão sendo substituídas por LEDs de alto brilho, letreiros, TVs e por ai vai.

Além das diferenças dos modelos como mostrado acima temos diferentes cores, que na verdade são o comprimento da onda de luz que o LED é capaz de imitir e assim temos LEDs coloridos, azuis, verdes, vermelhos, brancos, alaranjados/amarelos e algumas cores como o Ultra violeta e o Infra vermelho, que não são visíveis aos olhos humanos, porém podem ser usados em casos especiais para Tratamento em diversas áreas.

Abaixo segue um gráfico que apresenta as cores e sua colocação no Espectro Eletro Magnético:

|  |
| --- |
|  |

Conforme o material utilizado no LED para produzir um comprimento de onda diferente, temos uma tensão de junção diferente, portanto em muitos casos para se ter um brilho homogêneo entre as cores, é preciso ajustar o resistor para se manter a corrente na faixa dos 20mA.

Abaixo apresento uma tabela para facilitar a encontrar a tensão de calculo mais adequada para seu LED.

| **_~~Compr. de Onda (NM)~~_** | **_~~Cor~~_** | **_~~VF @ 20MA~~_** | **_~~MATERIAL~~_** |
| --- | --- | --- | --- |
| **_~~< 400~~_** | **_~~Ultravioleta~~_** | **_~~3.1 - 4.4~~_** | **_~~Aluminium nitride (AlN)~~_** |
| **_~~400 - 450~~_** | **_~~Violeta~~_** | **_~~2.8 - 4.0~~_** | **_~~Indium gallium nitride (InGaN)~~_** |
| **_~~450 - 500~~_** | **_~~Azul~~_** | **_~~2.5 - 3.7~~_** | **_~~Indium gallium nitride (InGaN)~~_** |
| **_~~500 - 570~~_** | **_~~Verde~~_** | **_~~1.9 - 4.0~~_** | **_~~Gallium phosphide (GaP)~~_** |
| **_~~570 - 590~~_** | **_~~Amarelo~~_** | **_~~2.1 - 2.2~~_** | **_~~Gallium arsenide phosphide (GaAsP)~~_** |
| **_~~590 - 610~~_** | **_~~Laranjado / ambar~~_** | **_~~2.0 - 2.1~~_** | **_~~Gallium arsenide phosphide (GaAsP)~~_** |
| **_~~610 - 760~~_** | **_~~Vermelho~~_** | **_~~1.6 - 2.0~~_** | **_~~Aluminium gallium arsenide (AlGaAs)~~_** |
| **_~~> 760~~_** | **_~~Infravermelho~~_** | **_~~< 1.9~~_** | **_~~Gallium arsenide (GaAs)~~_** |

Mais detalhes podem ser obtidos no link: [http](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[://](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[www](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[radio](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[electronics](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[com](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[info](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[data](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[semicond](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[leds](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[light](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[emitting](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[-](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[diodes](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[/](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[characteristics](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[.](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)[php](http://www.radio-electronics.com/info/data/semicond/leds-light-emitting-diodes/characteristics.php)

Diodos Zener

O diodo Zener é um componente muito interessante, e deve ser usado com muita cautela. E mais utilizado como um regulador de tensão e ao contrário do Diodo comum é deve ser usado no circuito com base na sua tenção reversa ou de ruptura, sendo aplicado em posição inversa ao diodo comum para surtir efeito.

É preciso ter cuidado no uso dos Diodos Zener, caso este se danifique ele perde seu efeito deixando passar a tensão total para o circuito, correndo o risco de queimar os demais componentes.

Vejamos na figura abaixo onde temos um circuito de analise:

|  | **_~~Vs = Tensão da Fonte~~_** |
| --- | --- |
|  |

|  | Vsmax é a tensão máxima que a fonte pode atingir. |
| --- | --- |
|  |

Transistores

Transistores são componentes semicondutores usados como amplificadores ou chaveadores. Sua entrada é uma corrente/tensão que altera a corrente/tensão de saída. Os transistores são a base de todos os circuitos integrados e placas modernos - alguns, como os microprocessadores, possuem milhões deles.

Para nossos estudos, iremos focar nos transistores de estrutura bipolar de junção (ou BJT, _Bipolar Junction Transistor,_ do Inglês) com polaridade **NPN** ou **PNP**, porém existem outros tipos, como os **FETs.**

|  |
| --- |
| **_~~Figura 2.11: Símbolos de transistores BJT em circuito elétrico~~_** |

Os transistores possuem três terminais: base, coletor e emissor. E suas principais equações caraterísticas são:

onde é uma constante (também referida como ) característica do transistor, é seu fator de amplificação.

A segunda equação nos evidencia o poder de amplificação de um transistor: dependendo da corrente que colocarmos na base (corrente ), ele permitirá maior ou menor corrente no coletor (corrente ).

Há muitas outras constantes e formulas relacionadas aos Transistores, que não serão estudas aqui, porém iremos

O encapsulamento dos Transistores

No mercado encontramos transistores NPN e PNP com vários encapsulamentos diferentes. alguns são o 2N3904 (NPN) e 2N3906 (PNP).

Abaixo uma imagem com alguns transistores em seus diferentes encapsulamentos:

|  |
| --- |
| **_~~Diversos tipos de transistores: TO-3, TO-218, TO-220, TO-126, TO-18, TO-92~~_**[^67] |

|  |
| --- |
| **_~~TO-3 em detalhes~~_** |

Utilização de transistores como relês

Relés são componentes úteis quando precisamos isolar eletronicamente um circuito de controle de um circuito de potência, Se quisermos, por exemplo, acender uma lâmpada incandescente (que utiliza corrente alternada) através do Arduino, podemos utilizar um relé: o Arduino controlará o relé, que então fará a conexão (ou não) da lâmpada com a tomada. Existem relés mecânicos e de estado sólido (SSR ou _Solid-state relay_, do Inglês), porém iremos utilizar um relé mecânico em nosso exemplo, por ser mais barato e fácil de se encontrar no mercado.

Nas imagens abaixo são apresentados, um tipo de rele em estado solido com 7 chaves construídas sobre sobre transistores darlingtons[^68],

|  |
| --- |
| **_~~UNL 2003 - Rele de estado solido~~_** |

Um relé comum de 5v,

|  |
| --- |
| **_~~Rele~~_** |

Abaixo está um MiniShield vendido na DealExtreame[^69], uma loja chinesa que vende diversos acessórios inclusive para Arduino.

|  |
| --- |
| **_~~Minishield Rele, Vendido na DealExtreme~~_**[^70] |

Como relés possuem correntes de ativação maiores que as portas digitais do Arduino conseguem suprir, precisamos amplificar a corrente que sai das portas digitais do Arduino para que ela seja capaz de acionar o relé, o MiniShield apresentado acima já tem no seu circuito os componentes que fazem a compensação de corrente necessária, porém, nos faremos um circuito com um transistor NPN.

Com um relé acionado por 5V, um transistor NPN (2N3904) e dois resistores (10Ω para o relé e 470Ω para a base do transistor), podemos utilizar o circuito a seguir, para controlar qualquer carga de corrente alternada -- basta ligar a carga às saídas do relé, que não estão indicadas no diagrama:

|  |
| --- |
| **_~~Figura 2.13: Circuito para ligar um relé (controlado por transistor) no Arduino~~_** |

Fica como exercício para o leitor verificar como seria o uso de um transistor PNP.

Ponte-H

Para estudarmos a Ponte H, precisamos conhecer melhor o funcionamento de um motor, veja abaixo a construção de um Motor de Corrente Continua.

|  |
| --- |
|  |  |  |
| **_~~Motor DC~~_** |

Em alguns projetos precisamos inverter a tensão de entrada de determinado circuito. Por exemplo: os motores de corrente contínua girando para um lado caso apliquemos tensão positiva em seu terminal esquerdo e negativa em seu terminal direito. Porém, para fazê los girar em sentido contrário, precisamos aplicar tensão negativa em seu terminal esquerdo e positiva em seu terminal direito.

Podemos implementar circuitos que fazem essa inversão de tensão a partir de 4 transistores funcionando como chave. Esse tipo de circuito se chama ponte-H por conta da disposição dos transistores com relação ao motor, como pode ser visto no diagrama a seguir:

|  |
| --- |
| **_~~Ponte H Conceitual~~_** |

Quando fechamos a chave S1 e S3, o terminal esquerdo do motor recebe tensão positiva e o direito recebe tensão negativa. Já quando fechamos as chaves s4 e S2, o terminal esquerdo recebe tensão negativa e o direito recebe tensão positiva. O que precisamos agora substituir as chaves por transistores capazes de fornecer a corrente adequada, e assim conseguiremos controlar os motores com o Arduino.

A seguir temos um circuito simples, porem, suficiente para testarmos uma ponte H. Neste circuito nossa fonte de energia será externa ao Arduino para que possamos alimentar da melhor forma o motor usado, a fonte externa deverá fornecer a tensão limite do Motor, ou seja, sendo o motor de 12V deverá ser uma fonte de 12V. Isto vale também para o limite de trenagem de corrente.

Observe este circuito é construído com quatro transistores Darlingtons TIP 120, que tem um HFE maior quanto maior for a corrente, como precisamos economizar ao máximo a corrente drenada do Arduino, e fornecer uma corrente média de 300mA para o motor, o valor ideal do resistor pode ser calculado conforme a formula a seguir:

Usando os seguintes parâmetros:

Para termos em torno de 1A no coletor teremos um HFE em torno de 1200;

Assim basta termos uma corrente na base de 1mA para obtermos mais 1,2A no Coletor;

Teremos como tensão o valor de 5V e a tensão de fuga do transitor o valor de 0,7V;

Neste caso não precisamos nos preocupar com o valor, visto que conseguimos um valor comercial[^71] para o resistor. Portanto os resistores R1 e R2 devem ter o valor de 4,3K?

|  |
| --- |
| **_~~Ponte H + Arduino~~_** |

Abaixo segue o esquema de montagem no Protoboard

|  |
| --- |
| **_~~Ponte H~~_** |

Já abaixo segue o desenho da placa que pode ser usada como um Shield para Arduino UNO.

|  |
| --- |
| **_~~Circuito feito no Fritzing para confecçionar a Placa~~_** |

Esta ponte é um modelo simples para se iniciar no conceito, existem diversos modelos de circuitos com maior proteção contra surtos de corrente e combinação incorreta da sinalização.

No site [http](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[://](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[www](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[.](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[mcmanis](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[.](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[com](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[chuck](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[robotics](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[tutorial](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[/](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[h](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[-](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge)[bridge](http://www.mcmanis.com/chuck/robotics/tutorial/h-bridge) é apresentado um esquema amplamente conhecido e utlizado na comunidade.

Outra opção é a compra de circuitos prontos para quem não quer montar seu proprio circuito, há opções de Shields como o mostrado abaixo e também circuitos integrados como o L293D

|  |
| --- |
| **_~~https://www.sparkfun.com/products/10018~~_** |

*   *   *   *   1.  PWM e Ponte-H para controle de velocidade

Como com PWM conseguimos controlar a quantidade de potência que será entregue a um circuito, caso utilizemos PWM como controle de uma ponte-H, podemos limitar a quantidade de potência entregue ao motor e, com isso, controlar sua velocidade.

*   1.  Capítulo

Eletrônica Digital

*   *   1.  Introdução

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

Capítulo

Introdução a Programação

*   *   1.  Introdução a Lógica de Programação

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

1.  Módulo

Comunicação ExternaSensoresMemória Permanente.

*   1.  Capítulo

Comunicações ExternasSe Comunicando Com Outro Dispositivos

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