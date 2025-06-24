# 🧠 Análise de Fala e Linguagem Natural com Azure Speech Studio e Language Studio

Este repositório demonstra como utilizar ferramentas da Microsoft Azure para realizar transcrição de fala e análise de linguagem natural. Usaremos o **Speech Studio** para converter áudio em texto, e o **Azure AI Foundry (Language Studio)** para extrair entidades, frases-chave e resumos.

## ✅ Pré-requisitos

- Conta no [Azure Portal](https://portal.azure.com/)
- Recursos de Azure AI criados ou permissão para criá-los
- Navegador atualizado
- Áudio (em `.wav`, `.mp3`, etc.) e/ou textos para testes

---

## 🔊 Etapa 1 – Transcrição de Fala com Azure Speech Studio

1. Acesse o [Speech Studio](https://speech.microsoft.com/portal) e faça login.
2. No painel lateral, selecione **Speech-to-text**.
3. Envie um arquivo de áudio ou grave diretamente.
4. Configure o idioma e selecione um recurso de fala criado anteriormente.
5. Clique em **Recognize**.
6. O resultado incluirá:
   - Texto transcrito
   - Marcações temporais
   - Confiabilidade de cada trecho

---

## 🧠 Etapa 2 – Criação de Projeto no Azure AI Foundry

1. Acesse o portal do [Azure AI Foundry](https://ai.azure.com).
2. Vá em **Management Center > All Resources > Create**.
3. Escolha **Azure AI Foundry Resource**.
4. Preencha:
   - Nome do projeto
   - Assinatura e grupo de recursos
   - Região (East US, West Europe etc.)
5. Após criado, vá até **Playgrounds > Language Playground**.

---

## 🔍 Etapa 3 – Análises com Azure AI Language

### 🔹 Extração de Entidades Nomeadas

1. No Language Playground, vá em **Extract information > Extract named entities**.
2. Insira um texto (ex: avaliação de hotel).
3. Clique em **Run**.
4. Veja os tipos de entidades detectadas (local, data, organização) e suas pontuações de confiança.

### 🔹 Extração de Frases-Chave

1. Vá para **Extract information > Extract key phrases**.
2. Insira o texto desejado e clique em **Run**.
3. As frases extraídas representam os conceitos mais relevantes.

### 🔹 Resumo de Texto

1. Vá até **Summarize information > Summarize text**.
2. Cole um texto longo (ex: comentário de usuário).
3. Clique em **Run**.
4. Será gerado um resumo baseado nas sentenças com maior pontuação semântica.

---

## 🧹 Etapa Final – Limpeza de Recursos

Para evitar custos adicionais:

1. No [Azure Portal](https://portal.azure.com), vá no **Grupo de Recursos** usado.
2. Selecione os recursos e clique em **Excluir**.

---

## 📌 Recursos de Apoio

- [Documentação do Azure Speech](https://learn.microsoft.com/azure/cognitive-services/speech-service/)
- [Documentação do Azure AI Language](https://learn.microsoft.com/azure/ai-services/language-service/)
- [Azure AI Foundry Portal](https://ai.azure.com)

---

## 🧪 Exemplos de Uso Prático

### Exemplo 1: Transcrição de Reuniões

- **Cenário:** Uma equipe de projeto grava suas reuniões semanais.
- **Uso:** O áudio é enviado ao *Speech Studio* para transcrição automática.
- **Resultado:** O texto gerado é compartilhado com o time como ata da reunião, com marcações temporais para revisão de decisões.

### Exemplo 2: Análise de Comentários de Clientes

- **Cenário:** Uma empresa coleta avaliações de seus clientes sobre serviços de hotelaria.
- **Uso:** Os textos são processados no *Language Studio* com:
  - Extração de frases-chave para identificar pontos fortes e fracos.
  - Identificação de entidades para mapear locais e marcas mencionados.
  - Geração de resumos para relatórios executivos.

### Exemplo 3: Treinamento de Chatbots

- **Cenário:** Uma startup quer treinar um assistente virtual.
- **Uso:** Utiliza transcrições reais de conversas (Speech Studio) e as analisa com o *Language Studio* para extrair padrões de linguagem, intenções e entidades.
- **Resultado:** O modelo de linguagem do bot é aprimorado com base em dados reais.
