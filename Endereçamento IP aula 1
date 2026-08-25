# Tema — Endereçamento IP

## 1. O que é o endereçamento IP?

O **endereçamento IP** é utilizado para identificar dispositivos dentro de uma rede e permitir que eles sejam localizados e alcançados durante uma comunicação.

Um endereço IP permite:

* Identificar uma interface de rede;
* Determinar a qual rede o dispositivo pertence;
* Localizar a rede de destino;
* Encaminhar pacotes de dados até a rede correta e, posteriormente, até o dispositivo correto.

Além disso, o endereçamento permite organizar os dispositivos de acordo com diferentes redes, sub-redes e funções.

---

# 2. IPv4 e IPv6

Atualmente existem duas versões principais do **Internet Protocol (IP)**:

* **IPv4 (Internet Protocol version 4)** — versão mais antiga e ainda amplamente utilizada;
* **IPv6 (Internet Protocol version 6)** — versão mais recente, criada principalmente para solucionar a limitação de endereços do IPv4.

---

# 3. IPv4

O IPv4 utiliza **32 bits** para representar um endereço.

Como cada bit pode assumir dois valores (`0` ou `1`), temos:

```text
2³² = 4.294.967.296
```

Portanto, o IPv4 possui aproximadamente **4,3 bilhões de combinações de endereços**.

> **Importante:** esse número representa a quantidade total de combinações possíveis no espaço de endereçamento IPv4. Na prática, nem todos esses endereços podem ser atribuídos diretamente a dispositivos na Internet.

---

# 4. Representação do IPv4

Os computadores trabalham naturalmente com dados binários, utilizando `0` e `1`.

Um endereço IPv4 poderia ser representado diretamente pelos seus 32 bits:

```text
11000000101010000000000100000001
```

Porém, essa representação seria pouco prática para os seres humanos.

Por isso, os 32 bits são divididos em **quatro grupos de 8 bits**, chamados de **octetos**.

```text
11000000 . 10101000 . 00000001 . 00000001
```

Cada octeto é convertido de binário para decimal:

```text
192 . 168 . 1 . 1
```

Assim, o IPv4 é normalmente representado no formato:

```text
192.168.1.1
```

### Faixa de cada octeto

Como cada octeto possui 8 bits, ele pode representar valores de:

```text
0 até 255
```

Isso ocorre porque:

```text
2⁸ = 256 valores
```

Contando de `0` até `255`, temos exatamente 256 possibilidades.

---

# 5. IPv6

O IPv6 foi desenvolvido principalmente para resolver a limitação do espaço de endereçamento do IPv4.

Enquanto o IPv4 utiliza **32 bits**, o IPv6 utiliza **128 bits**.

Portanto:

```text
2¹²⁸
```

possibilidades de endereços podem ser representadas.

Esse número é aproximadamente:

**340 undecilhões de endereços.**

Com isso, o IPv6 possui um espaço de endereçamento extremamente maior que o IPv4.

> No IPv6, a preocupação principal deixa de ser a escassez de endereços individuais. O grande espaço disponível permite trabalhar com uma quantidade enorme de redes e sub-redes.

---

# 6. Representação do IPv6

Representar 128 bits em binário também seria pouco prático.

Por isso, o IPv6 utiliza a representação **hexadecimal**.

Os 128 bits são divididos em **8 grupos de 16 bits**.

Cada grupo de 16 bits é chamado de **hexteto**.

Um endereço IPv6 pode ser representado assim:

```text
2001:0db8:0000:0000:0000:ff00:0042:8329
```

Os grupos são separados por `:`.

---

# 7. Sistema hexadecimal

O sistema hexadecimal utiliza 16 símbolos:

```text
0 1 2 3 4 5 6 7 8 9 A B C D E F
```

Os valores de `0` a `9` possuem seus valores tradicionais.

As letras representam:

```text
A = 10
B = 11
C = 12
D = 13
E = 14
F = 15
```

Cada dígito hexadecimal representa exatamente **4 bits**.

Por isso:

```text
4 bits × 4 dígitos = 16 bits
```

