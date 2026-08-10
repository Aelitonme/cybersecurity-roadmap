📡 DHCP (Dynamic Host Configuration Protocol)

«Categoria: Redes de Computadores
Nível: Básico
Status: 📖 Revisão»

---

📌 O que é?

O DHCP (Dynamic Host Configuration Protocol) é um protocolo responsável por fornecer automaticamente configurações de rede para os dispositivos.

Quando um computador ou celular entra em uma rede, ele precisa de informações como:

- Endereço IP.
- Máscara de sub-rede.
- Gateway padrão.
- Servidor DNS.

Em vez de configurar essas informações manualmente em cada dispositivo, o servidor DHCP pode entregá-las automaticamente.

---

🎯 Objetivos

- Distribuir endereços IP automaticamente.
- Evitar configurações manuais em cada dispositivo.
- Reduzir conflitos de endereços IP.
- Informar configurações importantes da rede.
- Facilitar a administração de redes com muitos dispositivos.

---

🧠 Conceitos importantes

O DHCP funciona seguindo uma sequência conhecida como:

DORA

Significa:

D → Discover
O → Offer
R → Request
A → Acknowledge

Uma forma simples de memorizar:

Cliente: "Tem algum servidor DHCP aí?"       → Discover

Servidor: "Tenho. Posso oferecer este IP."   → Offer

Cliente: "Quero utilizar esse IP."           → Request

Servidor: "Confirmado. Pode utilizá-lo."     → ACK

---

🔄 Processo DORA

1️⃣ DHCP Discover

Quando um dispositivo entra na rede, ele ainda não possui as configurações necessárias.

Então envia uma mensagem:

DHCP Discover

Basicamente perguntando:

«"Existe algum servidor DHCP nesta rede?"»

Como o dispositivo ainda não conhece o servidor DHCP, essa mensagem normalmente é enviada por broadcast.

---

2️⃣ DHCP Offer

O servidor DHCP recebe a solicitação e responde:

DHCP Offer

Ele oferece uma configuração ao dispositivo.

Por exemplo:

IP:      192.168.1.20
Máscara: 255.255.255.0
Gateway: 192.168.1.1
DNS:     192.168.1.1

É basicamente o servidor dizendo:

«"Tenho este endereço disponível para você."»

---

3️⃣ DHCP Request

O cliente recebe a oferta e responde:

DHCP Request

Ele informa que deseja utilizar a configuração oferecida.

É como dizer:

«"Quero utilizar esse endereço IP."»

---

4️⃣ DHCP ACK

Finalmente, o servidor responde:

DHCP ACK

ACK significa Acknowledgment.

É a confirmação de que o endereço foi concedido ao dispositivo.

O servidor está basicamente dizendo:

«"Confirmado. Você pode utilizar esse endereço."»

---

📊 Processo completo

        CLIENTE                         SERVIDOR DHCP

           │
           │──── DHCP Discover ───────────►
           │
           │◄──── DHCP Offer ─────────────
           │
           │──── DHCP Request ────────────►
           │
           │◄──── DHCP ACK ───────────────
           │
           ▼

      Configuração recebida

Ou simplesmente:

DISCOVER
   ↓
OFFER
   ↓
REQUEST
   ↓
ACK

---

⏳ DHCP Lease

O endereço IP fornecido pelo DHCP normalmente não pertence permanentemente ao dispositivo.

Ele é concedido por determinado período.

Esse período é chamado de:

DHCP Lease

ou:

Tempo de concessão.

Por exemplo:

Notebook recebe:

192.168.1.20

Lease:

24 horas

Antes do tempo terminar, o dispositivo normalmente tenta renovar a concessão.

---

🗃️ Pool DHCP

O servidor DHCP possui uma faixa de endereços disponíveis para distribuir.

Essa faixa é chamada de DHCP Pool.

Exemplo:

192.168.1.100
até
192.168.1.200

Quando um dispositivo entra:

Notebook → 192.168.1.100
Celular  → 192.168.1.101
TV       → 192.168.1.102

O servidor administra quais endereços estão sendo utilizados.

---

🚪 Portas utilizadas

O DHCP utiliza UDP.

Porta| Função
UDP 67| Servidor DHCP
UDP 68| Cliente DHCP

Portanto:

Servidor → UDP 67
Cliente  → UDP 68

---

🏠 Quem é o servidor DHCP?

Em uma rede doméstica, normalmente o próprio roteador executa a função de servidor DHCP.

Por exemplo:

Internet
   │
   ▼
Roteador
192.168.1.1
   │
   │ DHCP
   │
   ├── Notebook → 192.168.1.20
   ├── Celular  → 192.168.1.21
   └── TV       → 192.168.1.22

Em empresas, pode existir um servidor dedicado responsável pelo DHCP.

---

💡 Exemplo prático

Você chega em casa e conecta seu celular ao Wi-Fi.

Você não precisa configurar manualmente:

IP
Máscara
Gateway
DNS

O processo acontece automaticamente.

Simplificando:

Celular
   │
   │ "Tem DHCP?"
   ▼
Roteador
   │
   │ "Use 192.168.1.25"
   ▼
Celular
   │
   │ "Quero esse IP."
   ▼
Roteador
   │
   │ "Confirmado."
   ▼
