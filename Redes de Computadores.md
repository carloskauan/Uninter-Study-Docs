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

# Aula 3 — Componentes de Redes

## Objetivo da aula

Compreender quais são os principais componentes de uma rede de computadores, suas funções e como eles são representados em projetos e documentações de redes.

---

# 1. Componentes de uma Rede

Uma rede de computadores é formada por **três categorias principais** de componentes:

1. **Dispositivos Finais**
2. **Dispositivos Intermediários**
3. **Meios Físicos**

Cada categoria possui uma função específica para que a comunicação entre os dispositivos ocorra corretamente.

---

# 2. Representação em Diagramas de Rede

Em projetos de redes, utiliza-se uma **simbologia padronizada** para representar cada equipamento.

Esses diagramas permitem visualizar:

- como os dispositivos estão conectados;
- o caminho percorrido pelos dados;
- os equipamentos presentes na infraestrutura;
- a organização da rede.

> **Importante:** A simbologia pode variar de acordo com o fabricante (Cisco, MikroTik, Huawei, etc.), mas a função de cada equipamento permanece a mesma.

---

# 3. Dispositivos Finais (Hosts)

Os **dispositivos finais** são aqueles que iniciam ou recebem uma comunicação na rede.

São chamados de **Hosts**, pois estão localizados nas extremidades da comunicação.

### Definição

Um **Host** é qualquer dispositivo conectado à rede capaz de enviar e/ou receber informações.

---

## Exemplos de Hosts

- Computadores
- Notebooks
- Smartphones
- Tablets
- Impressoras de rede
- Servidores
- Smart TVs
- Câmeras IP
- Dispositivos IoT
- Consoles de videogame

Todos esses equipamentos podem participar do processo de comunicação.

---

## Identificação de um Host

Para que um Host possa participar da rede, ele precisa ser identificado.

Essa identificação permite que outros dispositivos saibam para onde enviar as informações.

### Exemplo

Em redes TCP/IP, essa identificação é feita por meio do:

- **Endereço IP (Internet Protocol)**

O endereço IP funciona como o "endereço" do dispositivo dentro da rede.

Sem um identificador, um Host não pode participar corretamente da comunicação.

---

## Função dos Hosts

Os Hosts são responsáveis por:

- iniciar comunicações;
- receber informações;
- executar aplicações;
- consumir ou fornecer serviços.

Dependendo da situação, um Host pode atuar como:

- Cliente;
- Servidor;
- Ambos (em aplicações P2P).

---

# 4. Dispositivos Intermediários

Os **dispositivos intermediários** são responsáveis por conectar os Hosts entre si e encaminhar os dados pela rede.

Eles não são o destino final da comunicação, mas fazem com que as informações cheguem corretamente ao destinatário.

---

## Principais funções

- Interligar dispositivos.
- Encaminhar pacotes.
- Controlar o tráfego da rede.
- Ampliar a cobertura da rede.
- Permitir a comunicação entre diferentes segmentos.

---

## Exemplos

### Switch

Conecta diversos dispositivos dentro da mesma rede local (LAN).

```text
Computador
      │
      ▼
   Switch
      │
 ┌────┴────┐
 │         │
PC      Impressora
```

---

### Roteador (Router)

Conecta redes diferentes.

O exemplo mais comum é conectar a rede da sua casa à Internet.

```text
Internet
     │
     ▼
 Roteador
     │
 ┌───┴────┐
 │        │
PC     Celular
```

---

### Access Point (AP)

Permite que dispositivos sem fio (Wi-Fi) acessem a rede.

```text
Notebook )))))
             \
          Access Point
               │
            Switch
```

---

# Diferença entre os dispositivos intermediários

| Equipamento | Função principal |
|-------------|------------------|
| **Switch** | Conecta dispositivos dentro da mesma rede local. |
| **Roteador** | Conecta redes diferentes e encaminha os dados entre elas. |
| **Access Point** | Fornece acesso à rede por meio do Wi-Fi. |

---

# 5. Meios Físicos

Os **meios físicos** são os canais utilizados para transportar os dados entre os dispositivos da rede.

É por meio deles que a comunicação realmente acontece.

---

## Principais tipos

### Cabo de cobre

Utiliza sinais elétricos para transportar informações.

Exemplo:

- Cabo de rede Ethernet (UTP).

---

### Fibra óptica

Utiliza pulsos de luz.

Vantagens:

- Alta velocidade;
- Longas distâncias;
- Baixa interferência eletromagnética.

