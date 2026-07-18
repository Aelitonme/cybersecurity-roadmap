# 🔒 HTTPS (HyperText Transfer Protocol Secure)

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que é?

O **HTTPS (HyperText Transfer Protocol Secure)** é a versão segura do protocolo HTTP.

Ele utiliza o protocolo **TLS (Transport Layer Security)** para criptografar a comunicação entre o cliente e o servidor, protegendo as informações durante a transmissão.

Sempre que você acessa um site que começa com:

```text
https://
```

significa que a comunicação está protegida por criptografia.

---

# 🎯 Objetivos

* Proteger os dados transmitidos entre cliente e servidor.
* Impedir que terceiros leiam informações durante a comunicação.
* Garantir que os dados não sejam alterados durante o trajeto.
* Confirmar que o usuário está se comunicando com o servidor correto.

---

# 🧠 Conceitos importantes

* HTTPS = **HTTP + TLS**.
* Toda comunicação é criptografada antes de ser enviada.
* Utiliza certificados digitais para autenticar a identidade do servidor.
* É utilizado na maioria dos sites modernos.

---

# 📚 Como funciona?

Quando você acessa um site utilizando HTTPS, ocorre um processo chamado **handshake TLS**.

Durante esse processo:

1. O navegador solicita uma conexão segura.
2. O servidor envia seu certificado digital.
3. O navegador verifica se o certificado é confiável.
4. Cliente e servidor negociam chaves criptográficas.
5. A comunicação criptografada é iniciada.

Depois disso, todos os dados trafegam protegidos.

---

# ⚙️ Funcionamento passo a passo

### 1. O usuário acessa um site

Exemplo:

```text
https://www.openai.com
```

↓

### 2. O navegador solicita uma conexão segura

O servidor responde enviando seu certificado digital.

↓

### 3. O navegador valida o certificado

Ele verifica:

* Quem emitiu o certificado.
* Se ele ainda é válido.
* Se pertence ao domínio acessado.

↓

### 4. Cliente e servidor negociam uma chave de sessão

Essa chave será utilizada para criptografar toda a comunicação.

↓

### 5. Comunicação segura

Agora todas as informações trafegam criptografadas.

---

# 🔐 O que o HTTPS protege?

Durante a comunicação, informações como:

* Senhas.
* Dados bancários.
* Cartões de crédito.
* Cookies de sessão.
* Dados pessoais.
* Mensagens.

São protegidas contra interceptação.

---

# 🛡️ Os três pilares da segurança

O HTTPS ajuda a garantir três propriedades fundamentais:

## Confidencialidade

Somente o cliente e o servidor conseguem ler as informações transmitidas.

---

## Integridade

Os dados não podem ser alterados durante a transmissão sem que isso seja detectado.

---

## Autenticação

O certificado digital ajuda a confirmar que o servidor é realmente quem diz ser.

---

# 💡 Exemplo prático

Imagine que você faz login em um banco.

Sem HTTPS:

* Usuário envia login.
* Senha viaja pela rede sem criptografia.
* Um invasor pode interceptar essas informações.

Com HTTPS:

* Login e senha são criptografados.
* Mesmo que alguém intercepte os dados, eles estarão ilegíveis sem a chave correta.

---

# ⚖️ HTTP × HTTPS

| HTTP                             | HTTPS                        |
| -------------------------------- | ---------------------------- |
| Não utiliza criptografia.        | Utiliza criptografia TLS.    |
| Porta padrão 80.                 | Porta padrão 443.            |
| Comunicação em texto legível.    | Comunicação criptografada.   |
| Menor segurança.                 | Maior segurança.             |
| Não utiliza certificado digital. | Utiliza certificado digital. |

---

# 📜 Certificado Digital

Um certificado digital funciona como uma identidade do servidor.

Ele contém informações como:

* Nome do domínio.
* Chave pública.
* Autoridade Certificadora (CA).
* Data de validade.

O navegador utiliza essas informações para verificar se a conexão é confiável.

---

# ⚠️ Riscos de utilizar apenas HTTP

Sem HTTPS, um agente malicioso pode:

* Interceptar senhas.
* Roubar cookies.
* Alterar páginas durante a transmissão.
* Espionar informações enviadas pelo usuário.
* Realizar ataques do tipo **Man-in-the-Middle (MitM)**.

---

# 📝 Resumo

O HTTPS é a versão segura do HTTP.

Ele utiliza o protocolo TLS para criptografar a comunicação entre cliente e servidor.

Além da criptografia, o HTTPS também utiliza certificados digitais para autenticar o servidor e garantir maior segurança durante a navegação.

---

# 🎓 O que preciso lembrar?

* ✅ HTTPS significa **HyperText Transfer Protocol Secure**.
* ✅ Utiliza o protocolo TLS.
* ✅ Criptografa a comunicação.
* ✅ Utiliza certificados digitais.
* ✅ Porta padrão **443**.
* ✅ Garante confidencialidade, integridade e autenticação.

---

# ❓ Perguntas para revisar

1. O que é HTTPS?
2. Qual a diferença entre HTTP e HTTPS?
3. O que é TLS?
4. Para que serve um certificado digital?
5. Qual é a porta padrão do HTTPS?
6. Quais informações o HTTPS protege?
7. O que é o handshake TLS?
8. Quais propriedades de segurança o HTTPS ajuda a garantir?

---

# 🔑 Palavras-chave

* HTTPS
* HTTP
* TLS
* SSL
* Certificado Digital
* Criptografia
* Handshake
* Porta 443
* Confidencialidade
* Integridade
* Autenticação

---

# 🛠️ Ferramentas relacionadas

* **Google Chrome DevTools** — visualizar detalhes da conexão HTTPS.
* **OpenSSL** — inspecionar certificados e conexões TLS.
* **Wireshark** — analisar o handshake TLS.
* **SSL Labs Server Test** — verificar a configuração HTTPS de um servidor.

---

# 📖 Referências

* RFC 9110 – HTTP Semantics.
* RFC 8446 – The Transport Layer Security (TLS) Protocol Version 1.3.
* Documentação da Mozilla (MDN) sobre HTTPS e TLS.
* OWASP Transport Layer Protection Cheat Sheet.
