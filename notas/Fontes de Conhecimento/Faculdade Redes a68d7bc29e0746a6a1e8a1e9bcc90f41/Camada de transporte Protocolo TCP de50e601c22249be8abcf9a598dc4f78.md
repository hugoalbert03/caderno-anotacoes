# Camada de transporte: Protocolo TCP

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled.png)

# Dica do professor

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%201.png)

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%202.png)

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%203.png)

Comunicação do endereço IP e identificação de portas

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%204.png)

Números de portas conhecidos

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%205.png)

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%206.png)

# Na prática

Sincronização de Dados de dispositivo para o Servidor e Vice-Versa

**Passo 1**

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%207.png)

O usuário envia uma requisição SYN

**Passo 2**

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%208.png)

O servidor responde com SYN ACK

**Passo 3**

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%209.png)

O cliente responde com o ACK estabelecendo conexão e confirmando o recebimento

**Regulação de Buffer Destinatário e Receptor**

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%2010.png)

Receptor de pequena capacidade

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%2011.png)

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%2012.png)

Multiplexação e Demultiplexação entrega dos dado contidos em um seguimentos de camada de transporte ao socket( Porta receptora de destino)

Multiplexação → reúne todos os dados, encapsula e envia para a camada de rede

Demultiplexação → Separa todas as partes dos pacotes e os dividem em processos

Os 4 elementos do Socket

1. IP de origem
2. Porta de origem
3. IP destino
4. Porta destino

![Untitled](Camada%20de%20transporte%20Protocolo%20TCP%20de50e601c22249be8abcf9a598dc4f78/Untitled%2013.png)

Varias portas de origem de varias máquinas enviam requisição a porta de destino