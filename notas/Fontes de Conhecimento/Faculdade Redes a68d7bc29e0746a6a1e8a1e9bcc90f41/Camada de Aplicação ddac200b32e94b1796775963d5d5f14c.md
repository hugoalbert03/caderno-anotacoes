# Camada de Aplicação

**Sempre que um programador cria dois aplicativos que se comunicam, ele especifica
detalhes como:**

- A sintaxe e a semântica da mensagem que pode ser trocada.
- O iniciador da interação, que é ou o cliente ou o servidor.
- As ações a serem realizadas em caso de erro.
- Como os dois lados sabem quando a comunicação termina.

tipos genéricos de protocolos da camada de aplicação que dependem do uso pretendido:

- **Serviço privado**. Um programador ou uma empresa cria um par de aplicativos
que se comunicam por meio da Internet com a intenção de que nenhum outro crie
software cliente ou servidor para esse serviço. Não existe necessidade de publicar
e distribuir uma especificação formal para definir a interação, porque nenhuma
aplicação externa precisaria entender os detalhes de protocolo. De fato, se a interação entre os dois aplicativos é suficientemente simples, pode até não haver um
documento de protocolo interno.
- **Serviço padronizado**. Um serviço da Internet é definido com a expectativa de
que muitos programadores criem o software servidor que oferece o serviço ou o
software cliente para acessar o serviço. Em tais casos, o protocolo da camada de
aplicação deve ser documentado independentemente de qualquer implementação. Além disso, a especificação deve ser precisa, e não ambígua, para que aplicativos cliente-servidor possam ser construídos de tal modo que se interoperem corretamente.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled.png)

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%201.png)

**A HyperText Markup Language (HTML) é um padrão de representação que especifica a
sintaxe para a página Web. O HTML tem as seguintes características gerais:**

- Usa uma representação textual.
- Descreve páginas Web que contém multimídia.
- Segue o paradigma da linguagem declarativa em vez do da imperativa.
- Fornece as especificações de marcação (markup specifications) em vez de formatação.
- Permite que um hiperlink seja aninhado em um objeto qualquer.
- Permite ao documento incluir metadados.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%202.png)

O protocolo de transferência de hipertexto (HTTP, HyperText Transfer Protocol), é o
protocolo de transferência principal que um navegador usa para interagir com um servidor Web. Em termos de modelo cliente-servidor, o navegador é um cliente que extrai o
nome do servidor de uma URL e contata-o. A maioria das URLs contém uma referência
explícita ao protocolo HTTP; caso ela seja omitida, o HTTP é assumido.

**O HTTP pode ser caraterizado da seguinte maneira**:

- Usa mensagem de controle textual
- Transfere arquivos de dados binários
- Pode baixar ou carregar dados
- Incorpora caching

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%203.png)

A forma mais comum de interação começa quando um navegador requere uma
página de um servidor. O navegador envia uma requisição GET na conexão e o servidor
responde enviando um cabeçalho, uma linha em branco e o documento requisitado. No
HTTP, uma requisição e um cabeçalho usados em resposta são informações textuais. Por
exemplo, uma requisição GET tem a seguinte forma:

<aside>
💡 GET /item version CRLF

</aside>

onde item fornece a URL para o item que está sendo requisitado, version especifica uma
versão do protocolo (usualmente HTTP/1.0 ou HTTP/1.1) e CRLF denota dois caracteres ASCII, carriage return e linefeed, que são usados para indicar o fim de uma linha
de texto.

A informação de versão é importante no HTTP porque ela permite que o protocolo
mude e permaneça compatível com a versão anterior. Por exemplo, quando um navegador usa a versão 1.0 do protocolo e interage com um servidor que usa uma versão mais
atual, o servidor retorna para a versão anterior do protocolo e formula uma resposta de
acordo. Para resumir:

> Um navegador, quando usa HTTP, envia a informação de versão que permite ao
servidor escolher a versão mais atualizada do protocolo, que o navegador e o
servidor possam entender.
> 

