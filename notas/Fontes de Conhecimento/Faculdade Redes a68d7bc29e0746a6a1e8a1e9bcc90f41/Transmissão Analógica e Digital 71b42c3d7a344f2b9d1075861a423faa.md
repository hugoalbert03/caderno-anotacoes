# Transmissão Analógica e Digital

# Sinal analógico (Sinal de movimento contínuo)

## Analogia gráfica das ondas

**Horizontal →** *tempo da onda*
**Vertical →** *valor da onda*

# Sinal Digital

## Analogia gráfica das ondas

→ Conversão de dados digitais em sinais digitais
→ Variação de 0 e 1

### Codificação de linha

> Converte dados digitais em sinais digitais. Os dados podem ser textos, números, imagens, áudios, vídeos ou qualquer meio, mas sempre serão armazenados na memória do computador na forma de sequência de bits.
> 

### Codificação em bloco

> Fornece um desempenho melhor do que a codificação de linha, pois provê a redundância necessária para possibilitar a sincronização e, ainda, um mínimo de detecção de erros no código.
	→ Na codificação de bloco, um bloco de bits é transformado em um outro bloco de bits,      maior do que o bloco inicial.

	→ Geralmente, a codificação de bloco consiste nas etapas de divisão, em que uma            sequência de bits é dividida em grupos de bits; substituição, na qual um grupo de bits é substituído por outro grupo de bits; e combinação, quando os grupos de bits são recombinados para formar um fluxo de bits, que tem um número maior de bits do que o grupo de bits original.
> 

### Embaralhamento

> É utilizado quando é preciso substituir longos pulsos de nível zero por uma combinação de outros níveis, fornecendo sincronização.
> 

# Transmissão Analógica

- Calssificação de modulação
    - Amplitude
    - Frequência
    - Fase
    - Capaz de transmitir dados analógicos ou digitais
- **codificação polar:** a tensão oscila entre valores positivos e negativos;
- **codificação bipolar:** existem três níveis de tensão, que são o positivo,
o negativo e o zero;
- **codificação multinível:** apresenta envio de mais bits a cada variação
do sinal.
- **Modulação em amplitude:** nesse tipo de modulação, existe uma
variação da amplitude de uma portadora, de maneira proporcional
à informação enviada, ou seja, variando com um sinal. A portadora
vai continuar oscilando em uma frequência fixa, mas a amplitude da
onda vai variar. Na modulação em amplitude, somente a amplitude,
ou a magnitude, da onda senoidal recebe modificações. O gráfico do
tempo de uma portadora modulada vai ter uma forma semelhante à do
sinal que foi utilizado .

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled.png)

- **Modulação em frequência:** quando esse tipo de modulação é utilizado,
a amplitude da portadora vai permanecer inalterada, mas a frequência
vai se modificar de acordo com o sinal. Pode-se dizer que, quando o
sinal for forte, a frequência da portadora vai aumentar, e quando o sinal
for fraco, a frequência da portadora vai diminuir. A modulação em
Camada física 7
frequência  é mais difícil de ser observada, porque pequenas
alterações na frequência não são visíveis de maneira muito clara.

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%201.png)

**Modulação por deslocamento de fase:** esse tipo de modulação envolve o deslocamento de um tempo de referência na onda senoidal. A
modulação por fase é possível, mas apenas na teoria, pois raramente
se utiliza esse tipo de modulação em um sinal analógico. Isso acontece
porque, se a fase mudar após um ciclo, a próxima onda senoidal vai
começar um pouco depois, e qualquer atraso vai fazer a modulação
ficar parecida com uma alteração na frequência. É por isso que a modulação por deslocamento de fase pode ser confundida com
a modulação em frequência.

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%202.png)

# Multiplexação

Na multiplexação, o principal objetivo é partilhar, de maneira física, um
meio de comunicação entre várias conexões independentes e simultâneas
em um mesmo espaço de comunicação.

A multiplexação envolve a divisão
da capacidade de transmissão de um meio ou da banda passante desse meio
em porções menores, a fim de obter canais lógicos menores e independentes,
mas sempre no mesmo meio

