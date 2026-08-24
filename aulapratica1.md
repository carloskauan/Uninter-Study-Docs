# Rede LAN Básica no Cisco Packet Tracer

## 1. O que é uma rede LAN básica?

Uma **LAN (Local Area Network)** é uma rede local utilizada para conectar dispositivos dentro de uma área limitada, como uma residência, laboratório, escritório ou empresa.

No Cisco Packet Tracer, uma topologia LAN básica pode ser representada por:

* **PCs/hosts** — dispositivos finais que utilizam a rede.
* **Switch** — equipamento responsável por conectar os dispositivos dentro da LAN.
* **Servidor** — pode fornecer serviços para os demais dispositivos, como DNS, DHCP, HTTP etc.
* **Cabos** — representam os meios físicos utilizados para transportar os dados.

Uma topologia simples pode ser representada assim:

```text
PC1 ───┐
PC2 ───┤
PC3 ───┤── Switch ─── Servidor
PC4 ───┘
```

> **Ideia principal:** os hosts normalmente se conectam ao switch, e o switch permite que eles se comuniquem dentro da rede local.

---

# 2. Meio físico da conexão

Para estabelecer a conexão física entre os dispositivos, utilizamos meios de transmissão.

### Cabo UTP

O **UTP (Unshielded Twisted Pair)** é um dos meios mais comuns em redes Ethernet.

No Packet Tracer, ele é representado pelos cabos de cobre, como o **Copper Straight-Through**.

Em uma rede real, o cabo UTP é muito utilizado para conectar:

* PC → Switch
* Servidor → Switch
* Switch → Switch
* Roteador → Switch

### Fibra óptica

A **fibra óptica (FO)** também pode ser utilizada, principalmente quando precisamos de:

* maiores distâncias;
* maior capacidade de transmissão;
* menor interferência eletromagnética.

Em uma rede empresarial, por exemplo, podemos utilizar fibra para interligar switches localizados em diferentes áreas do prédio.

---

# 3. Tipos de switch

Existem diferentes tipos de switches.

### Switch Layer 2 — Cisco 2960

O **Cisco Catalyst 2960** é um exemplo de switch predominantemente de **Camada 2 (Layer 2)**.

Ele trabalha principalmente com:

* endereços MAC;
* VLANs;
* quadros Ethernet;
* comunicação dentro da rede local.

### Switch Layer 3 — Cisco 3560

O **Cisco Catalyst 3560** possui recursos de **Camada 3**, podendo trabalhar também com funções de roteamento IP.

Isso permite, por exemplo, realizar o roteamento entre diferentes VLANs.

### Switches genéricos

Alguns switches presentes no Packet Tracer representam equipamentos mais flexíveis, nos quais podemos adicionar diferentes tipos de interfaces, dependendo do modelo.

> **Importante:** o tipo de switch escolhido depende da função que ele terá na rede. Para uma LAN simples, um switch Layer 2 normalmente é suficiente.

---

# 4. Montando a LAN no Packet Tracer

Depois de posicionar os dispositivos, precisamos estabelecer as conexões físicas.

Por exemplo:

```text
PC1 ─────┐
PC2 ─────┤
PC3 ─────┤── Switch 2960
PC4 ─────┘
```

Cada PC deve ser conectado a uma porta Ethernet do switch.

Depois de realizar as conexões, o Packet Tracer mostrará o estado das interfaces.

Quando uma conexão está funcionando corretamente, os indicadores das portas tendem a mudar para o estado operacional correspondente.

### Atenção ao conceito de loop

Em uma rede Ethernet, precisamos evitar **loops de Camada 2**.

Quando existem caminhos físicos redundantes entre switches, pode ocorrer um loop.

Para evitar problemas desse tipo, switches Cisco podem utilizar protocolos como o **STP (Spanning Tree Protocol)**.

O STP identifica caminhos redundantes e pode colocar determinadas portas em estado de bloqueio, evitando que os quadros circulem indefinidamente pela rede.

> **Resumo:** redundância pode ser útil para disponibilidade, mas precisa ser controlada para evitar loops.

---

# 5. Configurando os endereços IP dos hosts

Depois de montar a parte física da rede, precisamos configurar a parte lógica.

Cada dispositivo que precisa participar da comunicação IP deve possuir um **endereço IP**.

Para este laboratório, vamos utilizar a rede:

```text
192.168.10.0/24
```

Nesse caso:

```text
192.168.10 = identificação da rede
X          = identificação do dispositivo
```

Por exemplo:

```text
PC1 → 192.168.10.1
PC2 → 192.168.10.2
PC3 → 192.168.10.3
PC4 → 192.168.10.4
```

A máscara de sub-rede utilizada será:

```text
255.255.255.0
```

## Configurando um PC

