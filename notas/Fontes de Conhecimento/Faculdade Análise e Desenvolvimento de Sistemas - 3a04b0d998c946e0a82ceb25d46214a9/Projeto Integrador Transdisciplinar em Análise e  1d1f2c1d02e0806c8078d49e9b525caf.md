# Projeto Integrador Transdisciplinar em Análise e Desenvolvimento de Sistemas I

Expressão Regular  é um método formal de se especificar o padrão de texto

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image.png)

Permite que padrões de caracteres sejam buscados, validados  e substituídos  quando necessário

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%201.png)

A Regex `^0[0-9]3[0-9]` pode ajudar a localizar partidas entre 4h30 e 41h35 min em um terminal de ônibus

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%202.png)

## Ferramentas

Regex na ferramenta VSCode

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%203.png)

Regex na ferramenta Siblime Text

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%204.png)

Através de código na procura a ferramenta localiza o código da Regex

## Meta Caracteres

Formada pelo agrupamento entre símbolos e caracteres literais, uma expressão pode ser considerada uma regra, pois, diante das condições estabelecidas, retorna somente os resultados positivos.

Os metacaracteres possuem funções especiais e não podem ser usados como um caractere literal; caso este seja o objetivo, o metacaractere deve ser precedido por um *escape* (\).

### Tipos de Metacaracteres

**Repersentante:** qualquer coisa ‘.’, lista ‘[…]’ e lista negada ‘[^…]’.

- 9 – busca o dígito 9 acompanhado de qualquer caractere.
- 9\. – busca o dígito 9 acompanhado de um ponto-final.
- [09] – busca os dígitos 0 ou 9.
- [0-9] – busca dígitos entre 0 e 9.
- [^5-9] – busca qualquer outro valor exceto os dígitos entre 5 e 9.
- [0-9]) – busca dígitos entre 0 e 9 seguidos por um parêntese de fechamento.
- [:digit:] – busca qualquer número, equivalente a [0-9].

**Quantificadores:** opicional ’?’, algum ‘+’, qualquer quantidade ‘*’, intervalor’{}’.

- código? – busca a ocorrência do termo no singular e no plural.
- </+html – match apenas com a tag de fechamento (1 ou mais ocorrências).
- </*html – busca tags de abertura e fechamento.
- \d{4} – busca uma sequência de dígitos com 4 posições.
- \d{9,11} – busca uma sequência de dígitos com 9 ou 11 posições.
- \d{9, } – busca uma sequência de dígitos com, no mínimo, 9 posições.

**Âncora:** início ‘^’ e fim de linha ‘$’, borda de palavras ‘\b’.

- ^[AO] – para localizar linhas iniciadas pelos artigos definidos.
- [.;]$ – busca linhas que encerram com um ponto-final ou ponto e vírgula.
- \bdia – match com as palavras dia, diafragma e bom-dia!
- dia\b – match com as palavras dia, melodia e bom-dia!
- \bdia\b – match com as palavras dia e bom-dia!

### Outros tipos de Metacaractere

- OU ‘a (b | c) d’ – match com ‘abd’ ou ‘acd’, enquanto ‘ablcd’ retornará ‘ab’ ou ‘cd’.
- Grupos ‘([0-9]{2})([0-9]{2})’ – a expressão é organizada em $1$2.
- Barra-letra – \d) – retorna sucesso quando um dígito seguido por um parêntese de fechamento é localizado.

| Barra-letra | Equivalente POSIX | Significa |
| --- | --- | --- |
| \d | [[:digit:]] | Dígito |
| \D | [^[:digit:]] | Não dígito |
| \w | [[:alnum:]] | Palavra |
| \W | [^[:alnum:]] | Não palavra |
| \s | [[:space:]] | Branco |
| \S | [^[:space:]] | Não branco |

### Expressões Regulares na GOOGLE SHEET 2

- REGEXMATCH confirmará se encontrou o padrão no texto.
- REGEXEXTRACT extrairá o texto que corresponde ao padrão.
- REGEXREPLACE substituirá o texto que corresponde ao padrão.

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%205.png)

![image.png](Projeto%20Integrador%20Transdisciplinar%20em%20Ana%CC%81lise%20e%20%201d1f2c1d02e0806c8078d49e9b525caf/image%206.png)

- **[:upper:]** - busca letras maiúsculas, equivalente a [A-Z];
- **[:lower:]** - busca letras minúsculas, equivalente a [a-z];
- **[:alpha:]** - busca letras maiúsculas e minúsculas, equivalente a [A-Za-z];
- **[:alnum:]** - busca letras e números, equivalente a [A-Za-z0-9];
- **[:digit:]** - busca letras e números, equivalente a [0-9];
- **[:punct:]** - busca sinais de pontuação, equivalente a [.' !?: ... ].