Celular conectado

---

⚠️ O que acontece se o DHCP falhar?

O dispositivo pode ficar sem uma configuração IPv4 válida para aquela rede.

Isso pode causar:

- Falha no acesso à Internet.
- Falha na comunicação com outros dispositivos.
- Ausência de gateway.
- Problemas de DNS.
- Endereço autoconfigurado pelo próprio sistema.

Em alguns sistemas, o dispositivo pode utilizar automaticamente um endereço link-local.

No IPv4, é comum encontrar:

169.254.x.x

Esse mecanismo é conhecido no Windows como APIPA.

Encontrar um endereço "169.254.x.x" pode ser uma pista de que o dispositivo não conseguiu obter uma configuração IPv4 via DHCP.

---

🔍 DHCP e investigação de rede

O DHCP também pode fornecer informações úteis durante uma investigação.

Imagine que os registros mostram:

10:00 → 192.168.1.20 → Notebook-A

14:00 → Lease expirou

15:00 → 192.168.1.20 → Notebook-B

O mesmo endereço IP pode ter sido utilizado por dispositivos diferentes em momentos diferentes.

Por isso:

«Somente o endereço IP pode não ser suficiente para identificar historicamente um dispositivo.»

É importante correlacionar informações como:

IP + MAC + horário + logs DHCP

Isso permite entender melhor qual dispositivo possuía determinado IP em determinado momento.

---

🛡️ DHCP e Segurança

O DHCP também possui importância em cybersecurity.

Um exemplo de ameaça é um Rogue DHCP Server.

Isso acontece quando um servidor DHCP não autorizado aparece na rede e começa a fornecer configurações aos dispositivos.

Ele poderia, por exemplo, informar um gateway ou servidor DNS controlado pelo atacante.

Por isso, redes corporativas podem utilizar mecanismos adicionais de proteção, como DHCP Snooping em switches compatíveis.

---

🔄 DHCP × DNS

Os dois protocolos possuem funções diferentes.

DHCP| DNS
Fornece configurações de rede.| Traduz nomes em endereços IP.
Pode entregar IP ao dispositivo.| Localiza o IP associado a um domínio.
Pode informar qual DNS utilizar.| Responde consultas sobre nomes.

Um dispositivo pode receber via DHCP:

IP:      192.168.1.20
Gateway: 192.168.1.1
DNS:     1.1.1.1

Depois utiliza o servidor DNS informado para resolver nomes de domínio.

---

🔄 DHCP × NAT

Também são funções diferentes:

DHCP
↓
Entrega uma configuração IP ao dispositivo.

NAT/PAT
↓
Traduz endereços/conexões entre a rede privada e a rede externa.

Exemplo simplificado:

DHCP
   ↓
Notebook recebe
192.168.1.20
   ↓
NAT/PAT no roteador
   ↓
IP público
   ↓
Internet

---

📝 Resumo

O DHCP automatiza a configuração dos dispositivos em uma rede.

Quando um dispositivo entra na rede, ocorre normalmente o processo DORA:

1. Discover.
2. Offer.
3. Request.
4. ACK.

Depois disso, o dispositivo recebe as configurações necessárias para participar da rede durante determinado período chamado lease.

---

🎓 O que preciso lembrar?

- ✅ DHCP significa Dynamic Host Configuration Protocol.
- ✅ Distribui configurações de rede automaticamente.
- ✅ DORA = Discover → Offer → Request → ACK.
- ✅ DHCP utiliza UDP.
- ✅ Servidor utiliza porta UDP 67.
- ✅ Cliente utiliza porta UDP 68.
- ✅ Lease é o período de concessão do endereço.
- ✅ Pool é a faixa de IPs disponíveis.
- ✅ "169.254.x.x" pode indicar falha na obtenção de configuração IPv4 via DHCP.
- ✅ Logs DHCP podem ajudar em investigações.

---

❓ Perguntas para revisar

1. O que é DHCP?
2. Qual é sua principal função?
3. O que significa DORA?
4. O que acontece no DHCP Discover?
5. O que significa DHCP Offer?
6. Para que serve o DHCP Request?
7. O que significa ACK?
8. O que é DHCP Lease?
9. O que é DHCP Pool?
10. Quais portas o DHCP utiliza?
11. O que pode indicar um endereço "169.254.x.x"?
12. Por que IP + horário + MAC + logs são importantes em uma investigação?

---

🔑 Palavras-chave

- DHCP
- DORA
- Discover
- Offer
- Request
- ACK
- DHCP Lease
- DHCP Pool
- UDP 67
- UDP 68
- APIPA
- IP
- Gateway
- DNS
- MAC Address
- Rogue DHCP
- DHCP Snooping

---

🛠️ Ferramentas relacionadas

- Wireshark — permite observar o processo DORA.
- ipconfig — consulta configurações de rede no Windows.
- ip — consulta interfaces e endereços no Linux.
- Cisco Packet Tracer — permite criar laboratórios DHCP.
- tcpdump — captura tráfego DHCP pelo terminal.

---

📖 Referências

- RFC 2131 — Dynamic Host Configuration Protocol.
- RFC 2132 — DHCP Options and BOOTP Vendor Extensions.
- RFC 3927 — Dynamic Configuration of IPv4 Link-Local Addresses.