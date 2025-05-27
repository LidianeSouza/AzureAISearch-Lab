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