A primeira linha de um cabeçalho-resposta contém um código status que diz ao
navegador se tem o servidor manipulou a requisição. Se a requisição foi formulada incorretamente ou se o item requisitado não estava disponível, o código do status aponta
o problema. Por exemplo, um servidor retorna o conhecido status código 404 se o item
requisitado não pôde ser encontrado. Quando a requisição é atendida, um servidor retorna
o status código 200; linhas adicionais do cabeçalho fonecem mais informações sobre o
item, como seu comprimento, quando foi modificado pela última vez e o tipo de conteúdo.
A Figura 4.6 mostra o formato geral de linhas em um cabeçalho básico de resposta.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%204.png)

O campo status_code é um valor numérico representado como uma cadeia de caracteres de dígitos decimais que informa um status e um status_string, que é uma explicação correspondente para um humano ler. A Figura 4.7 lista exemplos de strings e
códigos de status comumente usados. O campo server_identification contém uma cadeia
de caracteres que fornece uma descrição do servidor legível pelo ser humano, possivelmente incluindo o nome do domínio do servidor. O campo datasize no cabeçalho
Content-Length especifica o tamanho do item de dados que segue, medido em bytes.
O campo document_type contém uma cadeia de caracteres que informa ao navegador
sobre o conteúdo do documento. A cadeia de caracteres contém dois itens separados por
uma barra: o tipo do documento e sua representação. Por exemplo, quando um servidor
retorna um documento HTML, o document_type é text/html e, quando ele retorna um
arquivo jpeg, o tipo é image/jpeg.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%205.png)

A Figura 4.8 mostra um exemplo de saída de um servidor Web Apache. O item
requisitado é um arquivo de texto de 16 caracteres (isto é, o texto This is a test. mais o
caractere NEWLINE). Embora a requisição GET especifique a versão HTTP 1.0, o servidor executa a versão 1.1. O servidor retorna nove linhas de cabeçalho, uma linha em
branco e o conteúdo do arquivo.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%206.png)

## Caching nos navegadores

O caching fornece uma otimização importante para o acesso Web, porque usuários tendem a visitar o mesmo site Web repetidamente. Grande parte do conteúdo de um dado site consiste em grandes imagens que usam padrões tais como Graphics Image Format
(GIF) ou Joint Photographic Experts Group (JPEG). Tais imagens geralmente contêm
fundos ou banners que não mudam com frequência. A ideia-chave é:

> Um navegador pode reduzir o tempo de download significativamente salvando
uma cópia de cada imagem em um cache no disco do usuário e usando essa cópia.
> 

Uma questão pertinente: o que acontece se o documento no servidor Web muda
depois que um navegador armazena uma cópia da imagem no seu cache? Isto é, como
um navegador pode saber se sua cópia no cache está desatualizada? A Figura 4.8
contém uma pista: o cabeçalho Last-Modified. Sempre que um navegador obtém um
documento a partir de um servidor Web, o cabeçalho especifica a última vez que o
documento foi alterado. Um navegador salva a informação da data Last-Modified da
cópia armazenada no cache. Antes de usar um documento do cache local, o navegador faz uma requisição do HEAD para o servidor e compara a data Last-Modified do
servidor com a data Last-Modified da cópia do cache. Se a versão do cache está desatualizada, ele carrega a nova versão. 

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%207.png)

O algoritmo omite vários detalhes menores. Por exemplo, o HTTP permite a um
site Web incluir um cabeçalho sem cache que especifica que um dado item não deveria
ser armazenado no cache. Além disso, os navegadores não armazenam no cache pequenos itens, porque mantê-los pode aumentar o tempo de pesquisa no cache e o tempo de
carga do item pequeno com uma requisição GET é aproximadamente o mesmo necessário para fazer uma requisição HEAD

## Arquitetura do navegador

Um navegador é complexo porque fornece uma grande quantidade de serviços gerais e
suporta uma interface gráfica complexa capaz de atender aos referidos serviços. É claro que
um navegador deve entender o HTTP, mas, também, fornecer suporte para outros protocolos. Em particular, como uma URL pode especificar um determinado protocolo, um navegador deve conter o código-cliente capaz de tratar cada um dos protocolos utilizados. Para
cada serviço, o navegador deve saber como interagir com um servidor e como interpretar as
respostas. Por exemplo, um navegador deve saber como acessar o serviço FTP discutido na
próxima seção. A Figura 4.9 ilustra os componentes que compõem um navegador.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%208.png)

## File Transfer Protocol (FTP)

