🔄 NAT (Network Address Translation)

«Categoria: Redes de Computadores
Nível: Básico
Status: 📖 Revisão»

---

📌 O que é?

O NAT (Network Address Translation) é um mecanismo utilizado principalmente em roteadores para traduzir endereços IP privados em endereços IP públicos, e vice-versa.

Ele permite que vários dispositivos de uma rede local utilizem um endereço IP público para se comunicar com a Internet.

Imagine uma casa com vários dispositivos:

Celular      → 192.168.1.10
Notebook     → 192.168.1.20
Computador   → 192.168.1.30
                    │
                    ▼
                 Roteador
                    │
                    ▼
              IP Público
                    │
                    ▼
                 Internet

Os dispositivos utilizam endereços privados dentro da rede. Quando precisam acessar a Internet, o roteador realiza a tradução necessária.

---

🎯 Objetivos

- Permitir que dispositivos com IP privado acessem a Internet.
- Reduzir a necessidade de endereços IPv4 públicos.
- Traduzir endereços entre redes privadas e públicas.
- Permitir que vários dispositivos compartilhem um endereço público quando utilizado junto ao PAT.

---

🧠 Conceitos importantes

IP Privado

É utilizado dentro de redes locais e não é roteável diretamente pela Internet pública.

Faixas privadas IPv4:

10.0.0.0     – 10.255.255.255
172.16.0.0   – 172.31.255.255
192.168.0.0  – 192.168.255.255

IP Público

É um endereço utilizado para comunicação através da Internet pública.

Normalmente é atribuído pelo provedor de Internet à conexão do cliente.

---

📚 Como funciona?

Imagine um notebook com:

192.168.1.20

Ele deseja acessar um servidor na Internet.

O pacote chega ao roteador.

O roteador realiza uma tradução:

192.168.1.20

        ↓ NAT

203.0.113.10

        ↓

Internet

Para o servidor externo, a comunicação aparece como originada do endereço público do roteador.

Quando a resposta retorna, o roteador consulta o estado da tradução e encaminha o tráfego ao dispositivo correto da rede interna.

---

🚪 NAT e PAT

Em redes domésticas é extremamente comum encontrar PAT (Port Address Translation).

O PAT permite que vários dispositivos compartilhem o mesmo endereço IP público utilizando números de portas diferentes.

Exemplo:

192.168.1.10:5000 ─┐
                    │
192.168.1.20:5001 ─┼──► 203.0.113.10
                    │
192.168.1.30:5002 ─┘

O roteador mantém uma tabela para saber qual conexão pertence a cada dispositivo.

---

📋 Exemplo de tradução

Imagine:

Notebook
192.168.1.20:5000

Ao acessar a Internet, o roteador pode criar uma tradução como:

IP privado                 IP público

192.168.1.20:5000   →   203.0.113.10:40001

Quando uma resposta chega para:

203.0.113.10:40001

o roteador consulta sua tabela e sabe que deve encaminhá-la para a conexão correspondente do notebook.

---

🗃️ Tabela NAT/PAT

Uma representação simplificada seria:

Dispositivo| Endereço interno| Tradução externa
Notebook| 192.168.1.20:5000| 203.0.113.10:40001
Celular| 192.168.1.30:5000| 203.0.113.10:40002
PC| 192.168.1.40:5000| 203.0.113.10:40003

Mesmo que diferentes dispositivos utilizem a mesma porta internamente, o roteador pode diferenciá-los por meio das traduções que mantém.

---

🔢 Tipos de NAT

NAT Estático

Cria uma associação fixa entre um endereço privado e um endereço público.

192.168.1.10 ↔ 203.0.113.10

É útil quando determinado equipamento precisa de uma tradução previsível.

---

NAT Dinâmico

Utiliza um conjunto de endereços públicos disponíveis.

Um endereço privado recebe temporariamente um dos endereços públicos desse conjunto.

---

PAT / NAT Overload

Permite que vários dispositivos utilizem um único endereço IP público.

As conexões são diferenciadas principalmente pelos números das portas.

É muito utilizado em:

- Casas.
- Escritórios.
- Pequenas empresas.

