# 🌐 Modelo OSI (Open Systems Interconnection)

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que é?

O **Modelo OSI (Open Systems Interconnection)** é um modelo de referência criado pela **ISO (International Organization for Standardization)** para padronizar a comunicação entre dispositivos em uma rede.

Seu principal objetivo é dividir a comunicação em **7 camadas**, onde cada uma possui uma responsabilidade específica. Dessa forma, torna-se mais fácil desenvolver, compreender e solucionar problemas em redes de computadores.

> **Importante:** O Modelo OSI é um modelo **conceitual**. Na prática, a Internet utiliza principalmente o **Modelo TCP/IP**, mas o OSI continua sendo amplamente utilizado para estudo, documentação e diagnóstico de redes.

---

# 🎯 Objetivos

* Padronizar a comunicação entre diferentes fabricantes.
* Dividir um processo complexo em etapas menores.
* Facilitar o desenvolvimento de tecnologias de rede.
* Auxiliar na identificação e solução de problemas.
* Melhorar a interoperabilidade entre sistemas.

---

# 🧠 Conceitos importantes

* O Modelo OSI possui **7 camadas**.
* Cada camada executa uma função específica.
* Cada camada fornece serviços para a camada superior.
* Os dados descem pelas camadas no dispositivo de origem e sobem pelas camadas no dispositivo de destino.
* Cada camada adiciona informações ao pacote durante o envio (encapsulamento).

---

# 🏢 Analogia do prédio

Imagine um prédio com **7 andares**.

Cada andar representa uma etapa do envio de uma encomenda.

A encomenda só chega ao destinatário porque passa por todos os andares na ordem correta.

Se algum andar falhar, a entrega poderá apresentar problemas ou nem acontecer.

---

# 📚 As 7 Camadas

## Camada 7 — Aplicação (Application)

### Função

É a camada mais próxima do usuário.

Ela permite que programas utilizem os serviços da rede.

### Exemplos

* Navegadores
* Clientes de e-mail
* Aplicativos de mensagens
* FTP

### Protocolos

* HTTP
* HTTPS
* FTP
* SMTP
* POP3
* IMAP
* DNS

### Exemplo

Quando você abre o navegador e acessa um site, a comunicação começa nesta camada.

---

## Camada 6 — Apresentação (Presentation)

### Função

Prepara os dados antes do envio.

Pode:

* Converter formatos
* Comprimir dados
* Criptografar informações
* Descriptografar dados recebidos

### Exemplos

* JPEG
* PNG
* MP3
* SSL/TLS

### Exemplo

Quando você acessa um site HTTPS, a criptografia acontece nesta camada (didaticamente).

---

## Camada 5 — Sessão (Session)

### Função

Controla a comunicação entre dois dispositivos.

Ela:

* Inicia sessões
* Mantém sessões
* Finaliza sessões

### Exemplo

Uma videoconferência permanece aberta graças ao gerenciamento da sessão.

---

## Camada 4 — Transporte (Transport)

### Função

Responsável pela entrega dos dados.

Pode:

* Garantir entrega
* Dividir informações em segmentos
* Reorganizar segmentos
* Controlar erros

### Protocolos

### TCP

* Mais confiável
* Confirma entrega
* Corrige perdas
* Mais lento

Usado em:

* Bancos
* Sites
* E-mails

### UDP

* Mais rápido
* Não confirma entrega
* Não retransmite pacotes perdidos

Usado em:

* Jogos online
* Streaming
* Chamadas de vídeo

---

## Camada 3 — Rede (Network)

### Função

Define o caminho que os dados seguirão.

É responsável pelo roteamento.

### Trabalha com

* Endereço IP
* Roteadores

### Protocolos

* IPv4
* IPv6
* ICMP

### Exemplo

Quando um pacote precisa viajar do Brasil para outro país, esta camada escolhe o caminho mais adequado.

---

## Camada 2 — Enlace de Dados (Data Link)

### Função

Responsável pela comunicação entre dispositivos da mesma rede.

Utiliza:

* Endereço MAC
* Switches

### Protocolos

* Ethernet
* Wi-Fi (IEEE 802.11)

### Exemplo

O switch verifica o endereço MAC para entregar o pacote ao computador correto.

