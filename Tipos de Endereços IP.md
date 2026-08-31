# Tema — Tipos de Endereços IP

## 1. Unicast

**Unicast** é um tipo de comunicação em que **um dispositivo envia dados para um único destino**.

É a forma mais comum de comunicação nas redes.

### Exemplo

```text
Computador A ───────────→ Computador B
       1 origem              1 destino
```

### Características

- Comunicação **um para um**;
- Possui um único destino;
- É utilizado para comunicação entre dispositivos específicos;
- Pode utilizar diferentes tipos de endereços IP, dependendo da localização e finalidade.

> **Importante:** Unicast descreve o **tipo de comunicação**, enquanto categorias como **Global, Link-Local, Loopback e ULA** descrevem diferentes tipos de endereços e seus alcances.

---

## 2. Endereços Link-Local

Um endereço **Link-Local** é utilizado para comunicação dentro do **próprio enlace ou rede local**.

A principal característica é que esses endereços **não são roteáveis para outras redes**.

### IPv6 — Link-Local

No IPv6, os endereços Link-Local pertencem ao bloco:

```text
FE80::/10
```

São utilizados para comunicação no próprio enlace, descoberta de vizinhos e funcionamento de mecanismos do IPv6.

### IPv4 — Link-Local

No IPv4, a faixa utilizada é:

```text
169.254.0.0/16
```

Pode aparecer quando um dispositivo tenta obter automaticamente um endereço IPv4, mas não consegue receber um endereço válido de um servidor DHCP.

---

## 3. Endereços de Loopback

O endereço **Loopback** permite que um dispositivo se comunique **com ele mesmo**.

É utilizado principalmente para testes de conectividade, testes de aplicações, desenvolvimento e verificação da própria pilha de rede.

### IPv4

```text
127.0.0.0/8
```

O endereço mais conhecido é:

```text
127.0.0.1
```

### IPv6

```text
::1
```

Portanto:

```text
IPv4 → 127.0.0.1
IPv6 → ::1
```

---

## 4. Endereços Globais

Um **endereço global** identifica uma interface que pode participar de comunicações entre diferentes redes.

### IPv6 — Global Unicast

Os endereços IPv6 Global Unicast pertencem ao bloco:

```text
2000::/3
```

Esse espaço é destinado a endereços globalmente roteáveis.

> **Atenção:** `2001:db8::/32` é reservado para **documentação**, portanto não representa um endereço global real da Internet.

### IPv4 — Endereços públicos

No IPv4, não existe uma única faixa que represente todos os endereços públicos.

Um IPv4 público é, de forma geral, um endereço que pode ser **roteado globalmente na Internet** e que não pertence a uma faixa reservada para outra finalidade.

Exemplo:

```text
8.8.8.8
```

---

## 5. Endereços Privados no IPv4

As principais faixas IPv4 privadas são:

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

São muito utilizadas em redes domésticas, empresas, escolas, laboratórios e outras redes internas.

Esses endereços **não são roteados diretamente pela Internet pública**.

Para que dispositivos com endereços privados acessem a Internet, é comum utilizar **NAT (Network Address Translation)**.

### Exemplo

```text
Computador
192.168.1.10
      │
      ↓
   Roteador
      │
      ↓
Endereço público
      │
      ↓
  Internet
```

---

## 6. ULA — Unique Local Address

No IPv6 existe uma categoria destinada à utilização local chamada:

> **ULA — Unique Local Address**

O bloco reservado para ULA é:

```text
FC00::/7
```

Na prática, os endereços ULA normalmente utilizam:

```text
FD00::/8
```

São destinados a redes privadas ou locais, como redes corporativas, domésticas e laboratórios.

Podem ser roteados dentro da organização, mas não devem ser roteados globalmente na Internet.

---

## 7. IPv4 Privado x IPv6 ULA

| IPv4 | IPv6 |
|---|---|
| `10.0.0.0/8` | ULA |
| `172.16.0.0/12` | ULA |
| `192.168.0.0/16` | ULA |
| Uso em redes privadas | Uso em redes locais/privadas |
| Não roteável diretamente na Internet | Não roteável globalmente na Internet |

---

## 8. CGNAT

A faixa IPv4:

```text
100.64.0.0/10
```