Um arquivo é uma abstração fundamental de armazenamento. Como um arquivo pode
conter um objeto arbitrário (isto é, um documento, um programa de computador, uma
imagem gráfica ou um videoclipe), a facilidade de enviá-lo de um computador para
outro é um mecanismo muito poderoso para a troca de dados. O termo transferência de
arquivo é usado para tal serviço.
A transferência de arquivo através da Internet é complicada porque os computadores são heterogêneos, o que significa que cada sistema de computador tem que possuir
as representações dos arquivos, a informação de tipo, a nomeação e os mecanismos de
acesso ao arquivo.
Em alguns sistemas de computador, a extensão .jpg é usada para uma imagem
JPEG e, em outros, é utilizada a extensão .jpeg. Em alguns sistemas, cada linha em um
arquivo de texto é encerrada por um único caractere LINEFEED, enquanto outros sistemas exigem o caractere CARRIAGE RETURN seguido do LINEFEED. Alguns sistemas
utilizam uma barra (/) como um separador em nomes de arquivos, e outros usam uma
Capítulo 4 Aplicações tradicionais da Internet 55
barra invertida (\). Além disso, um sistema operacional pode definir um conjunto de contas de usuário que especificam o direito de acesso a arquivos determinados. No entanto,
a informação de conta é diferente entre os computadores, de modo que o usuário X em
um computador não é o mesmo que o usuário X no outro.
O serviço padrão de transferência de arquivos na Internet usa o File Transfer Protocol (FTP). O FTP pode ser caracterizado a partir destes aspectos:

- Conteúdos arbitrários de arquivo. O FTP pode transferir qualquer tipo de dados,
incluindo documentos, imagens, músicas ou vídeos armazenados.
- Transferência bidirecional. O FTP pode ser usado para baixar (download) arquivos (transferir do servidor para o cliente) ou carregar (upload) arquivos (transferir
do cliente para o servidor).
- Suporte para autenticação e propriedade. O FTP permite que cada arquivo tenha
propriedade e restrições de acesso.
- Habilidade para navegar em pastas. O FTP permite que um cliente navegue nos
conteúdos de um diretório (ou seja, uma pasta).
- Mensagens de controle textual. Como muitos outros serviços aplicativos da Internet, as mensagens de controle trocadas entre um cliente e um servidor FTP são
enviadas como texto ASCII.
- Acomodação de heterogeneidade. O FTP esconde os detalhes dos sistemas operacionais dos computadores individuais e pode transferir uma cópia de um arquivo
entre dois computadores quaisquer.

Como poucos usuários lançam uma aplicação FTP, o protocolo é geralmente invisível. No entanto, ele costuma ser chamado automaticamente pelo navegador quando um
usuário solicita uma transferência de arquivo.

## O paradigma de comunicação FTP

Um dos aspectos mais interessantes do FTP decorre da maneira com que um cliente
interage com o servidor. No geral, a abordagem parece simples: um cliente estabelece
uma conexão com um servidor de FTP e envia uma série de pedidos para que o servidor
responda. Ao contrário do HTTP, um servidor FTP não envia respostas pela mesma
conexão em que o cliente envia solicitações. Em vez disso, a conexão que o cliente cria,
chamada de conexão de controle, é reservada para os comandos. Cada vez que o servidor precisa baixar ou carregar um arquivo, ele (não o cliente) abre uma nova conexão.
Para distingui-las da conexão de controle, as conexões usadas para transferir arquivos
são chamadas de conexões de dados.

Surpreendentemente, o FTP inverte o relacionamento cliente-servidor para conexões de dados. Isto é, quando abre uma conexão de dados, o cliente age como se
fosse um servidor (ou seja, espera pela conexão de dados) e o servidor age como se
fosse um cliente (ou seja, inicia a conexão de dados). Depois de ter sido utilizada para
uma transferência, a conexão de dados é fechada. Se o cliente envia outro pedido,
o servidor abre uma nova conexão de dados. A Figura 4.10 ilustra a interação, mas
omite vários detalhes importantes. Por exemplo, depois de criar a conexão de controle, um cliente deve se conectar ao servidor por meio do envio de um login e de uma
senha; um login anônimo com senha de convidado é usado para obter os arquivos que são públicos. Um servidor envia um status numérico através da conexão de controle
como uma resposta a cada pedido, inclusive o do login; a resposta permite que o
cliente saiba se o pedido era válido.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%209.png)