É muito utilizada pelos provedores de Internet.

---

### Radiofrequência

Utiliza ondas de rádio para transmitir informações.

Exemplos:

- Wi-Fi;
- Bluetooth;
- Redes móveis (4G e 5G).

Sua principal vantagem é eliminar a necessidade de cabos.

---

# Comparação dos meios físicos

| Meio físico | Tipo de sinal | Exemplo |
|-------------|---------------|----------|
| Cabo de cobre | Sinais elétricos | Ethernet (UTP) |
| Fibra óptica | Pulsos de luz | Backbone de provedores |
| Radiofrequência | Ondas de rádio | Wi-Fi, Bluetooth, 4G e 5G |

---

# Como ocorre a comunicação

Durante uma comunicação, os três componentes trabalham juntos.

Exemplo:

```text
Notebook (Host)
        │
        │ Wi-Fi
        ▼
Access Point
        │
        ▼
Switch
        │
        ▼
Roteador
        │
        │ Fibra óptica
        ▼
Internet
        │
        ▼
Servidor (Host)
```

Observe que:

- O **Notebook** e o **Servidor** são **Hosts**.
- O **Access Point**, o **Switch** e o **Roteador** são **dispositivos intermediários**.
- O **Wi-Fi** e a **Fibra Óptica** são os **meios físicos** utilizados para transportar os dados.

---

# Resumo da Aula

Uma rede é composta por três elementos fundamentais:

## 1. Dispositivos Finais (Hosts)

São os equipamentos que enviam ou recebem informações.

Exemplos:

- Computadores;
- Smartphones;
- Servidores;
- Impressoras;
- IoT.

---

## 2. Dispositivos Intermediários

São responsáveis por conectar os Hosts e encaminhar os dados.

Exemplos:

- Switch;
- Roteador;
- Access Point.

---

## 3. Meios Físicos

São os canais utilizados para transportar as informações.

Exemplos:

- Cabo de cobre;
- Fibra óptica;
- Radiofrequência.

---

# Conceitos Importantes

| Conceito | Definição |
|----------|-----------|
| **Host** | Dispositivo final capaz de enviar e receber informações na rede. |
| **Endereço IP** | Identificador de um Host em uma rede TCP/IP. |
| **Dispositivo Intermediário** | Equipamento que conecta Hosts e encaminha os dados. |
| **Switch** | Interliga dispositivos dentro da mesma rede local. |
| **Roteador** | Conecta redes diferentes e encaminha o tráfego entre elas. |
| **Access Point (AP)** | Permite que dispositivos sem fio acessem a rede. |
| **Meio Físico** | Canal utilizado para transportar os dados entre dispositivos. |

# Tema 4 - Classificação das redes

Abragencia das redes: Desde a rede domestica até a rede mundial(internet)
Redes domesticas Terminais de usuario e dispositivos smart
Redes residenciais:SOHO (Small Office/ Home Office)
Rede mundial: WWW (World Wide Web)

Classificação usual: Redes locais, LAN - Local Area Network e redes de grande abrangencia geografica WAN - Wide Area Network

Acesso a internet: ISP (Internet Service Provide) no final voce como usuario utiliza um provedor que se conectam entre si.


Carateristicas da rede LAN: Conexão dos dispositivos finais em area limitada como em escolas, residencias, escritorios, industrias, campus...etc. São utilizados dispositivos intermediarios como switchs e acess point. Redes corporativas são admistrada por uma unica corporação e redes residenciais por um unico individuo e utilizam largura de banda de alta velocidade como 1gbps.

Carcteristicas da rede WAN: É uma interconexão das redes LAN de uma forma publica.O acesso a WAN e feito atraves de um provedor de acesso a internet(ISP) ou empressas de telecomunicações. Tem a taxa de transmissão menorque a rede LAN pois altas taxas de transmissão geram mais custo, no trafego corporativo temos servidores internos com menor demanda WAN pois a maioria das demandas já estão em rede local e servidores internos e na rsidencial temos maior demanda e pode apresentar gargalo de trafego  pois a maior demanda e de conexão a WAN.O dispositivo responsavel por conectar a rede LAN e WAN e o Roteador.

# Aula 4 — Classificação das Redes

## Objetivo da aula

Compreender como as redes de computadores são classificadas de acordo com sua **abrangência geográfica**, conhecendo as características das redes **LAN (Local Area Network)** e **WAN (Wide Area Network)**, além da importância dos provedores de Internet (ISP) na comunicação entre redes.

