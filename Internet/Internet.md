# O que é a internet?

A internet é a rede mais popular de computadores do mundo, ela começou como um projeto de pesquisa acadêmica em 1969 e se tornou uma rede comercial global por volta dos anos 90. Hoje é usada por mais de 5 BILHÕES de pessoas ao redor do mundo.
<br>
<br>
Por incrível que pareça, a internet é descentralizada, ou seja, ninguém é dono dela ou controla quem acessa através do mundo, ao invés disso, milhares de organizações operam suas próprias redes e fazem acordos de conexões entre si.

Resumindo: Internet é uma enorme rede de computadores onde todos comunicam entre si.

# Como a internet funciona?

Internet se tornou parte de nossas vidas nos dias de hoje e nós não sabemos muito bem como ela funciona, vamos começar com um exemplo simples:
Se você tem um computador e quer mandar um arquivo da pasta `A` para a pasta `B` ou quer trazer um arquivo da pasta `C` para a pasta `A` é simples de imaginar, porém, e se quiser enviar de um computador para o outro?
<img src="https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-1.png" alt="Computers connected"/>

Nesse caso precisamos mandar o arquivo do computador `A` para o computador `B`, simples, né?

Mas e se tivermos mais aparelhos?

<img src="https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-2.png" alt="Ten computers connected">

Vamos precisar de um fio pra cada conexão? Então se você comprar um computador, vai ter que comprar bilhões de fios pra conectar em todos os compudadores do mundo?

**Obviamente não!**

Vamos conectar num aparelho como um roteador e ele vai direcionar as mensagens que queremos pro computador certo: 

<img src="https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work/internet-schema-3.png" alt="Computers connected by a router">

Imagine esse roteador como um carteiro tentando entregar vários pacotes e, para entregar esses pacotes nos lugares certos, ele precisa dos endereços.

# Quais são os endereços dos computadores?

`Endereços de IP`, onde IP quer dizer `Internet Protocol`, tem o formato `nnn.nnn.nnn.nnn` onde cada `nnn` é um número de 000 a 255, ou seja, 256 possibilidades de números diferentes. Se multiplicarmos 256x256x256x256 temos 4294967296 de possibilidades, mais de 4 bilhões de endereços diferentes e cada aparelho conectado vai ter um endereço único.

# Como é a rede?

A internet tem uma representação mais parecida com essa:

<img src="../img/internetconnection.gif" alt="Diagrama mais detalhado" style="background-color:white"/>

Nossos aparelhos conectados a um modem que estão conectados à rede de telefone que conectam a um conjunto de modems, conectado a uma porta do ISP, que basicamente é um Internet Service Provider (Provedor de Serviços de internet), esse ISP não é o topo da cadeia, acima dele temos o NSP que é Network Service Provider, mas não vamos nos aprofundar nisso por aqui, se quiser se aprofundar, vou deixar os links nas referências.

# Como um dado é enviado?

Se queremos enviar uma mensagem, como ela é enviada?
Vamos supor que você tá enviando um vídeo de 10 Gigabytes pra algum amigo e quer mandar uma mensagem pra sua mãe, imagina se fosse igual fila e sua mensagem só fosse enviada depois que o vídeo todo tivesse sido enviado, ainda mais nas internets de baixa velocidade de antigamente, seria inviável. Por conta disso, as coisas que enviamos na internet são divididas em pacotes, agora vamos supor que esse vídeo foi dividido em milhões de pacotes, como saber se todos chegaram no endereço certo, se nenhum tá faltando e se tá na ordem certa? Pra isso criamos um protocolo.

# Transmission Control Protocol (Protocolo de controle de transmissão)

O TCP funciona como se fosse um estoquista, ele verifica se todos os pacotes de dados chegaram e coloca eles na ordem certa. E se não chegarem todos? O TCP vai fazer a requisição pro endereço inicial pelos pacotes que faltaram até todos os pacotes estarem ali. Resumindo, para enviar os dados, precisamos do endereço e do protocolo.
Mas e se quisermos enviar "fotos de corujas fofas" pro google, vamos saber que o endereço dele é `142.250.190.78`? E nos outros sites? Vamos ficar decorando os endereços de IP deles? Bem improvável! Então é por isso que temos o `DNS`.

# Domain Name Service (Serviço de nome de domínio)

O DNS funciona como uma lista telefonica da internet, você procura o nome da pessoa, no caso o nome do site como por exemplo `google.com` e acha lá o número dela, que no caso é o endereço de IP `142.250.190.78`.

Falando desses links, o que são os famosos `www`, `http`, `https`, `.com`, etc?

# HTTP & HTTPS

`HTTP` é a sigla para Hypertext Transfer Protocol, que significa Protocolo de Transferência de Hipertexto que é o protocolo usado pelos navegadores e servidores para comunicarem entre si, é um conjunto de regras que define como a informação é trocada entre seu navegador e o server do website que você está visitando.
A diferença dele pro `HTTPS` é o S de Secure ou Seguro no português, que é o HTTP com uma camada de segurança a mais, nesse caso o seu navegador e o server usam um processo chamado SSL/TLS(Secure Sockets Layer/ Transport Security Layer) para encriptar a informação enviada e a recebida para prevenir ela de ser interceptada e usada por pessoas com intenções maliciosas.

# .com

O .com é um TLD (Top-Level Domain), que traduziríamos como Domínio de alto nível e faz parte do DNS que falamos antes e é abreviação de commercial, originalmente era pra ser usado por organizações comerciais, mas com o passar do tempo todo tipo de website usa, temos outros TLD famosos como .org para organizações não lucrativas, .edu para instituições educacionais e .gov para agencias do governo. Além disso, também existem os de países .br .uk .cn e por incrível que pareça, algumas famosas que vemos hoje em dia são de países e hoje em dia são utilizadas pra todo tipo de site, como a .io e a .tv

# www

www é a sigla para `world wide web` que basicamente significa `rede mundial de computadores`é um sistema de documentos e recursos interconectados, identificados por URLs (Uniform Resource Locators) que significia Localizadores Uniformes de recursos, que são acessados via internet usando o navegador. Hoje em dia o www faz parte da vida de todos nós e nos permite acessar uma vasta quantidade de informações e conectarmos com as pessoas ao redor do mundo, é o que as pessoas costumam se fererir quando falam de internet, é bem parecido, mas não se engane, a www é apenas uma parte da internet.


# Referências

<a href="https://developer.mozilla.org/en-US/docs/Learn/Common_questions/Web_mechanics/How_does_the_Internet_work"> How does the internet work? [MDN]</a>

<a href="http://web.stanford.edu/class/msande91si/www-spr04/readings/week1/InternetWhitepaper.htm"> How does the internet work? [Stanford]</a>


# Canal

<a href="https://www.youtube.com/@hugo_nicolau/sub_confirmation=1">Hugo Nicolau</a>

# Correções

> Se virem algo errado aqui ou no vídeo do canal, podem me contactar para me corrigir 
>>Gmail: nicolau.hugogiles@gmail.com