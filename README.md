<div align="center">
  <img src="https://img.shields.io/badge/Semantic_Kernel-1.0-blue?style=for-the-badge&logo=microsoft&logoColor=white" alt="Semantic Kernel Badge"/>
  <img src="https://img.shields.io/badge/Google-Gemini-4285F4?style=for-the-badge&logo=google&logoColor=white" alt="Gemini Badge"/>
  <img src="https://img.shields.io/badge/IA-Generativa-orange?style=for-the-badge" alt="Generative AI Badge"/>
  <img src="https://img.shields.io/badge/Licença-MIT-green?style=for-the-badge" alt="License MIT Badge"/>
</div>

<h1 align="center">🧠 TechGadgets API Inteligente</h1>

<p align="center">
  <strong>O código-fonte oficial do e-book 📘 "APIs Inteligentes: .NET, Semantic Kernel e Gemini"</strong>
</p>

<p align="center">
  Esta é a evolução da TechGadgets API. Neste projeto, integramos o poder da <strong>Inteligência Artificial Generativa</strong> para criar uma experiência de usuário rica e automatizada.
</p>

<p align="center">
  <a href="#-pré-requisitos"><strong>Pré-requisitos</strong></a> •
  <a href="#-o-que-há-de-novo"><strong>Novas Features de IA</strong></a> •
  <a href="#-começando"><strong>Como Começar</strong></a> •
  <a href="#-testando-a-ia"><strong>Testando a IA</strong></a>
</p>

---

### ⚠️ Pré-requisitos

> Este projeto é a continuação direta do e-book "Construindo APIs Escaláveis em .NET Core". Para o máximo aproveitamento, é **altamente recomendado** que você tenha concluído o primeiro livro ou que tenha um domínio completo do projeto base.
> 
> - **Repositório Base:** `techgadgets-api-dotnet`
> - **Nova Dependência:** Uma chave de API para o **Google Gemini**, que pode ser obtida gratuitamente no [Google AI Studio](https://aistudio.google.com/).

<div align="center">
  <h3>🚀 Adquira já o e-book "APIs Inteligentes" e adicione IA ao seu portfólio!</h3>
  <p><em>[Link para a página de vendas do seu segundo e-book aqui]</em></p>
</div>

---

### 🧠 O que há de novo?

Evoluímos a API da TechGadgets com um "cérebro" de IA, orquestrado pelo **Microsoft Semantic Kernel** e alimentado pelo **Google Gemini**.

| Categoria              | Feature                                                                      |
| ---------------------- | ---------------------------------------------------------------------------- |
| 🤖 **Orquestração de IA** | Uso do Microsoft Semantic Kernel para criar e combinar funções de IA (Plugins). |
| 🧠 **Motor de IA**        | Integração nativa com a API do Google Gemini, aproveitando o nível gratuito.   |
| 🧩 **Injeção de Dependência** | Configuração elegante com `Microsoft.Extensions.AI` para registrar o Kernel.     |
| ✍️ **Geração de Conteúdo** | Gerador de descrições de produtos que cria textos de marketing atraentes.    |
| 💬 **Chatbot Inteligente** | Chatbot especialista que responde perguntas sobre os produtos usando Plugins.  |
| 🔍 **Busca Avançada**     | Busca Semântica que entende linguagem natural através de `Planners`.         |
| 🖼️ **Análise de Imagem**  | Identificação de produtos por imagem usando o **Gemini Pro Vision**.         |

---

### 🏁 Começando

Os passos são similares ao projeto base, com um passo adicional para configurar a chave de IA.

#### 1. Pré-requisitos
- Todos os pré-requisitos do projeto base.
- Sua chave de API do Google Gemini.

#### 2. Clone o Repositório
```bash
git clone https://github.com/seu-usuario/techgadgets-api-ia-semantic-kernel.git
cd techgadgets-api-ia-semantic-kernel
```

#### 3. Configure a Chave de API
Renomeie o arquivo `appsettings.Development.json.example` para `appsettings.Development.json`. Além das configurações do projeto anterior, adicione sua chave do Gemini na nova seção `Gemini`:

```json
{
  // ... outras configurações
  "Gemini": {
    "ApiKey": "SUA_CHAVE_DO_GEMINI_API_AQUI"
  }
}
```

#### 4. Rodando com Docker (Recomendado)
O mesmo comando sobe todo o ambiente. A API já estará pronta para usar as features de IA.

```bash
docker-compose up -d --build
```

---

### 🚀 Exemplos de Uso (Testando a IA)

Use o **Swagger UI** (`http://localhost:8080/swagger`) ou `curl` para interagir com os novos endpoints de IA.

#### Gerar a descrição de um produto (ID 1):

```bash
curl -X POST http://localhost:8080/api/product/1/generate-description
```

#### Conversar com o chatbot especialista:

```bash
curl -X POST http://localhost:8080/api/chat \
  -H "Content-Type: application/json" \
  -d '{
    "question": "O notebook gamer tem teclado iluminado e qual a sua memória RAM?"
  }'
```

---

### 🏛️ Evolução da Arquitetura

A **Clean Architecture** do projeto original nos permitiu adicionar as novas capacidades de IA de forma limpa e isolada.

- **ProductApi.Core:** Agora contém as interfaces para os serviços de IA.
- **ProductApi.Infrastructure:** Implementa os conectores para o Semantic Kernel e o Gemini.
- **ProductApi.Api:** Expõe os novos endpoints inteligentes.

---

### 🤝 Contribuindo

Sua ajuda é bem-vinda! Se encontrar qualquer problema ou tiver uma sugestão, por favor, abra uma [**Issue**](https://github.com/seu-usuario/techgadgets-api-ia-semantic-kernel/issues).

---

### 📄 Licença

Este projeto é distribuído sob a licença MIT. Veja o arquivo `LICENSE` para mais detalhes.