O canal lógico é um elemento físico, tem caracterização física e não pode
ser confundido com o conceito de circuito ou canal virtual de rede. A divisão
em que a multiplexação consiste pode ser implementada por divisão de frequência ou por divisão de tempo.

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%203.png)

Quando a transmissão de dados passou a ser algo importante, as fontes de
informação eram praticamente todas analógicas, como o rádio, a televisão e
a telefonia. Dessa forma, era muito utilizada a forma de multiplexação em
frequência, que tem como principais características :

- ser o tipo mais antigo de multiplexação;
- aplicar-se muito bem a sinais analógicos;
- ser pouco eficiente, pois necessita de muita banda de resguardo;
- precisar de um determinado hardware para cada canal lógico;
- ter uma implementação complicada e de custo alto.

Com o passar do tempo, as fontes de informação foram tornando-se predominantemente digitais e, então, a multiplexação em tempo passou a ser mais comum.
As principais características desse tipo de multiplexação são:

- aplicar-se muito bem a sinais digitais;
- ser muito eficiente e não necessitar de quase nada de tempo de resguardo;
- poder ser implementado por software ou por hardware, de modo que
a implementação é mais fácil;
- o custo é mais baixo.

# Os modos de transmissão e a largura de banda

O termo modo de transmissão é utilizado quando se faz referência à forma
como os dados são enviados de um ponto a outro. Normalmente, os modos
de transmissão são divididos em dois tipos: a paralela e a serial.

A **transmissão paralela** é o tipo de transmissão em que vários bits são
enviados de uma só vez, e a **transmissão serial** é o tipo de transmissão em que
um bit é enviado por vez. Na **transmissão serial**, existe uma *categorização de
acordo com o tempo de transmissão*.

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%204.png)

## Transmissão Paralela

Esse tipo de transmissão é aquele em que vários bits de dados são transmitidos de cada vez, por meios de transmissão separados, geralmente
envolvendo meios com fios independentes. Os sinais em todos os fios são
sincronizados, isto é, cada bit trafega em cada um dos fios exatamente ao
mesmo tempo.

Além dos fios paralelos que transportam os dados, uma interface paralela possui outros fios, que vão permitir que o emissor e o receptor sejam
coordenados. Outra característica importante é que os fios de um sistema de
transmissão paralela ficam em um único cabo físico. Dessa forma, apenas um
cabo físico conecta o emissor e o receptor, e não um conjunto de fios físicos
independentes um do outro.

As principais vantagens na utilização da transmissão paralela são as seguintes (COMER, 2016):

- alta banda passante: como é possível enviar vários bits ao mesmo tempo,
então pode-se dizer que um sistema de transmissão paralela pode enviar
vários bits enquanto um sistema de transmissão serial envia apenas
um bit;
- semelhante ao hardware: se for observado internamente, o hardware
de comunicação utiliza circuitos paralelos, ou seja, um sistema de
transmissão paralela corresponde ao hardware interno.

## Transmissão serial

Esse tipo de transmissão é considerado uma alternativa à utilização da transmissão paralela, pois envia apenas um bit de cada vez. Apesar de parecer um
absurdo optar pela transmissão serial, principalmente em termos de velocidade
de transmissão, uma grande parte dos sistemas de comunicação utiliza esse
modo de transmissão. Essa preferência se dá, principalmente, por três motivos:

- o sistema de transmissão serial custa bem menos do que o sistema
de transmissão paralela, pois são necessários menos fios físicos e os
componentes eletrônicos utilizados são bem mais baratos;
- os sistemas de transmissão paralelos exigem que cada fio tenha o mesmo
comprimento, pois uma diferença de alguns milímetros já pode gerar
problemas na transmissão;
- os sinais nos fios paralelos podem causar ruídos eletromagnéticos que
vão causar interferência com os sinais em outros fios, sempre que as
taxas de dados forem extremamente elevadas.

Em um sistema de transmissão serial, os mecanismos podem ser divididos
em três tipos, dependendo de como as transmissões ficam divididas ao longo
do tempo

