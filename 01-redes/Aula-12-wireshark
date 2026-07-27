🦈 Wireshark

«Categoria: Redes de Computadores
Nível: Básico
Status: 📖 Revisão»

---

📌 O que é?

O Wireshark é um analisador de protocolos de rede (Network Protocol Analyzer) utilizado para capturar, visualizar e analisar o tráfego que passa por uma interface de rede.

Ele é uma das ferramentas mais utilizadas por profissionais de Redes, Cybersecurity, Suporte, Forense Digital e Pentest para entender como os dispositivos se comunicam e identificar possíveis problemas ou comportamentos suspeitos.

---

🎯 Objetivos

- Capturar pacotes de rede.
- Analisar protocolos de comunicação.
- Identificar falhas de conexão.
- Auxiliar na solução de problemas de rede.
- Investigar incidentes de segurança.

---

🧠 Conceitos importantes

- O Wireshark captura pacotes de rede.
- Cada pacote contém diversas informações, como endereços IP, endereços MAC, portas e protocolos.
- A ferramenta apenas observa o tráfego, sem modificá-lo.
- É possível aplicar filtros para visualizar apenas os pacotes desejados.

---

📚 Como funciona?

Quando a captura é iniciada:

1. O Wireshark monitora uma interface de rede (Ethernet, Wi-Fi etc.).
2. Os pacotes que passam por essa interface são capturados.
3. Cada pacote é organizado e exibido na tela.
4. O usuário pode analisar protocolos, endereços, portas e outros detalhes.

---

⚙️ Estrutura da interface

A interface do Wireshark é dividida em três partes principais:

1. Lista de Pacotes

Mostra todos os pacotes capturados em ordem cronológica.

Exibe informações como:

- Número do pacote.
- Horário.
- Endereço IP de origem.
- Endereço IP de destino.
- Protocolo.
- Tamanho.
- Resumo da comunicação.

---

2. Detalhes do Pacote

Exibe informações detalhadas sobre o pacote selecionado.

É possível visualizar:

- Cabeçalho Ethernet.
- Endereço MAC.
- Cabeçalho IP.
- TCP ou UDP.
- HTTP.
- DNS.
- TLS.
- Entre outros protocolos.

---

3. Dados em Hexadecimal

Mostra os dados do pacote em formato hexadecimal e ASCII.

Essa visualização é útil para análises mais avançadas.

---

🔍 Principais protocolos encontrados

Durante uma captura é comum encontrar:

- ARP
- DNS
- ICMP
- TCP
- UDP
- HTTP
- HTTPS (TLS)
- DHCP

---

🎯 Filtros mais utilizados

Os filtros ajudam a localizar rapidamente pacotes específicos.

HTTP

http

Mostra apenas tráfego HTTP.

---

DNS

dns

Mostra consultas e respostas DNS.

---

TCP

tcp

Mostra somente pacotes TCP.

---

UDP

udp

Mostra somente pacotes UDP.

---

ICMP

icmp

Mostra mensagens ICMP, como as utilizadas pelo comando ping.

---

HTTPS (TLS)

tls

Mostra o tráfego relacionado ao protocolo TLS.

---

Endereço IP específico

ip.addr == 192.168.1.10

Exibe apenas os pacotes enviados ou recebidos por esse endereço IP.

---

Porta específica

tcp.port == 443

Mostra apenas o tráfego TCP da porta 443 (HTTPS).

---

💡 Exemplo prático

Imagine que um usuário informa que não consegue acessar um site.

Durante a análise no Wireshark, você observa:

1. Uma consulta DNS para descobrir o endereço IP.
2. O servidor DNS responde com o IP correto.
3. O cliente inicia o TCP Three-Way Handshake.
4. O cliente e o servidor realizam o Handshake TLS.
5. O navegador envia uma requisição HTTP sobre HTTPS.
6. O servidor responde com a página solicitada.

Analisando essas etapas, é possível identificar em qual momento ocorreu uma falha.

---

🛡️ Aplicações em Cybersecurity

O Wireshark pode ser utilizado para:

- Identificar tráfego suspeito.
- Investigar incidentes de segurança.
- Detectar tentativas de comunicação incomuns.
- Analisar ataques de rede.
- Estudar protocolos.
- Validar configurações de rede.

Importante: utilize o Wireshark apenas em redes para as quais você possui autorização. Capturar tráfego de redes de terceiros sem permissão pode violar políticas ou leis.

---

📝 Resumo

O Wireshark é uma ferramenta utilizada para capturar e analisar pacotes de rede.

Ele permite visualizar detalhadamente como os dispositivos se comunicam, identificar falhas, compreender protocolos e auxiliar na investigação de incidentes de segurança.

É considerado uma das ferramentas fundamentais para profissionais de Redes e Cybersecurity.

---

🎓 O que preciso lembrar?

- ✅ O Wireshark captura pacotes de rede.
- ✅ Permite analisar diversos protocolos.
- ✅ Utiliza filtros para facilitar a análise.
- ✅ Exibe informações como IP, MAC, portas e protocolos.
- ✅ É amplamente utilizado em redes e cybersecurity.
- ✅ Deve ser utilizado apenas em ambientes autorizados.

---

❓ Perguntas para revisar

1. O que é o Wireshark?
2. Para que ele é utilizado?
3. O que é um pacote de rede?
4. Quais informações podem ser visualizadas em um pacote?
5. Como visualizar apenas consultas DNS?
6. Como filtrar tráfego HTTP?
7. Como visualizar apenas conexões na porta 443?
8. Em quais áreas da tecnologia o Wireshark é utilizado?

---

🔑 Palavras-chave

- Wireshark
- Captura de Pacotes
- Packet Analyzer
- TCP
- UDP
- HTTP
- HTTPS
- TLS
- DNS
- ARP
- ICMP
- Ethernet
- Análise de Rede

---

🛠️ Ferramentas relacionadas

- tcpdump — captura de pacotes via linha de comando.
- TShark — versão em terminal do Wireshark.
- Nmap — descoberta de hosts e portas.
- ping — teste de conectividade.
- traceroute / tracert — análise de rotas de rede.

---

📖 Referências

- Documentação oficial do Wireshark.
- Wireshark User's Guide.
- RFC 791 – Internet Protocol (IPv4).
- RFC 9293 – Transmission Control Protocol (TCP).
- RFC 768 – User Datagram Protocol (UDP).