---

## Camada 1 — Física (Physical)

### Função

Transmite os bits pelo meio físico.

Pode utilizar:

* Cabo de rede
* Fibra óptica
* Ondas de rádio

### Equipamentos

* Cabos
* Conectores
* Hubs
* Repetidores

### Exemplo

É nesta camada que os sinais elétricos, ópticos ou de rádio realmente trafegam.

---

# 📦 Encapsulamento dos dados

Durante o envio, os dados passam por todas as camadas.

Cada camada adiciona informações importantes.

Fluxo de envio:

Aplicação

↓

Apresentação

↓

Sessão

↓

Transporte

↓

Rede

↓

Enlace

↓

Física

No destino, acontece o processo inverso.

---

# 💡 Exemplo prático

Você acessa o site da OpenAI.

1. O navegador cria a solicitação (Aplicação).
2. Os dados podem ser criptografados (Apresentação).
3. A sessão é iniciada (Sessão).
4. O TCP organiza os dados (Transporte).
5. O IP define o destino (Rede).
6. O MAC identifica o dispositivo dentro da rede local (Enlace).
7. Os bits percorrem o cabo ou Wi-Fi (Física).

O servidor recebe a solicitação e devolve a resposta pelo caminho inverso.

---

# 🔄 Diferença entre IP e MAC

| Endereço IP                     | Endereço MAC                   |
| ------------------------------- | ------------------------------ |
| Indica onde o dispositivo está. | Indica quem é o dispositivo.   |
| Pode mudar.                     | Normalmente permanece o mesmo. |
| Camada 3.                       | Camada 2.                      |
| Utilizado pelos roteadores.     | Utilizado pelos switches.      |

---

# 🔄 Diferença entre TCP e UDP

| TCP              | UDP                  |
| ---------------- | -------------------- |
| Confiável        | Rápido               |
| Confirma entrega | Não confirma entrega |
| Corrige erros    | Não corrige erros    |
| Mais lento       | Mais rápido          |

---

# 📝 Resumo

O Modelo OSI divide a comunicação de rede em sete camadas independentes.

Cada camada possui uma função específica e trabalha em conjunto com as demais para garantir que os dados sejam enviados e recebidos corretamente.

Embora a Internet utilize o Modelo TCP/IP, o Modelo OSI continua sendo a principal referência para estudos, documentação e solução de problemas em redes.

---

# 🎓 O que preciso lembrar?

* ✅ O Modelo OSI possui 7 camadas.
* ✅ Foi criado pela ISO.
* ✅ É um modelo conceitual.
* ✅ A Internet utiliza principalmente o Modelo TCP/IP.
* ✅ TCP é confiável.
* ✅ UDP é mais rápido.
* ✅ IP identifica o endereço do dispositivo.
* ✅ MAC identifica a placa de rede.
* ✅ Roteadores trabalham com IP.
* ✅ Switches trabalham com MAC.

---

# ❓ Perguntas para revisar

1. O que é o Modelo OSI?
2. Quem criou o Modelo OSI?
3. Qual é o objetivo do Modelo OSI?
4. Quais são as sete camadas?
5. Qual camada utiliza endereços IP?
6. Qual camada utiliza endereços MAC?
7. Qual a diferença entre TCP e UDP?
8. Qual a diferença entre IP e MAC?
9. O que é encapsulamento?
10. Qual modelo é utilizado pela Internet atualmente?

---

# 🔑 Palavras-chave

* Modelo OSI
* ISO
* Redes
* Camadas
* TCP
* UDP
* IPv4
* IPv6
* MAC Address
* Switch
* Roteador
* Encapsulamento
* Comunicação de Rede

---

# 📖 Referências

* ISO/IEC 7498-1 — Open Systems Interconnection (OSI) Reference Model.
* RFC 791 (IPv4).
* RFC 8200 (IPv6).
* RFC 9293 (TCP).
* RFC 768 (UDP).


* **Wireshark** — analisar pacotes de rede.
* **Cisco Packet Tracer** — simular redes.
* **GNS3** — emulação de equipamentos de rede.
* **ping**, **tracert/traceroute**, **ipconfig/ifconfig**, **arp** — comandos úteis para estudar as camadas.