- **transmissão assíncrona:** é o tipo de transmissão que pode ocorrer a
qualquer tempo, tendo uma espera aleatória entre as transmissões dos
itens de dados. Esse tipo de sistema permite que o meio físico fique
inativo por um tempo indeterminado entre as transmissões. Esse é o
tipo de transmissão ideal para quando as aplicações geram dados de
forma aleatória, sem um espaço definido de tempo entre elas. Um bom
exemplo é quando existe um usuário que está lendo notícias na internet
e, a cada vez que ele finaliza a leitura em um site, ele clica no link de
outro para ler uma nova notícia, mas não se sabe precisar de quanto em
quanto tempo ele irá para outro link. A maior desvantagem desse tipo de
transmissão é que o emissor e o receptor perdem a coordenação entre
eles, pois não se pode determinar por quanto tempo o meio ficará inativo;
- **transmissão síncrona:** caracteriza a principal alternativa ao tipo de
transmissão assíncrona, e é o tipo de transmissão que acontece de
forma contínua, sem nenhum intervalo de tempo de espera entre as
transmissões dos itens de dados. Nesse tipo, finalizada a transmissão
do último bit de um byte de dados, o emissor transmite um bit do
próximo byte de dados, o que avisa ao receptor que a transmissão vai
continuar. A principal vantagem desse tipo de transmissão é que o
emissor e o receptor ficam sincronizados o tempo todo, não perdem a
coordenação entre eles;
- **transmissão isócrona:** é o tipo de transmissão que acontece com um
intervalo de tempo fixo entre as transmissões dos itens de dados. Ele
pode ser visto como uma variação do tipo de transmissão síncrona, e
foi elaborado para oferecer um fluxo contínuo de bits, utilizado em
aplicações de voz ou de vídeo, pois a entrega de dados desse tipo, a uma
taxa constante, é o elemento mais importante, uma vez que atrasos não
são bem-vindos. Nesse sistema de transmissão, não é preciso que existam
dados para serem transmitidos, uma vez que a rede é concebida para
receber e enviar dados de forma ritmada e em intervalos fixos de tempo.

## Largura de banda

A largura de banda consiste na faixa de frequências ocupada pelo sinal modulado e pode fazer referência tanto à transmissão de dados analógica quanto
à transmissão de dados digital. Veja, a seguir, os tipos de
largura de banda de sinal analógico e digital.

- Largura de banda de sinal analógico: esse tipo de largura de banda
pode ser definido como a diferença entre as frequências mais altas e
mais baixas das partes integrantes do sistema. Para o cálculo, utiliza-
-se a análise de Fourier para saber as frequências maiores e menores.
Como exemplo, pode-se imaginar um sistema que produza sinais de 1
e 2 Hertz, o que, nesse caso, significa que a largura de banda de sinal
analógico é de 1 Hertz.
- **Largura de banda de sinal digital:** esse tipo de largura de banda
também utiliza a análise de Fourier para encontrar as ondas senoidais integrantes do sistema e, assim, poder verificar as frequências.
Quando esse tipo de análise é aplicado em uma onda quadrada, como
é o sinal digital, é produzido um conjunto infinito de ondas senoidais,
que seguem até o infinito. Nesse sentido, é possível compreender que
a largura de banda de um sinal digital é infinita, pois as frequências
crescem até o infinito.

# Dica do professor

**Codificação:**  processo de conversão de dados analógicos e digitais em sinal digitais

- Pode ter vário formatos, executados em formas de bits

**Modulações:** conversões de dados analógicos e digitais em  sinais analógicos

> Uma onda portadora consiste em um sinal de alta frequência que tem amplitude e frequência constantes e é gerado a partir de um oscilador de frequência de rádio
> 

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%205.png)

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%206.png)

## AM / FM

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%207.png)

**AM:** Modulação de Amplitude

**FM:** Modulação de frequência

**Multiplexação:** É utilizada para distribuir informações de várias entradas para uma única saída

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%208.png)

**Demutiplexação:** Múltiplas saídas de uma entrada

![Untitled](Transmissa%CC%83o%20Analo%CC%81gica%20e%20Digital%2071b42c3d7a344f2b9d1075861a423faa/Untitled%209.png)

Recupera os sinais misturados no canal e restaura-los  como sinais  individuais.

**Half Duplex** – Fluxo duplo entre as estações, mas não simultâneo. 

**Full Duplex** – Fluxo simultâneo de informações.