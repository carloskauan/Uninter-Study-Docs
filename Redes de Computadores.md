# Aula 1 — Processos de Comunicação

## Objetivo da aula

Compreender como ocorre o processo de comunicação, seus principais elementos e como esse conceito é aplicado às redes de computadores.

---

# 1. O Modelo de Comunicação

Toda comunicação, seja entre pessoas ou dispositivos, segue um modelo básico composto por três elementos principais:

- **Transmissor (Emissor):** quem envia a mensagem.
- **Receptor:** quem recebe a mensagem.
- **Meio físico (Canal):** por onde a mensagem é transportada.

### Exemplo

- **Transmissor:** Pessoa A
- **Mensagem:** "Olá!"
- **Meio:** Voz
- **Receptor:** Pessoa B

Em redes de computadores:

- **Transmissor:** Computador A
- **Mensagem:** Dados
- **Meio:** Cabo de rede, Wi-Fi ou fibra óptica
- **Receptor:** Computador B

---

# 2. A Mensagem

A **mensagem** é a informação que será transmitida entre o emissor e o receptor.

Para que a comunicação seja bem-sucedida, a mensagem deve:

- ser compreensível para o receptor;
- estar no formato adequado ao meio de transmissão;
- ser enviada seguindo regras previamente definidas.

Sem esses cuidados, a comunicação pode falhar ou a mensagem pode ser interpretada incorretamente.

---

# 3. Linguagem de Comunicação

A mensagem precisa utilizar uma linguagem conhecida tanto pelo transmissor quanto pelo receptor.

### Comunicação entre pessoas

A linguagem pode ser:

- Verbal
- Escrita
- Gestual

**Exemplo:**

Uma pessoa que fala apenas português terá dificuldade para compreender uma mensagem enviada em japonês.

---

### Comunicação entre computadores

Nos sistemas digitais, a linguagem corresponde à **codificação da informação**, ou seja, à forma como os dados são representados para que ambos os dispositivos consigam interpretá-los corretamente.

---

# 4. Adequação ao Meio

Nem toda mensagem pode ser enviada diretamente.

Ela precisa ser adaptada ao meio de transmissão utilizado.

### Exemplos

| Meio | Forma da mensagem |
|-------|-------------------|
| Papel | Texto escrito |
| Voz | Ondas sonoras |
| Cabo de rede | Sinais elétricos |
| Fibra óptica | Pulsos de luz |
| Wi-Fi | Ondas de rádio |

Cada meio possui características próprias, exigindo uma forma específica de transmissão.

---

# 5. Codificação e Decodificação

Para que a mensagem possa trafegar pelo meio físico, ela passa por dois processos importantes.

## Codificação

É o processo de converter a mensagem para um formato adequado ao meio de transmissão.

## Decodificação

É o processo inverso: transformar os dados recebidos novamente em uma informação compreensível pelo receptor.

### Fluxo da comunicação

```text
Transmissor
      │
      ▼
Codificação
      │
      ▼
Meio de transmissão
      │
      ▼
Decodificação
      │
      ▼
Receptor
```

### Exemplo

Ao enviar uma mensagem pelo WhatsApp:

1. Você escreve o texto.
2. O aplicativo codifica os dados.
3. A mensagem é enviada pela internet.
4. O celular do destinatário recebe os dados.
5. O aplicativo decodifica a mensagem e a exibe na tela.

---

# 6. Protocolos de Comunicação

Os **protocolos** são conjuntos de regras que definem como a comunicação deve acontecer entre dispositivos.

Eles garantem que todos os equipamentos utilizem o mesmo padrão durante a troca de informações.

Sem protocolos, cada dispositivo se comunicaria de uma maneira diferente, tornando a comunicação praticamente impossível.

---

# 7. Por que existem vários protocolos?

Nem todas as comunicações possuem as mesmas necessidades.

Cada cenário exige características específicas.

### Exemplos

- Navegação na internet
- Envio de e-mails
- Chamadas de vídeo
- Transferência de arquivos
- Streaming de vídeo
- Jogos online

Por isso existem diferentes protocolos, cada um desenvolvido para uma finalidade específica.

---

# 8. Requisitos de um Protocolo

Um protocolo normalmente define:

- Como identificar o emissor e o receptor;
- Qual linguagem ou codificação será utilizada;
- Como os dados serão organizados;
- A velocidade de transmissão;
- Como confirmar que a mensagem foi recebida corretamente.