Outro detalhe interessante diz respeito aos números das portas de protocolo usadas. Nesse sentido, surge a pergunta: o que o número de porta de protocolo deve especificar para que um servidor se conecte ao cliente? O FTP permite que o cliente decida:
antes de fazer um pedido para o servidor, um cliente aloca uma porta de protocolo em
seu sistema operacional local e envia o número da porta para o servidor. Ou seja, o
cliente amarra a porta para aguardar uma conexão e depois transmite o número da porta
através da conexão de controle como uma sequência de dígitos decimais. O servidor lê o
número e segue os passos que o Algoritmo 4.2 especifica.
A transmissão de informações de porta entre um par de aplicações pode parecer
inócua, mas não é, e a técnica não funciona bem em todas as situações. Em particular,

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2010.png)

a transmissão de um número de porta de protocolo irá falhar se um dos dois terminais
estiver por trás de um dispositivo Network Address Translation (NAT), como um roteador sem fio usado em uma residência ou em um pequeno escritório. O Capítulo 23
explica que o FTP é uma exceção – para suportar um FTP, um dispositivo NAT reconhece uma conexão de controle FTP, inspeciona o conteúdo da conexão e reescreve os
valores em um comando PORT.

## Mensagem eletrônica

Embora os serviços de mensagens instantâneas tenham se tornado populares, o e-mail
continua a ser um dos aplicativos mais usados na Internet. Como esse serviço foi concebido antes dos computadores pessoais e dos PDAs estarem disponíveis, ele foi projetado
para permitir que um usuário em um computador envie uma mensagem diretamente
para outro usuário em outro computador. A Figura 4.11 ilustra a arquitetura original e o
Algoritmo 4.3 lista os passos realizados.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2011.png)

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2012.png)

Como o algoritmo 4.3 indica, mesmo o software original de e-mail foi dividido
conceitualmente em duas partes separadas:

- Uma aplicação de interface de mensagem
- Uma aplicação de transferência de mensagem

Um usuário chama um aplicativo de mensagem diretamente. A interface desse aplicativo fornece mecanismos que permitem que um usuário componha e edite
mensagens de saída, bem como leia e processe mensagens recebidas. Um aplicativo
de mensagens não age como um cliente ou um servidor e não transfere mensagens
para outros usuários. Em vez disso, ele lê mensagens da caixa postal do usuário (ou
seja, um arquivo no computador do usuário) e passa mensagens adiante para um aplicativo de transferência de mensagens. O aplicativo de transferência de mensagens
age como um cliente para enviar cada mensagem de e-mail para o seu destino. Além
disso, ele também atua como um servidor para aceitar as mensagens recebidas e armazenar cada uma delas na caixa de correio do usuário apropriado.

As normas de protocolo usadas para mensagens na Internet podem ser divididas
em três tipos amplos, como a Figura 4.12 descreve

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2013.png)

## O Simple Mail Transfer Protocol (SMTP)

O Simple Mail Transfer Protocol (SMTP) é o protocolo padrão que o programa de transferência de mensagens usa para transferir uma mensagem para um servidor por meio da
Internet. O SMTP pode ser caracterizado assim:

- Segue o paradigma stream
- Usa mensagem de controle textual
- Transfere somente mensagem de texto
- Permite a um remetente especificar os nomes dos destinatários e checar cada um
deles
- Envia uma cópia de uma dada mensagem

O aspecto mais inesperado do SMTP decorre da sua restrição às mensagens
textuais. Uma seção posterior explica o padrão MIME dos anexos permitidos na mensagem, tais como imagens gráficas ou arquivos binários, mas o mecanismo do SMTP é
restrito ao texto.

O segundo aspecto do SMTP é sua capacidade de enviar uma única mensagem
para vários destinatários em um determinado computador. O protocolo permite que um
cliente liste os usuários um a um e em seguida envie uma única cópia de uma mensagem
para todos os usuários da lista. Ou seja, um cliente envia “Eu tenho uma mensagem de
correio para o usuário A” e o servidor responde “OK” ou “O usuário não existe aqui”.

