# 📜 Certificado Digital

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que é?

O **Certificado Digital** é um documento eletrônico que comprova a identidade de um servidor, site ou organização na Internet.

Ele funciona como uma **identidade digital**, permitindo que o navegador confirme se está realmente se comunicando com o servidor correto e não com um site falso.

Os certificados digitais são fundamentais para o funcionamento do **HTTPS**, pois são utilizados durante o **handshake TLS** para autenticar o servidor.

---

# 🎯 Objetivos

* Comprovar a identidade de um servidor.
* Permitir conexões HTTPS seguras.
* Aumentar a confiança durante a navegação.
* Reduzir o risco de ataques de falsificação de sites.

---

# 🧠 Conceitos importantes

* Todo site HTTPS utiliza um certificado digital.
* O certificado é emitido por uma **Autoridade Certificadora (CA)**.
* O navegador verifica automaticamente se o certificado é confiável.
* Um certificado possui prazo de validade e pode expirar.

---

# 📚 Como funciona?

Quando você acessa um site utilizando HTTPS:

1. O navegador solicita uma conexão segura.
2. O servidor envia seu certificado digital.
3. O navegador verifica se o certificado é válido.
4. Se estiver tudo correto, o navegador continua o handshake TLS.
5. A comunicação criptografada é iniciada.

Caso haja algum problema com o certificado, o navegador exibirá um aviso de segurança.

---

# ⚙️ O que contém um certificado digital?

Um certificado normalmente possui:

* Nome do domínio.
* Nome da organização (quando aplicável).
* Chave pública.
* Autoridade Certificadora (CA) que o emitiu.
* Número de série.
* Data de emissão.
* Data de expiração.
* Assinatura digital da Autoridade Certificadora.

---

# 🏛️ Autoridade Certificadora (CA)

Uma **Autoridade Certificadora (Certificate Authority)** é uma organização confiável responsável por emitir e assinar certificados digitais.

Alguns exemplos:

* Let's Encrypt
* DigiCert
* GlobalSign
* Sectigo

Os navegadores mantêm uma lista de CAs confiáveis para verificar a autenticidade dos certificados.

---

# 🔑 Relação com a criptografia

O certificado digital contém a **chave pública** do servidor.

Durante o handshake TLS:

* O cliente utiliza essa chave pública para estabelecer uma comunicação segura.
* O servidor utiliza sua **chave privada**, que nunca é compartilhada, para concluir o processo de autenticação e negociação das chaves.

---

# 💡 Exemplo prático

Imagine que você acessa o site do seu banco.

Antes de enviar sua senha, o navegador verifica o certificado digital.

Se o certificado for válido e pertencer ao domínio do banco, a conexão segura é estabelecida e seus dados passam a trafegar criptografados.

Se o certificado for inválido, expirado ou emitido para outro domínio, o navegador exibirá um alerta antes que você continue.

---

# ⚠️ O que acontece quando há problemas?

O navegador pode exibir mensagens como:

* Certificado expirado.
* Certificado inválido.
* Certificado emitido para outro domínio.
* Autoridade Certificadora não confiável.

Nesses casos, a conexão pode não ser segura e o ideal é não prosseguir sem verificar a causa.

---

# 🔒 Relação entre Certificado Digital, TLS e HTTPS

```text
Usuário acessa um site

        │
        ▼

Servidor envia o Certificado Digital

        │
        ▼

Navegador verifica a autenticidade

        │
        ▼

Handshake TLS

        │
        ▼

Comunicação HTTPS criptografada
```

O certificado digital é um dos elementos que tornam possível uma conexão HTTPS segura.

---

# 📝 Resumo

O certificado digital é a identidade de um servidor na Internet.

Ele é emitido por uma Autoridade Certificadora (CA) e utilizado durante o handshake TLS para autenticar o servidor.

Após essa verificação, cliente e servidor estabelecem uma conexão HTTPS criptografada, protegendo as informações transmitidas.

---

# 🎓 O que preciso lembrar?

* ✅ O certificado digital comprova a identidade do servidor.
* ✅ É utilizado pelo HTTPS.
* ✅ Faz parte do handshake TLS.
* ✅ Contém a chave pública do servidor.
* ✅ É emitido por uma Autoridade Certificadora (CA).
* ✅ Possui prazo de validade.

---

# ❓ Perguntas para revisar

1. O que é um certificado digital?
2. Qual é a função de um certificado digital?
3. O que é uma Autoridade Certificadora (CA)?
4. Em que momento o certificado é utilizado?
5. O que acontece se um certificado estiver expirado?
6. Qual a relação entre certificado digital, TLS e HTTPS?
7. O certificado contém a chave pública ou a chave privada?
8. Por que o navegador verifica o certificado antes de estabelecer a conexão?

---

# 🔑 Palavras-chave

* Certificado Digital
* HTTPS
* TLS
* SSL
* Chave Pública
* Chave Privada
* Autoridade Certificadora
* CA
* Handshake
* Criptografia
* Autenticação

---

# 🛠️ Ferramentas relacionadas

* **OpenSSL** — visualizar informações de certificados.
* **SSL Labs Server Test** — analisar certificados e configuração HTTPS de servidores.
* **Google Chrome** — clicar no cadeado da barra de endereços para visualizar detalhes do certificado.
* **Wireshark** — analisar o handshake TLS.

---

# 📖 Referências

* RFC 5280 – Internet X.509 Public Key Infrastructure Certificate.
* RFC 8446 – TLS 1.3.
* Mozilla Developer Network (MDN) – HTTPS e Certificados.
* Let's Encrypt – Documentação oficial.
