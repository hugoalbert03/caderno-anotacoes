# Camada de transporte: Protocolo UDP

# O UDP pode ser caracterizado como:

- **Fim-a-fim**. Ele é um protocolo de transporte que pode distinguir entre os vários
programas de aplicação executados em um computador.
- **Sem conexão**. A interface que o UDP fornece para as aplicações segue um para-
digma sem conexão.
- **Orientado à mensagem**. Uma aplicação que usa UDP envia e recebe mensagens
individuais.
- **Melhor esforço**. O UDP oferece às aplicações a mesma entrega via melhor esfor-
ço que é oferecida pelo IP.
- **Interação arbitrária**. O UDP permite que um aplicativo envie mensagens para
muitas outras aplicações, receba mensagens de muitas outras aplicações, ou se
comunique com exatamente outra aplicação.
- **Independente de sistema operacional**. O UDP fornece um meio de identificar
aplicações de forma independente do sistema operacional local.

> O UDP utiliza o paradigma de comunicação sem conexão, ou seja, uma aplicação que
utiliza UDP não precisa preestabelecer uma comunicação antes de enviar os dados nem
precisa informar quando terminar a comunicação; assim, ela pode gerar e enviar dados
a qualquer momento. Além disso, o UDP permite que um aplicativo insira um atraso
arbitrariamente longo entre a transmissão de duas mensagens.
>