Na verdade, cada mensagem do servidor SMTP começa com um código numérico; assim, respostas são escritas da forma “250 OK” ou “550 O usuário não existe aqui”. A Figura 4.13 mostra um exemplo de uma sessão SMTP que ocorre quando uma mensagem
de correio é transferida do usuário John_Q_Smith no computador [example.edu](http://example.edu/) para dois
usuários no computador [somewhere.com](http://somewhere.com/).

Na figura, cada linha é marcada como Cliente: ou Servidor: para indicar se é o
servidor ou o cliente que a envia; o protocolo não inclui os rótulos em itálico. O comando HELO permite ao cliente se autoautenticar por meio do envio de seu nome de
domínio. Por fim, a notação <CR> <LF> denota um CARRIAGE RETURN seguido
de um LINEFEED (ou seja, um fim-de-linha). Assim, o corpo de uma mensagem de
e-mail é finalizado por uma linha que consiste em um período com nenhum outro texto
ou espacejamento.

O termo simple no nome indica que o SMTP é simplificado. Como o antecessor
do SMTP era muito complexo, os projetistas eliminaram os recursos desnecessários e
concentraram-se no básico.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2014.png)

## ISPs, servidores de mensagens e acesso às mensagens

À medida que a Internet se expandiu para incluir novos consumidores, um novo paradigma surgiu por meio do e-mail. Como a maioria dos usuários não deixa o seu computador
funcionando de forma contínua e não sabe como configurar e gerenciar um servidor de
e-mail, os ISPs começaram a oferecer serviços de e-mail. Em essência, um ISP executa
um servidor de e-mail e fornece uma caixa de correio para cada assinante. Em vez de
fornecer um software de e-mail tradicional, cada ISP oferece um software de interface
que permite ao usuário acessar sua caixa de correio. A Figura 4.14 ilustra o arranjo.

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2015.png)

O acesso ao e-mail ocorre de uma das duas formas:

- Um aplicativo de interface de e-mail de propósito especial
- Um navegador Web que acessa uma página Web de e-mail

Aplicativos de interface de propósito especial são usados tipicamente em dispositivos móveis, como tablets ou smartphones. Devido ao fato de eles conhecerem o tamanho da tela e a capacidade do dispositivo, esses aplicativos podem mostrar o e-mail no
formato apropriado para o referido dispositivo. Outra vantagem de usar um aplicativo
de e-mail especial está relacionada com a habilidade de baixar toda a caixa de correio
no dispositivo local. Baixá-la toda é particularmente importante se o usuário móvel pretende ficar desconectado da rede, pois isso permite a ele processar as mensagens
mesmo que esteja sem conexão com a Internet (por exemplo, durante um vôo). Uma
vez que a conectividade com a Internet seja estabelecida, o aplicativo se encarrega da
comunicação com o servidor no ISP do usuário para carregar as mensagens redigidas e
para baixar novas mensagens que podem ter chegado na caixa de correio dele.
Usar um navegador Web como uma interface de e-mail é natural: um ISP fornece
uma página Web especial que mostra as mensagens da caixa de correio do usuário.
Dessa forma, o usuário lança um navegador Web padrão e acessa o servidor de e-mail
no ISP. A página Web inicial chama um mecanismo de autenticação que pergunta ao
usuário login e senha; o servidor Web usa o login do usuário para selecionar sua caixa de correio. O servidor Web recupera as mensagens da caixa de correio, gera uma
página HTML que lista as mensagens e retorna a página para o navegador do usuário.
A principal vantagem de usar uma página Web para e-mail é a facilidade de ler mensagens de qualquer computador ou dispositivo – o usuário não necessita de um dispositivo particular nem precisa rodar um aplicativo de interface de e-mail especial. Assim,
um usuário em viagem pode ter acesso às suas mensagens por meio do computador na
recepção de um hotel.

## Protocolos de acesso ao e-mail (POP, IMAP)

Diferentes protocolos têm sido criados para fornecer acesso ao e-mail. Um protocolo
de acesso é distinto de um protocolo de transferência porque um acesso envolve somente um usuário interagindo com sua caixa de correio, enquanto uma transferência
envolve o envio de mensagens de um usuário qualquer em um computador para uma
caixa de correio qualquer em outro computador. Protocolos de acesso têm as seguintes
características:

- Fornecem acesso à caixa de correio do usuário
- Permitem ao usuário ver cabeçalhos, baixar, excluir ou enviar mensagens individuais
- Rodam o cliente no computador ou no dispositivo do usuário
- Rodam o servidor no computador onde a caixa de correio está armazenada