Essas regras garantem uma comunicação organizada e confiável.

---

# 9. Identificação dos Dispositivos

Antes de enviar uma mensagem, é necessário saber quem irá recebê-la.

### Redes telefônicas

Cada aparelho é identificado por um **número de telefone**.

### Redes de computadores

Cada dispositivo é identificado por um **endereço IP (Internet Protocol)**.

Esse endereço funciona como o "endereço" do equipamento dentro da rede.

---

# 10. Velocidade de Transmissão

A velocidade de transmissão representa a quantidade de dados que pode ser enviada em determinado intervalo de tempo.

Uma comunicação eficiente deve respeitar a capacidade do receptor.

Se os dados forem enviados mais rapidamente do que o receptor consegue processar, podem ocorrer:

- perda de informações;
- atrasos;
- necessidade de retransmissão.

---

# 11. Confirmação de Recebimento

Em muitas comunicações, o receptor informa ao transmissor que os dados chegaram corretamente.

Esse mecanismo aumenta a confiabilidade da transmissão.

Caso a confirmação não seja recebida, os dados podem ser enviados novamente.

---

# 12. Estrutura da Informação

Além do conteúdo da mensagem, é necessário definir como ela será organizada durante a transmissão.

Essa organização inclui:

- formato dos dados;
- divisão em partes menores quando necessário;
- encapsulamento das informações.

Essa estrutura permite que o receptor consiga reconstruir corretamente a mensagem original.

---

# Resumo da Aula

O processo de comunicação é formado pelos seguintes elementos:

```text
Transmissor
      │
Mensagem
      │
Codificação
      │
Meio de transmissão
      │
Decodificação
      │
Receptor
```

Para que a comunicação funcione corretamente, é necessário que:

- exista um transmissor e um receptor;
- ambos utilizem a mesma linguagem ou codificação;
- a mensagem seja adequada ao meio de transmissão;
- existam protocolos que definam as regras da comunicação;
- os dispositivos sejam identificados corretamente;
- haja controle da velocidade de transmissão;
- seja possível confirmar o recebimento dos dados quando necessário.

---

# Conceitos Importantes

| Conceito | Definição |
|----------|-----------|
| **Transmissor** | Dispositivo ou pessoa que envia a mensagem. |
| **Receptor** | Dispositivo ou pessoa que recebe a mensagem. |
| **Mensagem** | Informação que será transmitida. |
| **Meio Físico** | Canal por onde a mensagem é transportada. |
| **Codificação** | Conversão da mensagem para um formato adequado ao meio. |
| **Decodificação** | Conversão da mensagem recebida para um formato compreensível. |
| **Protocolo** | Conjunto de regras que controla a comunicação. |
| **Endereço IP** | Identificação única de um dispositivo em uma rede. |
| **Encapsulamento** | Organização da mensagem em estruturas próprias para transmissão. |

# Aula 2 — Comunicação de Dados

## Objetivo da aula

Compreender como ocorre a comunicação de dados entre dispositivos, os principais modelos de comunicação utilizados nas redes de computadores e as diferenças entre clientes e servidores.

---

# 1. O que é Comunicação de Dados?

A **comunicação de dados** é o processo de troca de informações entre dois ou mais dispositivos conectados por um meio de comunicação.

Ao contrário da comunicação humana, na comunicação de dados as mensagens são enviadas e recebidas por dispositivos digitais, como computadores, smartphones, servidores e outros equipamentos conectados à rede.

---

# 2. Comunicação Bidirecional

Na maioria das redes modernas, a comunicação é **bidirecional**, ou seja, ambos os dispositivos podem enviar e receber informações.

Cada terminal pode atuar como:

- **Transmissor:** quando envia dados.
- **Receptor:** quando recebe dados.

### Exemplo

Durante uma conversa no WhatsApp:

- Você envia uma mensagem.
- Seu amigo responde.

Nesse momento, ambos os celulares atuam como **transmissores e receptores**, alternando suas funções conforme a comunicação acontece.

---

# 3. Evolução dos Sistemas de Comunicação

## Sistema Inicial

As primeiras comunicações digitais utilizavam principalmente a **rede telefônica**, onde era estabelecida uma conexão direta entre dois pontos.

Esse modelo era conhecido como **conexão ponto a ponto**.