é reservada para **Shared Address Space**, sendo utilizada principalmente em cenários de **CGNAT (Carrier-Grade NAT)**.

O CGNAT permite que vários clientes de um provedor compartilhem endereços IPv4 públicos.

```text
Cliente A ─┐
Cliente B ─┼──→ CGNAT do ISP ──→ IPv4 público ──→ Internet
Cliente C ─┘
```

> **Importante:** `100.64.0.0/10` não é uma faixa IPv4 privada tradicional como `192.168.0.0/16`.

---

## 9. Endereços para Documentação

Existem faixas reservadas para exemplos, aulas, tutoriais, documentação e laboratórios.

### IPv4

```text
192.0.2.0/24
198.51.100.0/24
203.0.113.0/24
```

### IPv6

```text
2001:db8::/32
```

Esses endereços devem ser utilizados como exemplos, e não como endereços reais para comunicação na Internet.

---

## 10. Comparação dos principais tipos

| Tipo | IPv4 | IPv6 | Alcance / finalidade |
|---|---|---|---|
| **Loopback** | `127.0.0.0/8` | `::1` | Próprio dispositivo |
| **Link-Local** | `169.254.0.0/16` | `FE80::/10` | Rede/enlace local |
| **Privado / ULA** | `10/8`, `172.16/12`, `192.168/16` | `FC00::/7` | Rede privada/local |
| **Global** | Endereços públicos | `2000::/3` | Comunicação entre redes / Internet |
| **CGNAT** | `100.64.0.0/10` | — | Compartilhamento de IPv4 pelo ISP |
| **Documentação** | `192.0.2/24`, `198.51.100/24`, `203.0.113/24` | `2001:db8::/32` | Exemplos e documentação |

---

## 11. Como memorizar

Uma forma simples de entender esses endereços é pensar no **alcance da comunicação**:

```text
                         ENDEREÇOS IP
                              │
             ┌────────────────┼────────────────┐
             │                │                │
          Próprio           Local            Global
         dispositivo        enlace          Internet
             │                │                │
         Loopback         Link-Local        Global
             │
        127.0.0.1
           ::1
```

Também existem endereços destinados a finalidades específicas:

```text
Privados / ULA
      ↓
Comunicação interna

CGNAT
      ↓
Compartilhamento de IPv4
pelo provedor

Documentação
      ↓
Exemplos, aulas e laboratórios
```

---

# 12. Resumo geral

## 🔵 Unicast

**Um dispositivo → um dispositivo**

É um tipo de comunicação **um para um**.

## 🟢 Link-Local

**Comunicação no próprio enlace/rede local.**

- IPv4: `169.254.0.0/16`
- IPv6: `FE80::/10`

Não é roteável para outras redes.

## 🔄 Loopback

**Dispositivo → ele mesmo**

- IPv4: `127.0.0.1`
- IPv6: `::1`

É utilizado principalmente para testes e comunicação dentro do próprio dispositivo.

## 🌎 Global

Endereços utilizados para comunicação entre diferentes redes e, no caso dos endereços globalmente roteáveis, através da Internet.

- IPv4: endereços públicos globalmente roteáveis;
- IPv6: `2000::/3`.

## 🏠 Privado / ULA

Utilizados principalmente para comunicação dentro de redes privadas.

### IPv4

```text
10.0.0.0/8
172.16.0.0/12
192.168.0.0/16
```

### IPv6

```text
FC00::/7
```

Na prática, ULA normalmente utiliza endereços dentro de:

```text
FD00::/8
```

## 🔄 CGNAT

Utilizado pelos provedores para compartilhar endereços IPv4 públicos entre vários clientes.

```text
100.64.0.0/10
```

## 📝 Documentação

Utilizados para exemplos, aulas e documentação.

### IPv4

```text
192.0.2.0/24
198.51.100.0/24
203.0.113.0/24
```

### IPv6

```text
2001:db8::/32
```

> **Ideia principal:** não basta saber apenas "qual é o IP". É importante entender **qual é o tipo daquele endereço e qual é o alcance ou finalidade dele**. Isso permite determinar se ele pode ser utilizado apenas no próprio dispositivo, dentro do enlace local, dentro de uma rede privada, em uma comunicação entre redes ou globalmente na Internet.