A possibilidade de ver a lista de mensagens sem baixar os conteúdos delas é
especialmente útil nos casos em que a conexão entre o usuário e o servidor de e-mail
é lenta. Por exemplo, um usuário navegando através de um telefone celular pode
olhar os cabeçalhos e deletar os spams sem esperar para baixar os conteúdos dessas
mensagens.
Diversos mecanismos têm sido propostos para acesso ao e-mail. Alguns ISPs fornecem software de acesso livre aos seus assinantes. Além disso, dois padrões de protocolos de acesso ao e-mail foram criados; a Figura 4.15 lista esses padrões:

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2016.png)

Embora ofereçam os mesmos serviços básicos, os dois protocolos diferem em
muitos detalhes. Cada um fornece seu próprio mecanismo de autenticação que um usuário segue para ele mesmo. A autenticação é necessária para garantir que um usuário não
acesse a caixa de correio de outro usuário.

## Padrões de representação de e-mail (RFC2822, MIME)

Duas representações de e-mail foram padronizadas:

- RFC2822 Mail Message Format
- Multi-purpose Internet Mail Extensions (MIME)

RFC2822 Mail Message Format. O formato padrão de mensagem de e-mail retira seu nome do documento padrão do IETF (Internet Engineering Task Force), Request
For Comments 2822. O formato é direto: uma mensagem de e-mail é representada como
um arquivo de texto e consiste em uma seção cabeçalho, uma linha em branco e um
body. As linhas do cabeçalho têm a forma:
Keyword: information
onde o conjunto de keywords é definido para incluir From:, To:, Subject:, Cc: e assim
por diante. Além disso, linhas do cabeçalho que iniciam com a letra maiúscula X podem
ser adicionadas sem afetar o processamento de e-mail. Assim, um e-mail pode incluir
uma linha randômica no cabeçalho, tal como:
X-Worst-TV-Shows: any reality show
Multi-purpose Internet Mail Extensions (MIME). Lembre-se de que o SMTP
pode transferir somente mensagens de texto. O padrão MIME estende a funcionalidade
de e-mail para permitir a transferência de mensagens de dados não textuais. O MIME especifica como um arquivo binário pode ser codificado dentro de caracteres imprimíveis,
incluídos na mensagem, e decodificado pelo destinatário.
Embora isso tenha introduzido o padrão de codificação Base64 que tem se tornado
popular, o MIME não restringe a codificação para uma forma específica. Em vez disso,
permite ao remetente e ao destinatário escolher uma codificação que seja mais conveniente. Para especificar o uso de uma codificação, o remetente inclui linhas adicionais
no cabeçalho da mensagem. Além disso, o MIME permite que um remetente divida a
mensagem em várias partes e especifique uma codificação para cada parte independentemente. Assim, com o MIME, um usuário pode enviar uma mensagem textual e anexar
imagens gráficas, uma planilha e um clipe de áudio, cada um com sua própria codificação. O sistema de e-mail destinatário pode decidir como processar os anexos (ou seja, se
salva uma cópia no disco ou mostra uma cópia).
De fato, o MIME adiciona duas linhas no cabeçalho: uma para declarar que o
MIME foi utilizado para criar a mensagem e outra para especificar como a informação
MIME está incluída no body. Por exemplo, as linhas do cabeçalho:

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2017.png)

especificam que a mensagem foi composta usando a versão 1.0 do MIME e que a linha contendo Mime_separator aparecerá no corpo antes de cada parte da mensagem.
Capítulo 4 Aplicações tradicionais da Internet 63
Quando o MIME é usado para enviar uma mensagem de texto padrão, a segunda linha
muda para:

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2018.png)

O MIME é compatível com os sistemas de e-mail que não entendem o padrão
MIME ou a codificação. É claro que tais sistemas não têm nenhuma maneira de extrair
anexos não textuais – eles tratam o corpo como um único bloco de texto. Para resumir:

> O padrão MIME insere linhas extras de cabeçalho para permitir que anexos
não textuais possam ser enviados dentro de uma mensagem de e-mail. Um anexo é codificado como letras imprimíveis e uma linha separadora aparece antes
de cada anexo.
> 

## Domain Name System (DNS)