```text
Telefone A ─────────── Telefone B
```

Cada conexão era exclusiva entre os dois participantes.

---

## Redes de Dados

Com o crescimento da Internet, surgiram novos modelos de comunicação.

Os dois principais são:

- Comunicação **Ponto a Ponto (Peer-to-Peer - P2P)**;
- Comunicação **Cliente/Servidor**.

Cada modelo atende necessidades diferentes.

---

# 4. Modelo Cliente/Servidor

O modelo **Cliente/Servidor** é o mais utilizado atualmente na Internet.

Nele existem dois papéis principais.

## Cliente

É o dispositivo ou programa responsável por solicitar um serviço ou informação.

Exemplos:

- Navegador (Google Chrome, Firefox)
- Aplicativo do WhatsApp
- Aplicativo do Instagram
- Computador do usuário

O cliente **inicia a comunicação**.

---

## Servidor

É o computador responsável por fornecer serviços, dados ou recursos aos clientes.

Exemplos:

- Servidor de páginas da Web
- Servidor de banco de dados
- Servidor de e-mail
- Servidor do WhatsApp

O servidor **aguarda solicitações** e responde quando um cliente faz uma requisição.

---

## Funcionamento

```text
Cliente
    │
Solicita um serviço
    │
    ▼
Servidor
    │
Processa a solicitação
    │
    ▼
Envia a resposta
    │
    ▼
Cliente
```

### Exemplo

Quando você acessa um site:

1. Seu navegador envia uma solicitação.
2. O servidor recebe essa solicitação.
3. O servidor processa o pedido.
4. O servidor envia a página.
5. O navegador exibe o conteúdo.

---

# 5. Troca de Mensagens

Mesmo no modelo Cliente/Servidor, a comunicação continua sendo **bidirecional**.

Isso significa que:

- O cliente envia solicitações.
- O servidor responde.

Ambos enviam e recebem informações durante toda a comunicação.

---

# 6. Diferenças entre Cliente e Servidor

Embora utilizem os mesmos princípios de comunicação, clientes e servidores possuem características bastante diferentes.

## 6.1 Capacidade de Processamento

### Cliente

Normalmente executa apenas as tarefas do usuário.

Exemplos:

- Navegar na Internet;
- Assistir vídeos;
- Jogar;
- Utilizar aplicativos.

Seu processamento é voltado para um único usuário.

---

### Servidor

Um servidor precisa atender **vários clientes simultaneamente**.

Por isso possui:

- maior capacidade de processamento;
- mais memória RAM;
- maior capacidade de armazenamento;
- sistemas operacionais e softwares especializados.

---

## 6.2 Segurança

### Cliente

A segurança é voltada principalmente para proteger os dados do próprio usuário.

Exemplos:

- antivírus;
- firewall;
- autenticação.

---

### Servidor

Como armazena informações de muitos usuários, exige um nível muito maior de segurança.

Entre as medidas adotadas estão:

- controle rigoroso de acesso;
- criptografia;
- backups;
- monitoramento constante;
- segurança física do datacenter.

---

## 6.3 Software

### Cliente

Executa aplicações destinadas ao usuário final.

Exemplos:

- navegador;
- WhatsApp;
- Spotify;
- Microsoft Word.

---

### Servidor

Executa softwares capazes de atender diversas solicitações simultaneamente.

Esses programas permanecem aguardando conexões em **portas específicas**, respondendo às requisições dos clientes.

Exemplos:

- Servidor Web
- Servidor FTP
- Servidor de Banco de Dados

---

# 7. Hardware de um Servidor

Um servidor deve permanecer disponível praticamente o tempo todo.

Por isso, seu hardware é muito mais robusto que o de um computador comum.

Características importantes:

- Alto desempenho;
- Grande quantidade de memória;
- Armazenamento rápido;
- Fontes redundantes;
- Discos em RAID;
- Múltiplas interfaces de rede;
- Processadores de alta capacidade.

---

## Redundância

Uma das características mais importantes de um servidor é a **redundância**.

Redundância significa possuir componentes de reserva para evitar interrupções.

Exemplos:

- duas fontes de alimentação;
- vários discos rígidos em RAID;
- múltiplas placas de rede.

Se um componente falhar, outro continua funcionando.

O objetivo é manter o servidor disponível sem interromper os serviços.

---

# 8. Conectividade do Servidor

