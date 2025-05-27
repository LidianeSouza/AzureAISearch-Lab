# 📖 Criando um Índice Inteligente – Organizando a Informação

Agora é hora de estruturar um **índice** para organizar os dados e facilitar a busca.  

## 📌 Passo 1: Criando o Serviço de Busca no Azure
1. Acesse o [Portal Azure](https://portal.azure.com).
2. Pesquise por **Azure AI Search** e clique em "Criar".
3. Escolha uma assinatura e um grupo de recursos.
4. Defina um **nome único** para o serviço.
5. Selecione um **Plano de Tarifação** adequado.
6. Clique em **Criar** e aguarde a implantação.

## 📌 Passo 2: Criando um Índice de Busca
1. Dentro do serviço **Azure AI Search**, vá até a aba **Índices**.
2. Clique em **Criar Índice** e defina um nome (ex: `coffee_reviews`).
3. Configure os **campos do índice** conforme o arquivo `config_index.json`.
4. Marque quais campos serão **pesquisáveis** (ex: `review`).
5. Salve e publique o índice.

## 📌 Passo 3: Inserindo Dados no Índice
1. Vá para a aba **Origem de Dados** e selecione **Azure Blob Storage**.
2. Configure o acesso ao armazenamento onde estão os arquivos de avaliações de café.
3. Crie um **conector** para mapear os dados ao índice `coffee_reviews`.
4. Execute a **ingestão de dados** e verifique se tudo está indexado corretamente.

## 📌 Passo 4: Testando Consultas
Agora, podemos realizar buscas dentro do índice! Exemplo de consulta para buscar cafés com avaliação acima de 4.5:

```json
GET /indexes/coffee_reviews/docs
{
  "search": "aroma",
  "filter": "rating gt 4.5",
  "top": 5
}