O Domain Name System (DNS) fornece um serviço que mapeia nomes simbólicos
legíveis por seres humanos para endereços de computadores. Navegadores, softwares
de e-mail e a maioria dos outros aplicativos da Internet usam o DNS. O sistema fornece um interessante exemplo de interação cliente-servidor, pois o mapeamento não é
executado por um simples servidor. Em vez disso, a informação de nomeação é distribuída, por meio da Internet, entre vários servidores localizados em sites. Sempre que
um aplicativo precisa traduzir um nome, ele torna-se cliente do sistema de nomeação.
O cliente envia uma mensagem de requisição para um servidor de nome, que encontra
o endereço correspondente e envia uma mensagem de resposta. Se ele não consegue
responder à requisição, um servidor de nome torna-se temporariamente cliente de um
outro servidor de nome, até que seja encontrado um servidor que pode responder à
requisição.
Sintaticamente, cada nome consiste em uma sequência de segmentos alfanuméricos separados por pontos. Por exemplo, um computador na Purdue University tem o
nome de domínio:

[mymail.purdue.edu](http://mymail.purdue.edu/)

e um computador na Google tem o nome de domínio:

[gmail.google.com](http://gmail.google.com/)

Os nomes de domínio são hierárquicos, com a parte mais significativa do nome
na direita. O segmento mais à esquerda do nome (mymail e gmail nos exemplos) é o
nome do computador individual. Outros segmentos no domínio de nome identificam o
grupo que possue o nome. Por exemplo, o segmento purdue dá o nome da universidade
e google dá o nome da companhia. O DNS não especifica o número de segmentos no
nome. Em vez disso, cada organização pode escolher quantos segmentos usar nos seus
computadores e o que cada segmento representa.

O domain name system especifica valores para o segmento mais significativo,
que é chamado de domínio de nível superior (TLD, Top-Level Domain). Os domínios
de nível superior são controlados pela Internet Corporation for Assigned Names and
Numbers (ICANN), que designa um ou mais registros de domínio para administrar um
determinado domínio de nível superior e aprovar nomes específicos. Alguns TLDs são
genéricos, o que significa que estão geralmente disponíveis. Outros TLDs são restritos
a grupos específicos ou a agências governamentais. A Figura 4.16 lista exemplos de
domínios DNS de nível superior.

Uma organização escolhe um nome de acordo com um dos domínios de nível superior existentes. Por exemplo, a maioria das corporações dos EUA opta por se registrar
sob o domínio com. Assim, uma empresa chamada Foobar pode solicitar o domínio
foobar sob o domínio de nível superior com. Uma vez que o pedido for aprovado, será
atribuído à empresa Foobar o domínio:

[foobar.com](http://foobar.com/)

Se o nome já tiver sido atribuído a outra organização chamada Foobar, é possível
utilizar [foobar.biz](http://foobar.biz/) ou [foobar.org](http://foobar.org/), mas não [foobar.com](http://foobar.com/). Além disso, uma vez que foobar.
com tenha sido atribuído, a empresa Foobar pode escolher quantos níveis adicionais
sejam necessários para adicionar significado aos seus computadores. Assim, se a Foobar
tem filiais na costa Leste e Oeste, pode utilizar nomes como:

[computer1.east-coast.foobar.com](http://computer1.east-coast.foobar.com/)

![Untitled](Camada%20de%20Aplicac%CC%A7a%CC%83o%20ddac200b32e94b1796775963d5d5f14c/Untitled%2019.png)

ou pode escolher uma hierarquia de nomeação plana com todos os computadores identificados pelo nome seguido do nome do domínio da empresa:

[computer1.foobar.com](http://computer1.foobar.com/)

Além da estrutura organizacional familiar, o DNS permite que as organizações
usem um registro geográfico. Por exemplo, a organização Corporation For National Research Initiatives registrou o domínio:

[cnri.reston.va.us](http://cnri.reston.va.us/)

devido ao fato de a organização estar localizada na torre de Reston, Virgínia, nos Estados
Unidos. Assim, os nomes dos computadores na organização terminam com .us em vez
de .com.
Alguns países estrangeiros têm adotado uma combinação de nomes de domínios
geográficos e organizacionais. Por exemplo, universidades na Inglaterra registram sob
o domínio:

[ac.uk](http://ac.uk/)

onde ac é uma abreviação para academic e uk é o código oficial para United Kingdom.