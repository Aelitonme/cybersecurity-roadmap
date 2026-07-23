# 🚪 Portas de Rede (Network Ports)

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que são portas de rede?

As **portas de rede** são números lógicos utilizados para identificar **qual serviço ou aplicação** deve receber os dados enviados pela rede.

Enquanto o **endereço IP** identifica **o dispositivo**, a **porta** identifica **o serviço** que está sendo executado nesse dispositivo.

Imagine um prédio:

* O **endereço IP** é o endereço do prédio.
* A **porta** é o número do apartamento.

Assim, os dados chegam ao computador correto (IP) e são entregues ao serviço correto (porta).

---

# 🎯 Objetivos

* Identificar serviços em um dispositivo.
* Permitir que vários serviços funcionem ao mesmo tempo.
* Direcionar corretamente o tráfego de rede.
* Facilitar a comunicação entre clientes e servidores.

---

# 🧠 Conceitos importantes

* As portas variam de **0 a 65535**.
* Cada porta pode estar associada a um serviço específico.
* TCP e UDP possuem suas próprias portas.
* Um mesmo computador pode utilizar diversas portas simultaneamente.

---

# 📚 Como funciona?

Quando um cliente deseja acessar um serviço:

1. Descobre o endereço IP do servidor.
2. Inicia uma conexão com uma porta específica.
3. O sistema operacional verifica qual aplicação está "escutando" aquela porta.
4. Os dados são entregues ao serviço correto.

---

# 📂 Faixas de portas

## Portas Bem Conhecidas (Well-Known Ports)

**0 – 1023**

Reservadas para protocolos e serviços padrão.

Exemplos:

* HTTP
* HTTPS
* SSH
* FTP
* DNS

---

## Portas Registradas (Registered Ports)

**1024 – 49151**

Utilizadas por aplicações e serviços registrados.

Exemplo:

* Banco de dados
* Aplicações corporativas

---

## Portas Dinâmicas ou Privadas

**49152 – 65535**

Utilizadas temporariamente pelo sistema operacional durante conexões.

Também são chamadas de **portas efêmeras (ephemeral ports)**.

---

# 🌐 Portas mais utilizadas

| Porta | Protocolo | Serviço                       |
| ----: | --------- | ----------------------------- |
|    20 | TCP       | FTP (Dados)                   |
|    21 | TCP       | FTP (Controle)                |
|    22 | TCP       | SSH                           |
|    23 | TCP       | Telnet                        |
|    25 | TCP       | SMTP                          |
|    53 | TCP/UDP   | DNS                           |
|    67 | UDP       | DHCP (Servidor)               |
|    68 | UDP       | DHCP (Cliente)                |
|    80 | TCP       | HTTP                          |
|   110 | TCP       | POP3                          |
|   143 | TCP       | IMAP                          |
|   443 | TCP       | HTTPS                         |
|  3306 | TCP       | MySQL                         |
|  3389 | TCP       | RDP (Área de Trabalho Remota) |

---

# ⚙️ Exemplo prático

Imagine que você acessa:

```text id="l3kh8v"
https://www.exemplo.com
```

O navegador:

1. Descobre o endereço IP do servidor.
2. Estabelece uma conexão TCP.
3. Utiliza a **porta 443**, pois o serviço é HTTPS.
4. O servidor responde utilizando essa mesma conexão.

---

# 🔄 Relação entre IP e Porta

| Endereço IP                              | Porta                                                  |
| ---------------------------------------- | ------------------------------------------------------ |
| Identifica o dispositivo.                | Identifica o serviço.                                  |
| Exemplo: 192.168.1.10                    | Exemplo: 443                                           |
| Trabalha na camada de Internet (TCP/IP). | Trabalha junto aos protocolos de transporte (TCP/UDP). |

---

# 🛡️ Segurança das portas

Portas abertas podem representar riscos quando um serviço está vulnerável ou mal configurado.

Por isso, administradores utilizam ferramentas como **firewalls** para permitir apenas as conexões necessárias.

Também é comum monitorar quais portas estão abertas para reduzir a superfície de ataque.

---

# 💡 Exemplo do dia a dia

Você acessa um site seguro.

O computador encontra o endereço IP do servidor e se conecta à **porta 443**.

Se você acessasse um servidor remoto via SSH, utilizaria a **porta 22**.

Cada serviço possui sua própria porta padrão, facilitando a comunicação entre clientes e servidores.

---

# 📝 Resumo

As portas de rede identificam os serviços que estão disponíveis em um dispositivo.

Enquanto o endereço IP informa **qual computador** deve receber os dados, a porta informa **qual aplicação** deve processá-los.

Elas são essenciais para que diversos serviços funcionem simultaneamente em um mesmo equipamento.

---

# 🎓 O que preciso lembrar?

* ✅ Portas identificam serviços.
* ✅ O intervalo de portas vai de **0 a 65535**.
* ✅ HTTP utiliza a porta **80**.
* ✅ HTTPS utiliza a porta **443**.
* ✅ SSH utiliza a porta **22**.
* ✅ DNS utiliza a porta **53**.
* ✅ IP identifica o dispositivo; porta identifica o serviço.

---

# ❓ Perguntas para revisar

1. O que é uma porta de rede?
2. Qual a diferença entre endereço IP e porta?
3. Qual é a função de uma porta?
4. Qual porta é utilizada pelo HTTP?
5. Qual porta é utilizada pelo HTTPS?
6. Qual porta é utilizada pelo SSH?
7. Qual porta é utilizada pelo DNS?
8. O que são portas bem conhecidas?
9. O que são portas dinâmicas?
10. Por que portas abertas podem representar um risco?

---

# 🔑 Palavras-chave

* Porta
* TCP
* UDP
* HTTP
* HTTPS
* SSH
* DNS
* FTP
* Firewall
* Serviço
* Socket

---

# 🛠️ Ferramentas relacionadas

* **netstat** — lista conexões e portas em uso.
* **ss** (Linux) — mostra sockets e portas abertas.
* **lsof** (Linux/macOS) — identifica processos usando portas.
* **Nmap** — verifica portas abertas em um dispositivo.
* **Wireshark** — analisa o tráfego entre portas.
* **telnet** ou **nc (netcat)** — testa conectividade com portas específicas.

---

# 📖 Referências

* RFC 6335 – Internet Assigned Numbers Authority (IANA): Port Number Registry.
* Documentação da IANA sobre portas de serviço.
* RFC 9293 – Transmission Control Protocol (TCP).
* RFC 768 – User Datagram Protocol (UDP).