No Packet Tracer:

```text
PC
 └── Desktop
      └── IP Configuration
```

Configure, por exemplo:

```text
IP Address:      192.168.10.1
Subnet Mask:     255.255.255.0
```

Faça o mesmo nos demais hosts, utilizando endereços diferentes.

### Por que os IPs precisam ser diferentes?

Cada dispositivo dentro da mesma rede deve possuir um endereço IP único.

Por exemplo, isto está correto:

```text
PC1 → 192.168.10.1
PC2 → 192.168.10.2
PC3 → 192.168.10.3
```

Mas isto está errado:

```text
PC1 → 192.168.10.1
PC2 → 192.168.10.1
```

Dois dispositivos não devem utilizar o mesmo IP na mesma rede, pois isso gera um **conflito de endereço IP**.

---

# 6. Testando a comunicação com o Ping

Depois de configurar os endereços IP, podemos verificar se os hosts conseguem se comunicar.

No Packet Tracer:

```text
PC
 └── Desktop
      └── Command Prompt
```

Utilize:

```bash
ping 192.168.10.2
```

Se estivermos executando o comando a partir do PC com IP `192.168.10.1`, estaremos testando a comunicação entre:

```text
PC1
192.168.10.1
      │
      │
      ▼
   Switch
      │
      │
      ▼
PC2
192.168.10.2
```

Se a comunicação estiver funcionando, receberemos respostas do dispositivo de destino.

### O que o ping está verificando?

O `ping` utiliza o **ICMP (Internet Control Message Protocol)** para verificar se existe conectividade IP entre origem e destino.

Portanto, quando fazemos:

```bash
ping 192.168.10.2
```

estamos basicamente perguntando:

> "Consigo alcançar o dispositivo que possui o endereço IP 192.168.10.2?"

---

# 7. Acessando o switch pela porta Console

Até agora configuramos os hosts.

Agora vamos configurar o switch.

Uma das maneiras de realizar a configuração inicial de um switch é através da **porta Console**.

A conexão pode ser representada assim:

```text
PC
 │
 │ Cabo Console
 │
 ▼
Switch
```

No Packet Tracer, conectamos o cabo Console do PC à porta Console do switch.

Depois:

```text
PC
 └── Desktop
      └── Terminal
```

Ao abrir o Terminal, podemos aceitar as configurações iniciais apresentadas pelo Packet Tracer.

Assim teremos acesso à CLI (**Command-Line Interface**) do switch.

---

# 8. Modos da CLI do Cisco IOS

Ao acessar o switch, podemos encontrar diferentes modos de operação.

### User EXEC

Representado por:

```text
Switch>
```

É o modo inicial, com acesso limitado a determinados comandos.

### Privileged EXEC

Utilizamos:

```bash
enable
```

O prompt muda para:

```text
Switch#
```

Esse modo permite executar comandos administrativos e acessar o modo de configuração.

### Global Configuration

Utilizamos:

```bash
configure terminal
```

O prompt passa para:

```text
Switch(config)#
```

Nesse modo podemos alterar diversas configurações do equipamento.

> **Regra importante para memorizar:**

```text
Switch>
      │
      │ enable
      ▼
Switch#
      │
      │ configure terminal
      ▼
Switch(config)#
```

---

# 9. Configurando um endereço IP para o switch

Um switch Layer 2 encaminha quadros utilizando principalmente endereços MAC, mas podemos configurar um endereço IP para permitir o **gerenciamento remoto** do equipamento.

Para isso, utilizamos uma interface VLAN, normalmente a VLAN 1 em um laboratório simples.

Primeiro:

```bash
enable
configure terminal
```

Depois:

```bash
interface vlan 1
```

Agora estamos configurando a interface virtual da VLAN 1.

Podemos atribuir o endereço:

```bash
ip address 192.168.10.101 255.255.255.0
```

A configuração ficará conceitualmente assim:

```text
Switch
 └── VLAN 1
      └── IP: 192.168.10.101
          Máscara: 255.255.255.0
```

---

# 10. Ativando a interface VLAN

Depois de configurar o endereço IP, precisamos verificar o estado da interface.

Podemos utilizar:

```bash
show ip interface brief
```

Esse comando apresenta um resumo das interfaces e seus estados.

Podemos encontrar algo semelhante a:

```text
Interface              IP-Address       Status       Protocol
Vlan1                  192.168.10.101   up           up
```

O objetivo é que a interface esteja operacional.

Se necessário, podemos utilizar:

```bash
no shutdown
```

Esse comando significa:

> **"Não desligue administrativamente esta interface."**

Ou seja, ele habilita a interface caso ela esteja administrativamente desativada.