Assim, cada hexteto IPv6 possui 16 bits.

As letras podem ser escritas em maiúsculas ou minúsculas:

```text
ABCD
```

e

```text
abcd
```

representam o mesmo valor.

---

# 8. Abreviação de endereços IPv6

Os endereços IPv6 podem ser escritos de forma abreviada para facilitar a leitura.

Existem duas regras importantes.

## 8.1 Remover zeros à esquerda

Zeros à esquerda de cada grupo podem ser removidos.

Por exemplo:

```text
2001:0db8:0000:0042:0000:0000:0000:0001
```

pode ser escrito como:

```text
2001:db8:0:42:0:0:0:1
```

---

## 8.2 Substituir grupos consecutivos de zeros por `::`

Uma sequência contínua de grupos `0000` pode ser substituída por:

```text
::
```

Exemplo:

```text
2001:db8:0:0:0:0:0:1
```

pode ser abreviado para:

```text
2001:db8::1
```

### Regra importante

A abreviação `::` pode aparecer **uma única vez em um endereço IPv6**.

Isso ocorre porque, se fosse utilizada mais de uma vez, não seria possível determinar quantos grupos de zeros existiam em cada posição.

---

# 9. Endereço IP como identificador e localização

O endereço IP possui duas funções importantes:

1. **Identificar** uma interface dentro de uma rede;
2. **Indicar a localização lógica** dessa interface dentro da estrutura de redes.

Isso permite que os equipamentos de rede saibam para onde os pacotes devem ser encaminhados.

Para entender isso, precisamos dividir o endereço IP em duas partes principais:

```text
Prefixo de rede + Identificador de interface
```

---

# 10. Prefixo de rede

O **prefixo de rede** identifica a rede à qual o dispositivo pertence.

Podemos imaginar o prefixo como uma identificação que representa todos os endereços pertencentes àquela rede.

Os protocolos de roteamento utilizam essa informação para determinar **para qual rede um pacote deve ser encaminhado**.

Por exemplo:

```text
192.168.1.0/24
```

Nesse caso:

```text
192.168.1.0
```

representa a rede.

O `/24` indica que os primeiros **24 bits** pertencem ao prefixo de rede.

---

# 11. Identificador de interface

A parte restante do endereço identifica a interface de rede dentro daquela rede.

De forma simplificada:

```text
Prefixo de rede | Identificador de interface
```

O prefixo informa:

> "Qual é a rede?"

O identificador de interface informa:

> "Qual dispositivo/interface dentro dessa rede?"

Essa divisão permite que o encaminhamento aconteça em etapas:

```text
Origem
   ↓
Rede de destino
   ↓
Dispositivo/interface de destino
```

---

# 12. Prefixo no IPv4

No IPv4, a quantidade de bits utilizada para representar a rede pode variar.

Por exemplo:

```text
192.168.1.0/24
```

significa que:

* 24 bits representam a rede;
* os 8 bits restantes representam a parte destinada aos dispositivos daquela rede.

Outro exemplo:

```text
192.168.1.0/26
```

Nesse caso:

* 26 bits representam a rede;
* 6 bits ficam para a parte destinada às interfaces.

Portanto, diferentemente do IPv6, o IPv4 possui diferentes tamanhos de prefixo dependendo da rede.

---

# 13. Notação CIDR

A representação:

```text
192.168.1.0/24
```

é chamada de **notação de prefixo** ou **CIDR (Classless Inter-Domain Routing)**.

O número depois da barra indica quantos bits pertencem ao prefixo.

Exemplos:

```text
/8
/16
/24
/26
/30
```

Quanto maior o número depois da barra, maior é a quantidade de bits utilizada para representar o prefixo.

---

# 14. Máscara de sub-rede no IPv4

No IPv4, o prefixo também pode ser representado utilizando uma **máscara de sub-rede**.

Por exemplo:

```text
192.168.1.0/24
```

corresponde à máscara:

```text
255.255.255.0
```

Em binário:

```text
11111111.11111111.11111111.00000000
```