---

# 1. Classificação das Redes

As redes de computadores podem ser classificadas de acordo com a **área geográfica que abrangem**.

Essa classificação ajuda a entender:

- o tamanho da rede;
- como os dispositivos se comunicam;
- quais equipamentos são utilizados;
- qual é o alcance da comunicação.

As duas classificações mais utilizadas são:

- **LAN (Local Area Network)** — Rede Local.
- **WAN (Wide Area Network)** — Rede de Longa Distância ou Grande Abrangência.

---

# 2. Abrangência das Redes

As redes podem variar desde uma pequena rede doméstica até a maior rede existente no mundo: **a Internet**.

## Exemplos

- Rede doméstica.
- Rede residencial (Home Office).
- Rede empresarial.
- Rede de uma escola.
- Rede de uma universidade.
- Internet.

Quanto maior a abrangência da rede, maior será sua complexidade.

---

# 3. Redes Domésticas

As redes domésticas conectam dispositivos utilizados no dia a dia de uma residência.

### Exemplos de dispositivos

- Computadores;
- Notebooks;
- Smartphones;
- Smart TVs;
- Impressoras;
- Videogames;
- Dispositivos IoT (câmeras, lâmpadas inteligentes, assistentes virtuais etc.).

Normalmente todos esses equipamentos compartilham:

- Internet;
- Arquivos;
- Impressoras;
- Serviços da rede local.

---

# 4. Redes SOHO (Small Office / Home Office)

SOHO significa:

> **Small Office / Home Office**
>
> (Pequeno Escritório / Escritório em Casa)

São redes utilizadas por:

- pequenos escritórios;
- consultórios;
- empresas de pequeno porte;
- profissionais que trabalham em casa.

Essas redes possuem características semelhantes às redes domésticas, porém costumam atender um número maior de usuários e equipamentos.

---

# 5. Rede Mundial

A maior rede existente é a **Internet**.

Ela conecta milhões de redes locais espalhadas pelo mundo.

É importante diferenciar dois conceitos:

## Internet

É a infraestrutura mundial formada pela interligação de milhares de redes.

## WWW (World Wide Web)

A **World Wide Web (WWW)** é um dos serviços que utiliza a Internet.

Ela corresponde ao conjunto de páginas e sites acessados pelos navegadores.

### Importante

A WWW **não é a Internet**.

Ela é apenas um dos diversos serviços disponíveis na Internet.

Outros serviços incluem:

- E-mail;
- FTP;
- Jogos online;
- Chamadas de vídeo;
- Streaming;
- Mensagens instantâneas.

---

# 6. LAN (Local Area Network)

## Definição

Uma **LAN** é uma rede que conecta dispositivos dentro de uma área geográfica limitada.

Seu objetivo é permitir a comunicação rápida entre dispositivos próximos.

---

## Exemplos de LAN

- Residências;
- Escolas;
- Escritórios;
- Empresas;
- Universidades;
- Indústrias;
- Campus.

---

## Características da LAN

- Área geográfica limitada.
- Alta velocidade de transmissão.
- Baixa latência.
- Administração geralmente feita por uma única pessoa ou organização.
- Comunicação entre dispositivos próximos.

---

## Dispositivos encontrados em uma LAN

### Hosts

- Computadores;
- Servidores;
- Smartphones;
- Impressoras.

### Dispositivos intermediários

- Switch;
- Access Point;
- Roteador (para acesso à Internet).

---

## Administração

Em uma empresa:

A LAN normalmente é administrada pela equipe de TI da organização.

Em uma residência:

A administração geralmente é feita pelo próprio proprietário da rede.

---

## Velocidade

As redes LAN normalmente possuem altas velocidades.

Exemplos:

- 100 Mbps
- 1 Gbps
- 2,5 Gbps
- 10 Gbps

Como os dispositivos estão próximos, é possível utilizar velocidades elevadas com baixo custo.

---

# 7. WAN (Wide Area Network)

## Definição

Uma **WAN** é uma rede que conecta várias redes LAN distribuídas por grandes áreas geográficas.

Em vez de conectar diretamente computadores, a WAN conecta **redes inteiras**.

---

## Exemplos

- Internet.
- Redes entre filiais de uma empresa.
- Redes de operadoras de telecomunicações.

---

## Como uma LAN acessa uma WAN?

O acesso ocorre através de um:

- **ISP (Internet Service Provider)**

