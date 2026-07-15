# 🌍 HTTP (HyperText Transfer Protocol)

> **Categoria:** Redes de Computadores
> **Nível:** Básico
> **Status:** 📖 Revisão

---

# 📌 O que é?

O **HTTP (HyperText Transfer Protocol)** é um protocolo de comunicação utilizado para transferir informações entre um **cliente** e um **servidor** na Internet.

Ele permite que navegadores, aplicativos e outros sistemas solicitem recursos, como páginas web, imagens, vídeos e arquivos.

O HTTP funciona seguindo o modelo **Cliente → Servidor**, onde o cliente inicia a comunicação enviando uma requisição e o servidor responde com o recurso solicitado.

---

# 🎯 Objetivos

* Permitir a comunicação entre cliente e servidor.
* Solicitar recursos disponíveis em um servidor.
* Entregar respostas ao cliente.
* Padronizar a comunicação na Web.

---

# 🧠 Conceitos importantes

* O HTTP é um protocolo da **Camada de Aplicação** do Modelo TCP/IP.
* O cliente sempre inicia a comunicação.
* O servidor aguarda solicitações e responde quando recebe uma requisição.
* O HTTP é um protocolo **sem estado (stateless)**, ou seja, cada requisição é independente da anterior.

---

# 📚 Como funciona?

A comunicação ocorre em três etapas:

### 1. Cliente envia uma requisição

O navegador ou aplicativo solicita um recurso ao servidor.

Exemplo:

* Acessar um site.
* Baixar uma imagem.
* Fazer login.
* Enviar um formulário.

---

### 2. Servidor processa a solicitação

O servidor recebe a requisição, verifica o pedido e prepara uma resposta.

---

### 3. Servidor responde

O servidor envia uma resposta contendo:

* Página HTML.
* Imagem.
* Arquivo.
* Mensagem de erro.
* Dados em JSON.
* Vídeo.

---

# ⚙️ Funcionamento

```
Cliente (Navegador)

        │
        │ Requisição HTTP
        ▼

Servidor Web

        │
        │ Resposta HTTP
        ▼

Cliente recebe a página
```

---

# 💡 Exemplo prático

Imagine que você digita no navegador:

```
https://www.google.com
```

O navegador envia uma requisição HTTP (ou HTTPS) para o servidor do Google.

O servidor processa a solicitação e responde enviando os arquivos necessários para que a página seja exibida.

---

# 🔄 Métodos HTTP

Os métodos informam ao servidor qual ação o cliente deseja realizar.

## GET

Solicita informações.

Exemplo:

Buscar uma página ou consultar um produto.

---

## POST

Envia informações ao servidor.

Exemplo:

Fazer login ou cadastrar um usuário.

---

## PUT

Atualiza completamente um recurso existente.

Exemplo:

Alterar todos os dados de um usuário.

---

## PATCH

Atualiza apenas parte de um recurso.

Exemplo:

Alterar somente o e-mail de um usuário.

---

## DELETE

Remove um recurso.

Exemplo:

Excluir uma conta ou um arquivo.

---

# 📩 Estrutura de uma requisição HTTP

Uma requisição normalmente possui:

* Método (GET, POST, PUT...)
* URL
* Cabeçalhos (Headers)
* Corpo (Body), quando necessário

Exemplo:

```
GET /produtos HTTP/1.1
Host: exemplo.com
```

---

# 📨 Estrutura de uma resposta HTTP

Uma resposta geralmente contém:

* Código de status.
* Cabeçalhos.
* Corpo da resposta.

Exemplo:

```
HTTP/1.1 200 OK
```

---

# 🚦 Principais códigos HTTP

## 200 OK

A solicitação foi realizada com sucesso.

---

## 201 Created

Um recurso foi criado com sucesso.

---

## 301 Moved Permanently

O recurso foi movido permanentemente.

---

## 400 Bad Request

A requisição possui erro de sintaxe ou dados inválidos.

---

## 401 Unauthorized

É necessário realizar autenticação.

---

## 403 Forbidden

O servidor entendeu a solicitação, mas negou o acesso.

---

## 404 Not Found

O recurso solicitado não foi encontrado.

---

## 500 Internal Server Error

Erro interno no servidor.

---

## 503 Service Unavailable

O serviço está temporariamente indisponível.

---

# 🔒 HTTP × HTTPS

| HTTP                                               | HTTPS                          |
| -------------------------------------------------- | ------------------------------ |
| Não utiliza criptografia.                          | Utiliza criptografia TLS/SSL.  |
| Menos seguro.                                      | Mais seguro.                   |
| Porta padrão 80.                                   | Porta padrão 443.              |
| Dados podem ser interceptados com mais facilidade. | Dados trafegam criptografados. |

---

# 📝 Resumo

O HTTP é o protocolo responsável pela comunicação entre clientes e servidores na Web.

O cliente sempre inicia a comunicação enviando uma requisição.

O servidor processa a solicitação e responde com o recurso solicitado.

Para proteger essa comunicação, normalmente utiliza-se o **HTTPS**, que adiciona criptografia por meio do protocolo TLS.

---

# 🎓 O que preciso lembrar?

* ✅ HTTP significa **HyperText Transfer Protocol**.
* ✅ O cliente inicia a comunicação.
* ✅ O servidor responde à solicitação.
* ✅ HTTP pertence à Camada de Aplicação.
* ✅ HTTPS utiliza criptografia (TLS).
* ✅ GET consulta informações.
* ✅ POST envia dados.
* ✅ 404 significa que o recurso não foi encontrado.
* ✅ 200 significa sucesso.

---

# ❓ Perguntas para revisar

1. O que é o protocolo HTTP?
2. Quem inicia a comunicação: cliente ou servidor?
3. Qual é a função do servidor?
4. O que significa HTTP ser "stateless"?
5. Qual a diferença entre HTTP e HTTPS?
6. Qual método é utilizado para consultar informações?
7. Qual método é utilizado para enviar dados?
8. O que significa o código HTTP 404?
9. O que significa o código HTTP 200?
10. Em qual camada do Modelo TCP/IP o HTTP atua?

---

# 🔑 Palavras-chave

* HTTP
* HTTPS
* Cliente
* Servidor
* Requisição
* Resposta
* GET
* POST
* PUT
* PATCH
* DELETE
* Status Code
* TLS
* Navegador

---

# 🛠️ Ferramentas relacionadas

* **Google Chrome DevTools (Network)** — visualizar requisições e respostas HTTP.
* **Postman** — testar APIs e métodos HTTP.
* **curl** — enviar requisições HTTP pelo terminal.
* **Wireshark** — analisar o tráfego de rede.

---

# 📖 Referências

* RFC 9110 – HTTP Semantics.
* RFC 9112 – HTTP/1.1.
* Documentação do Mozilla Developer Network (MDN) sobre HTTP.
