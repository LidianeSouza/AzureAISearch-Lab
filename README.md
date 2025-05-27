# 🔍 Laboratório de Azure AI Search

## Objetivo
Aplicação de técnicas de organização e pesquisa de documentos utilizando Azure AI Search.

## 📌 Etapas Realizadas

### 1️⃣ Ingestão de Conteúdo
- Dados fornecidos pelo Microsoft Learning.
- Processo de upload e estruturação dos documentos.

### 2️⃣ Criação de Índices Inteligentes
- Configuração do índice no Azure AI Search.
- Estratégias utilizadas para otimizar buscas.

### 3️⃣ Exploração de Dados
- Consultas realizadas para extrair insights.
- Exemplos práticos de utilização.

## 🚀 Resultados e Conclusões
- Aprendizados obtidos durante o laboratório.
- Possíveis melhorias para futuras aplicações.

# ☕🔎 Explorando **Azure AI Search** com Avaliações de Café  

## 🏁 Bem-vindo ao laboratório!  
Se você já se perguntou como grandes volumes de dados podem ser organizados e pesquisados de forma eficiente, este laboratório é para você!  
Hoje, vamos usar **Azure AI Search** para transformar um conjunto de avaliações de café (**zipped coffee reviews**) em um sistema inteligente de busca.  

🔹 **Objetivo:** Minerar conhecimento das avaliações e descobrir padrões!  
🔹 **Ferramenta:** **Azure AI Search** para indexação e pesquisa eficiente.  
🔹 **Desafio:** Como podemos encontrar os cafés mais bem avaliados com apenas algumas consultas?  

---

## 🔹 1. Preparando os Dados – O Primeiro Passo  
Antes de começar a busca, precisamos organizar os dados. No conjunto fornecido pelo [Microsoft Learning](https://aka.ms/mslearn-coffee-reviews), temos centenas de avaliações com diferentes notas, marcas e descrições.  

### 🔍 Explorando os Dados  
💡 **Pergunta:** Quais informações podem ser úteis para nossa pesquisa?  
📂 **Formato:** JSON, CSV e TXT contendo detalhes dos cafés.  

### 🚀 Tarefa para você!  
Antes de subir os dados no **Azure Blob Storage**, abra o arquivo e tente responder:  
✅ Quais são os principais atributos? (Marca, origem, avaliação, comentários...)  
✅ Existe um padrão nos textos das avaliações? (Palavras repetidas, como "suave" ou "encorpado"?)  

---

## 🔹 2. Criando um Índice Inteligente – Organizando a Informação  
Agora é hora de estruturar um **índice** para organizar os dados e facilitar a busca.  

### 📌 O que precisamos no índice?  
✅ **ID do café** – Cada café precisa de um identificador único.  
✅ **Marca e Origem** – Para filtrar por região ou produtor.  
✅ **Avaliação e Comentários** – Assim descobrimos os cafés mais bem avaliados.  

### 🔧 Configurando o Índice  
Aqui está um exemplo do índice no **Azure AI Search**:  
```json
{
  "name": "coffee_reviews",
  "fields": [
    {"name": "coffee_id", "type": "Edm.String", "key": true},
    {"name": "brand", "type": "Edm.String"},
    {"name": "origin", "type": "Edm.String"},
    {"name": "rating", "type": "Edm.Double"},
    {"name": "review", "type": "Edm.String"}
  ]
}

🔹 3. Buscando Insights – Descobrindo Padrões nos Cafés
Agora que temos o índice pronto, podemos fazer consultas para descobrir os melhores cafés!

🔍 Exemplo de consulta – Buscando cafés bem avaliados
GET /indexes/coffee_reviews/docs
{
  "search": "aroma",
  "filter": "rating gt 4.5",
  "top": 5
}

💡 O que descobrimos? ✅ Os cafés bem avaliados frequentemente mencionam aromas frutados e notas de chocolate. ✅ Cafés de origem etíope aparecem entre os mais elogiados. ✅ Os termos mais comuns nas avaliações incluem "suave", "encorpado" e "adocicado".
