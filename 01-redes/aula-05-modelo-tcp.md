# 🌐 Modelo TCP/IP

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que é?

O **Modelo TCP/IP (Transmission Control Protocol / Internet Protocol)** é o modelo utilizado na prática para a comunicação na Internet e em redes modernas.

Ele define como os dados devem ser organizados, enviados, roteados e recebidos entre dispositivos conectados à rede.

Diferente do Modelo OSI, que possui **7 camadas**, o Modelo TCP/IP agrupa funções semelhantes em **4 camadas**, tornando sua implementação mais simples e prática.

---

# 🎯 Objetivos

* Permitir a comunicação entre dispositivos em redes.
* Padronizar a transmissão de dados na Internet.
* Garantir que os dados cheguem ao destino correto.
* Facilitar a interoperabilidade entre diferentes sistemas.

---

# 🧠 Conceitos importantes

* É o modelo utilizado pela Internet.
* Possui **4 camadas**.
* Agrupa algumas funções que, no Modelo OSI, estão separadas.
* Foi desenvolvido antes do Modelo OSI e continua sendo a base da Internet moderna.

---

# 📚 As 4 Camadas do Modelo TCP/IP

## 1️⃣ Aplicação (Application)

### Função

É a camada responsável pela comunicação entre os programas e a rede.

Ela reúne as funções das camadas **Aplicação, Apresentação e Sessão** do Modelo OSI.

### Exemplos de protocolos

* HTTP
* HTTPS
* FTP
* SMTP
* POP3
* IMAP
* DNS
* SSH

### Exemplo

Quando você acessa um site pelo navegador, a comunicação começa nesta camada.

---

## 2️⃣ Transporte (Transport)

### Função

Responsável por transportar os dados entre origem e destino.

Ela controla:

* Segmentação dos dados.
* Controle de erros.
* Controle de fluxo.
* Confiabilidade da comunicação.

### Principais protocolos

### TCP (Transmission Control Protocol)

Características:

* Confiável.
* Confirma o recebimento dos dados.
* Retransmite pacotes perdidos.
* Mantém a ordem correta dos dados.

Utilizado em:

* Sites.
* Bancos.
* E-mails.
* Transferência de arquivos.

---

### UDP (User Datagram Protocol)

Características:

* Mais rápido.
* Não confirma a entrega.
* Não retransmite pacotes.
* Menor atraso na comunicação.

Utilizado em:

* Jogos online.
* Streaming.
* Chamadas de voz e vídeo.
* DNS.

---

## 3️⃣ Internet (Internet Layer)

### Função

É responsável pelo endereçamento lógico e pelo roteamento dos pacotes entre diferentes redes.

Ela determina qual caminho os dados devem seguir até o destino.

### Protocolos

* IPv4
* IPv6
* ICMP
* ARP*

> **Observação:** Em muitas referências didáticas o ARP é apresentado junto à camada de Internet por sua relação com endereços IP. Em outras classificações, ele é tratado como um protocolo entre as camadas de Internet e Acesso à Rede.

### Equipamentos

* Roteadores

### Exemplo

Quando um pacote sai da sua casa para um servidor em outro país, os roteadores utilizam o endereço IP para encaminhá-lo até o destino.

---

## 4️⃣ Acesso à Rede (Network Access ou Link)

### Função

Responsável pela transmissão física dos dados na rede local.

Ela reúne as funções das camadas **Enlace** e **Física** do Modelo OSI.

### Trabalha com

* Endereço MAC.
* Cabos.
* Fibra óptica.
* Wi-Fi.
* Switches.
* Placas de rede.

### Tecnologias

* Ethernet
* Wi-Fi (IEEE 802.11)

### Exemplo

Quando seu computador envia dados para o roteador através do cabo de rede ou do Wi-Fi, essa comunicação ocorre nesta camada.

---

# 🔄 Comparação entre OSI e TCP/IP

| Modelo OSI   | Modelo TCP/IP |
| ------------ | ------------- |
| Aplicação    | Aplicação     |
| Apresentação | Aplicação     |
| Sessão       | Aplicação     |
| Transporte   | Transporte    |
| Rede         | Internet      |
| Enlace       | Acesso à Rede |
| Física       | Acesso à Rede |

---

# 📦 Fluxo dos dados

Durante o envio, os dados passam pelas quatro camadas.

**Origem**

Aplicação

↓

Transporte

↓

Internet

↓

Acesso à Rede

↓

Meio físico (cabo, fibra ou Wi-Fi)

No dispositivo de destino, o processo acontece na ordem inversa.

---

# 💡 Exemplo prático

Imagine que você deseja acessar um site.

1. O navegador cria a solicitação (**Aplicação**).
2. O protocolo TCP organiza os dados (**Transporte**).
3. O IP identifica o servidor e define a rota (**Internet**).
4. Os dados são enviados pela placa de rede utilizando cabo ou Wi-Fi (**Acesso à Rede**).
5. O servidor recebe a solicitação e envia a resposta seguindo o caminho inverso.

---

# ⚖️ Modelo OSI × Modelo TCP/IP

| Modelo OSI                             | Modelo TCP/IP                    |
| -------------------------------------- | -------------------------------- |
| Utilizado principalmente para estudos. | Utilizado na prática.            |
| Possui 7 camadas.                      | Possui 4 camadas.                |
| Modelo de referência.                  | Modelo implementado na Internet. |
| Divide as funções em mais etapas.      | Agrupa funções semelhantes.      |

---

# 📝 Resumo

O Modelo TCP/IP é o padrão utilizado para a comunicação na Internet.

Ele organiza a comunicação em quatro camadas:

1. Aplicação.
2. Transporte.
3. Internet.
4. Acesso à Rede.

Seu objetivo é permitir que dispositivos diferentes consigam trocar informações de forma padronizada e eficiente.

---

# 🎓 O que preciso lembrar?

* ✅ O Modelo TCP/IP possui **4 camadas**.
* ✅ É o modelo utilizado na Internet.
* ✅ A camada de Aplicação reúne três camadas do Modelo OSI.
* ✅ TCP oferece confiabilidade.
* ✅ UDP oferece velocidade.
* ✅ A camada Internet utiliza endereços IP.
* ✅ A camada Acesso à Rede utiliza endereços MAC e realiza a transmissão física.

---

# ❓ Perguntas para revisar

1. O que é o Modelo TCP/IP?
2. Quantas camadas ele possui?
3. Qual é a função da camada de Aplicação?
4. Qual a diferença entre TCP e UDP?
5. Qual camada utiliza o endereço IP?
6. Qual camada utiliza o endereço MAC?
7. Qual a principal diferença entre o Modelo OSI e o Modelo TCP/IP?
8. Qual modelo é utilizado na Internet atualmente?

---

# 🔑 Palavras-chave

* TCP/IP
* Internet
* TCP
* UDP
* IPv4
* IPv6
* Endereço IP
* Endereço MAC
* Roteamento
* Aplicação
* Transporte
* Acesso à Rede

---

# 📖 Referências

* RFC 1122 – Requirements for Internet Hosts.
* RFC 791 – Internet Protocol (IPv4).
* RFC 8200 – Internet Protocol Version 6 (IPv6).
* RFC 9293 – Transmission Control Protocol (TCP).
* RFC 768 – User Datagram Protocol (UDP).