---

💡 Analogia simples

Imagine um prédio.

O endereço do prédio é:

203.0.113.10

Existem vários apartamentos:

Apartamento 10
Apartamento 20
Apartamento 30

O endereço do prédio representa o IP público.

Os apartamentos representam os dispositivos internos.

O NAT/PAT funciona como um porteiro que registra de qual apartamento saiu cada comunicação.

Quando chega uma resposta, ele consulta seu registro e entrega ao apartamento correto.

---

🌐 Exemplo completo

Seu notebook possui:

192.168.1.20

Você acessa um site.

O fluxo simplificado pode ser:

Notebook
192.168.1.20
      │
      ▼
Roteador
NAT/PAT
      │
      ▼
IP Público
203.0.113.10
      │
      ▼
Internet
      │
      ▼
Servidor

A resposta realiza o caminho inverso:

Servidor
    │
    ▼
203.0.113.10
    │
    ▼
Roteador consulta a tradução
    │
    ▼
192.168.1.20
    │
    ▼
Notebook

---

🛡️ NAT e Segurança

O NAT dificulta conexões iniciadas diretamente da Internet para dispositivos internos quando não existe uma tradução ou regra correspondente.

Porém:

«NAT não substitui um firewall.»

O objetivo principal do NAT é tradução de endereços, e não fornecer segurança.

Firewalls possuem funções específicas para permitir, bloquear e inspecionar tráfego de acordo com regras de segurança.

---

🔄 NAT × Firewall

NAT| Firewall
Traduz endereços.| Controla o tráfego.
Trabalha com IPs e, dependendo do mecanismo, portas.| Aplica regras de segurança.
Permite comunicação entre diferentes espaços de endereçamento.| Permite ou bloqueia conexões.
Não é um mecanismo de segurança completo.| É projetado para controle e proteção do tráfego.

---

📝 Resumo

O NAT traduz endereços utilizados dentro de uma rede para endereços utilizados em outra rede.

Em redes domésticas, normalmente encontramos NAT associado ao PAT, permitindo que vários dispositivos com endereços privados compartilhem um único endereço IPv4 público.

O roteador mantém informações sobre as traduções para saber para qual dispositivo interno deve encaminhar cada resposta.

---

🎓 O que preciso lembrar?

- ✅ NAT significa Network Address Translation.
- ✅ Traduz endereços IP entre redes.
- ✅ Endereços privados não são roteados diretamente pela Internet pública.
- ✅ PAT utiliza portas para diferenciar conexões.
- ✅ Vários dispositivos podem compartilhar um IP público através de PAT.
- ✅ O roteador mantém informações sobre as traduções.
- ✅ NAT não substitui um firewall.

---

❓ Perguntas para revisar

1. O que significa NAT?
2. Qual é a principal função do NAT?
3. Qual a diferença entre IP privado e IP público?
4. Por que utilizamos NAT?
5. O que é PAT?
6. Como o roteador diferencia conexões de vários dispositivos utilizando o mesmo IP público?
7. Qual a diferença entre NAT estático e dinâmico?
8. NAT e firewall são a mesma coisa?
9. Quais são as três faixas IPv4 privadas?
10. Como o roteador sabe para qual dispositivo enviar uma resposta?

---

🔑 Palavras-chave

- NAT
- Network Address Translation
- PAT
- NAT Overload
- IPv4
- IP Privado
- IP Público
- Porta
- Roteador
- Tabela NAT
- Tradução de Endereços

---

🛠️ Ferramentas relacionadas

- Wireshark — análise dos pacotes antes e depois de atravessarem diferentes pontos da rede.
- traceroute / tracert — análise do caminho dos pacotes.
- ip / ipconfig — consulta dos endereços das interfaces.
- ss / netstat — visualização de conexões e portas.
- Cisco Packet Tracer — criação de laboratórios para estudar NAT e PAT.

---

📖 Referências

- RFC 1918 — Address Allocation for Private Internets.
- RFC 3022 — Traditional IP Network Address Translator (Traditional NAT).
- RFC 6888 — Common Requirements for Carrier-Grade NATs.