> **Observação importante:** em uma SVI (como `interface vlan 1`), o fato de usar `no shutdown` não garante sozinho que ela ficará `up/up`; ela também precisa ter condições de operação, como uma porta física ativa pertencente à VLAN.

---

# 11. Configurando acesso remoto com VTY

Agora precisamos configurar as linhas **VTY**.

As linhas VTY são **linhas virtuais utilizadas para sessões de acesso remoto ao equipamento**, como Telnet e, dependendo da configuração, SSH.

Utilizamos:

```bash
line vty 0 5
```

Isso seleciona as linhas virtuais de **0 a 5**.

Em outras palavras, estamos configurando um conjunto de linhas que podem ser utilizadas para conexões remotas ao switch.

Depois podemos configurar uma senha:

```bash
password sua_senha
```

E exigir que essa senha seja utilizada:

```bash
login
```

A sequência fica:

```bash
line vty 0 5
password sua_senha
login
```

---

# 12. Acessando o switch remotamente com Telnet

Depois que o switch estiver configurado e conectado à rede, podemos tentar acessá-lo a partir de outro host.

Por exemplo, se o switch possui:

```text
IP: 192.168.10.101
```

No PC, abrimos:

```text
PC
 └── Desktop
      └── Command Prompt
```

E executamos:

```bash
telnet 192.168.10.101
```

Se a configuração estiver correta, o PC tentará estabelecer uma sessão remota com o switch.

O fluxo será:

```text
PC
192.168.10.1
   │
   │ Rede Ethernet
   ▼
Switch
192.168.10.101
```

Agora não precisamos estar fisicamente conectados à porta Console para realizar o acesso.

---

# 13. Console x acesso remoto

É importante entender a diferença entre os dois métodos.

### Console

```text
PC ─── Cabo Console ─── Switch
```

O computador precisa estar fisicamente conectado à porta Console.

É muito utilizado para:

* configuração inicial;
* recuperação de configuração;
* situações em que o acesso pela rede não está disponível.

### Acesso remoto

```text
PC ─── Rede ─── Switch
```

O computador acessa o switch através da rede.

Isso permite administrar o equipamento sem estar fisicamente conectado à porta Console.

---

# 14. Telnet x SSH

Embora o laboratório utilize Telnet para demonstrar o conceito de acesso remoto, em uma rede real **não devemos utilizar Telnet para administração de equipamentos quando SSH estiver disponível**.

### Telnet

O Telnet transmite a sessão sem criptografia adequada para proteger as credenciais e os dados da sessão.

### SSH

O **SSH (Secure Shell)** fornece um canal criptografado para administração remota.

Em um ambiente empresarial, o objetivo normalmente será:

```text
Administrador
      │
      │ SSH
      ▼
   Switch
```

Portanto, depois de compreender o funcionamento do Telnet neste laboratório, o próximo passo importante é aprender a configurar **SSH em equipamentos Cisco**.

---

# 15. Resumo do laboratório

O laboratório pode ser dividido em etapas:

### Etapa 1 — Montar a topologia

```text
PCs ─── Switch ─── Servidor
```

### Etapa 2 — Configurar os IPs

```text
PC1 → 192.168.10.1
PC2 → 192.168.10.2
PC3 → 192.168.10.3
PC4 → 192.168.10.4
```

Máscara:

```text
255.255.255.0
```

### Etapa 3 — Testar conectividade

```bash
ping 192.168.10.2
```

### Etapa 4 — Acessar o switch pelo Console

```text
PC → Desktop → Terminal
```

### Etapa 5 — Entrar nos modos de configuração

```bash
enable
configure terminal
```

### Etapa 6 — Configurar a interface de gerenciamento

```bash
interface vlan 1
ip address 192.168.10.101 255.255.255.0
no shutdown
```

### Etapa 7 — Configurar as linhas VTY

```bash
line vty 0 5
password sua_senha
login
```

### Etapa 8 — Testar o gerenciamento remoto

No PC:

```bash
telnet 192.168.10.101
```

---

# 16. O que você deve aprender com este laboratório?

Mais importante do que decorar os comandos é entender **o que está acontecendo em cada camada**.

```text
                 REDE LAN

        ┌───────────────────────┐
        │       Aplicação       │
        │   Serviços / Usuário  │
        ├───────────────────────┤
        │          IP           │
        │  192.168.10.0 /24     │
        ├───────────────────────┤
        │       Ethernet        │
        │     MAC / Switch      │
        ├───────────────────────┤
        │        Física         │
        │      UTP / Fibra      │
        └───────────────────────┘
```

O objetivo é começar a relacionar:

**cabo → interface → switch → MAC → IP → conectividade → gerenciamento remoto.**

Essa relação é fundamental para evoluir de uma configuração básica no Packet Tracer para a resolução de problemas reais de redes.