Um servidor deve ser capaz de atender diversos usuários ao mesmo tempo.

Por isso, sua conexão com a rede precisa suportar toda essa demanda.

### Exemplo

Se:

- 100 usuários estiverem conectados;
- cada um utilizar aproximadamente **100 Mb/s**;

o servidor deverá suportar aproximadamente:

```text
100 × 100 Mb/s = 10 000 Mb/s

10 000 Mb/s = 10 Gb/s
```

Quanto maior o número de clientes, maior deverá ser a capacidade de processamento e de comunicação do servidor.

---

# 9. Comunicação Ponto a Ponto (Peer-to-Peer — P2P)

Na comunicação **Ponto a Ponto (P2P)**, os dispositivos comunicam-se diretamente entre si, sem que um servidor central seja responsável por fornecer todos os dados.

Nesse modelo, cada dispositivo pode atuar simultaneamente como:

- Cliente;
- Servidor.

Ou seja, cada participante pode enviar e receber informações ao mesmo tempo.

---

## Exemplo em uma rede local

```text
Computador A ─────────── Computador B
```

Os dois computadores estão conectados diretamente.

---

## Exemplo na Internet

Aplicações P2P podem compartilhar arquivos diretamente entre os usuários.

Cada computador fornece uma parte das informações para os demais participantes da rede.

É assim que funcionam diversos sistemas de compartilhamento de arquivos.

---

# 10. Exemplo: Comunicação no WhatsApp

O WhatsApp utiliza principalmente o modelo **Cliente/Servidor**, mas o conceito abaixo ajuda a entender como ocorre a localização dos usuários.

Durante o processo de comunicação:

## Etapa 1 — Registro

Quando o aplicativo é iniciado, ele se conecta aos servidores do WhatsApp.

Esses servidores registram informações importantes, como:

- identificação do usuário;
- disponibilidade (online/offline);
- endereço de rede necessário para localizar o dispositivo.

```text
Celular
      │
Registro
      │
      ▼
Servidor do WhatsApp
```

---

## Etapa 2 — Localização

Quando você deseja conversar com alguém:

1. Seu aplicativo consulta o servidor.
2. O servidor informa onde o destinatário está disponível.
3. A comunicação pode então ser estabelecida.

```text
Cliente
      │
Consulta
      ▼
Servidor
      │
Informa onde está o destinatário
```

---

## Etapa 3 — Troca de Mensagens

Após localizar os participantes, ocorre a troca de mensagens.

> **Observação importante:** Na prática, o WhatsApp moderno utiliza seus próprios servidores para encaminhar as mensagens (modelo cliente/servidor). Diferentemente de aplicações P2P clássicas, as mensagens normalmente **não são enviadas diretamente de um celular para o outro** pela Internet. O exemplo apresentado serve para ilustrar o processo de registro e localização, mas não representa exatamente a arquitetura atual do WhatsApp.

---

# Resumo da Aula

Existem dois modelos principais de comunicação em redes:

## Cliente/Servidor

```text
Cliente
    │
Solicitação
    ▼
Servidor
    │
Resposta
    ▼
Cliente
```

Características:

- Mais utilizado na Internet;
- Centraliza os serviços;
- Servidor atende diversos clientes.

---

## Ponto a Ponto (P2P)

```text
Computador A ─────────── Computador B
```

Características:

- Comunicação direta entre os dispositivos;
- Cada participante pode atuar como cliente e servidor;
- Muito utilizado em sistemas de compartilhamento de arquivos.

---

# Conceitos Importantes

| Conceito | Definição |
|----------|-----------|
| **Comunicação de Dados** | Troca de informações entre dispositivos digitais. |
| **Comunicação Bidirecional** | Ambos os dispositivos enviam e recebem informações. |
| **Cliente** | Dispositivo que solicita um serviço ou recurso. |
| **Servidor** | Dispositivo que fornece serviços aos clientes. |
| **Cliente/Servidor** | Modelo em que clientes fazem requisições e servidores respondem. |
| **Ponto a Ponto (P2P)** | Comunicação direta entre dispositivos, onde ambos podem atuar como cliente e servidor. |
| **Redundância** | Existência de componentes de reserva para evitar interrupções. |
| **Porta de Comunicação** | Identificador utilizado pelos serviços para receber conexões específicas. |
| **Conectividade** | Capacidade de um dispositivo atender várias conexões simultaneamente. |