Os bits `1` representam a parte da rede.

Os bits `0` representam a parte destinada às interfaces.

```text
11111111.11111111.11111111.00000000
^^^^^^^^^^^^^^^^^^^^^^^^
       Rede

                         ^^^^^^^^
                         Interface
```

---

# 15. Como descobrir o prefixo de uma rede

Podemos utilizar uma operação lógica **AND bit a bit** entre:

```text
Endereço IP
        AND
Máscara de sub-rede
        =
Endereço da rede
```

Por exemplo:

```text
IP:       192.168.1.25
Máscara:  255.255.255.0
```

Resultado:

```text
Rede:     192.168.1.0
```

Portanto:

```text
192.168.1.25/24
```

pertence à rede:

```text
192.168.1.0/24
```

---

# 16. Prefixos no IPv6

No IPv6, é muito comum utilizar:

```text
/64
```

para redes de uso geral.

Nesse caso:

```text
64 bits → Prefixo de rede
64 bits → Identificador de interface
```

Representação simplificada:

```text
|-------- 64 bits --------|-------- 64 bits --------|
|     Prefixo de rede     | Identificador de interface |
```

Por exemplo:

```text
2001:db8:1234:5678::/64
```

Nesse caso, os primeiros 64 bits representam o prefixo da rede.

---

# 17. Prefixos IPv6 diferentes de /64

Embora `/64` seja o tamanho tradicional para muitas redes IPv6, existem outros tamanhos de prefixo.

Redes maiores podem utilizar prefixos menores, por exemplo:

```text
/48
/56
/60
```

Além disso, existem situações específicas em que podem ser utilizados prefixos maiores que `/64`.

Um exemplo são determinados enlaces ponto a ponto, nos quais podem aparecer prefixos como:

```text
/127
```

ou outros tamanhos apropriados ao cenário.

Portanto, não devemos interpretar `/64` como uma regra absoluta para todos os tipos de redes IPv6.

---

# 18. IPv4 x IPv6

| Característica          | IPv4            | IPv6                                     |
| ----------------------- | --------------- | ---------------------------------------- |
| Tamanho                 | 32 bits         | 128 bits                                 |
| Representação comum     | Decimal         | Hexadecimal                              |
| Divisão visual          | 4 octetos       | 8 hextetos                               |
| Separador               | `.`             | `:`                                      |
| Exemplo                 | `192.168.1.1`   | `2001:db8::1`                            |
| Espaço de endereçamento | ~4,3 bilhões    | ~3,4 × 10³⁸                              |
| Prefixos                | Variáveis       | `/64` é comum                            |
| Máscara decimal         | Muito utilizada | Não utilizada da mesma forma que no IPv4 |

---

# 19. Resumo visual

```text
                    ENDEREÇAMENTO IP
                           │
             ┌─────────────┴─────────────┐
             │                           │
           IPv4                         IPv6
             │                           │
          32 bits                     128 bits
             │                           │
      Decimal com pontos         Hexadecimal com :
             │                           │
      4 octetos                    8 hextetos
             │                           │
      Prefixo + interface          Prefixo + interface
             │                           │
       Ex.: /24                      Ex.: /64
```

---

# 20. Conceito fundamental

O ponto mais importante é entender que um endereço IP não serve apenas para "dar um número" a um dispositivo.

Ele permite estruturar a comunicação em redes.

De forma simplificada:

```text
Endereço IP
     │
     ├── Prefixo de rede
     │       ↓
     │   Identifica a rede
     │
     └── Identificador de interface
             ↓
       Identifica a interface
       dentro daquela rede
```

Quando um dispositivo envia um pacote, os equipamentos de rede utilizam principalmente o **prefixo de destino** para determinar para qual rede o pacote deve ser encaminhado.

Depois, dentro da rede de destino, o tráfego pode ser entregue à interface correspondente.

> **Ideia principal:** o endereçamento IP fornece uma forma hierárquica de identificar e localizar interfaces dentro de redes, permitindo que os roteadores determinem para onde os pacotes devem ser encaminhados.