ou seja,

**Provedor de Serviços de Internet**.

Exemplos conhecidos:

- Claro;
- Vivo;
- TIM;
- Oi.

O provedor conecta a sua rede local à infraestrutura mundial da Internet.

---

# 8. ISP (Internet Service Provider)

O ISP é a empresa responsável por fornecer acesso à Internet.

Seu papel é:

- conectar sua rede doméstica à Internet;
- fornecer um endereço IP público;
- encaminhar os dados para outras redes.

Sem um ISP, uma rede LAN consegue funcionar internamente, mas não consegue acessar a Internet.

---

# 9. Características da WAN

Uma WAN possui características diferentes de uma LAN.

### Área geográfica

Muito maior.

Pode conectar cidades, estados, países e continentes.

---

### Velocidade

Em geral, a velocidade disponível na WAN é menor que na LAN.

Isso ocorre porque transmitir dados por longas distâncias exige uma infraestrutura muito mais complexa e cara.

---

### Custo

Quanto maior a velocidade contratada na WAN, maior tende a ser o custo do serviço.

---

### Administração

Normalmente é administrada por:

- provedores de Internet;
- operadoras de telecomunicações;
- grandes empresas.

---

# 10. LAN x WAN em empresas

Em uma empresa, grande parte da comunicação ocorre dentro da própria LAN.

Por exemplo:

- acesso ao servidor de arquivos;
- impressão em rede;
- sistemas internos;
- banco de dados local.

Esses acessos **não utilizam a Internet**, tornando a comunicação mais rápida e reduzindo o tráfego na WAN.

A WAN é utilizada principalmente para:

- acessar sites;
- enviar e-mails externos;
- utilizar serviços em nuvem;
- conectar filiais;
- acessar sistemas hospedados fora da empresa.

---

# 11. LAN x WAN em residências

Em uma residência, a situação costuma ser diferente.

Grande parte do tráfego é destinada à Internet.

Exemplos:

- YouTube;
- Netflix;
- Jogos online;
- Redes sociais;
- Navegação na Web.

Por isso, o uso da WAN costuma ser muito maior do que em muitas redes corporativas.

---

# 12. O papel do Roteador

O roteador é o dispositivo responsável por conectar a **LAN** à **WAN**.

Ele recebe os dados da rede local e os encaminha para outras redes, como a Internet.

Sem um roteador:

- os dispositivos da LAN continuam se comunicando entre si;
- porém, não conseguem acessar a Internet.

---

# Exemplo de comunicação

```text
Notebook
     │
 Wi-Fi
     │
Access Point
     │
Switch
     │
Roteador
     │
ISP (Provedor)
     │
Internet (WAN)
     │
Servidor
```

Nesse exemplo:

- **Notebook** → Host.
- **Access Point** → Conecta dispositivos Wi-Fi à LAN.
- **Switch** → Interliga os dispositivos da LAN.
- **Roteador** → Conecta a LAN à WAN.
- **ISP** → Fornece acesso à Internet.
- **Internet** → WAN.
- **Servidor** → Host.

---

# Resumo da Aula

## LAN (Local Area Network)

- Rede local.
- Área geográfica limitada.
- Alta velocidade.
- Administrada por uma única organização ou pessoa.
- Utilizada em residências, empresas, escolas e universidades.

---

## WAN (Wide Area Network)

- Rede de grande abrangência.
- Conecta diversas LANs.
- Utiliza provedores de Internet (ISP).
- Maior custo de infraestrutura.
- Velocidade geralmente menor que a da LAN.

---

## ISP

- Empresa que fornece acesso à Internet.
- Conecta a LAN à WAN.
- Encaminha o tráfego para outras redes.

---

## Roteador

- Conecta a rede local (LAN) à rede de longa distância (WAN).
- Permite o acesso à Internet.

---

# Conceitos Importantes

| Conceito | Definição |
|----------|-----------|
| **LAN** | Rede local utilizada em áreas geográficas limitadas. |
| **WAN** | Rede de longa distância que conecta várias LANs. |
| **ISP** | Empresa que fornece acesso à Internet. |
| **SOHO** | Small Office / Home Office (Pequeno Escritório / Escritório em Casa). |
| **WWW** | World Wide Web, conjunto de páginas e sites acessados pela Internet. |
| **Internet** | Infraestrutura mundial que interliga milhares de redes. |
| **Roteador** | Dispositivo que conecta a LAN à WAN. |
