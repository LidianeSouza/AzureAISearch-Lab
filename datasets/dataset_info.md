# 📊 Informações sobre o Conjunto de Dados - Coffee Reviews  

## 📌 Origem dos Dados  
Os dados utilizados neste laboratório foram fornecidos pelo **Microsoft Learning** e podem ser acessados no seguinte link:  
[Zipped Coffee Reviews Dataset](https://aka.ms/mslearn-coffee-reviews)  

Este conjunto de dados contém avaliações de cafés, incluindo informações como:  
✅ **Marca do café**  
✅ **Origem (país ou região)**  
✅ **Nota média dada pelos consumidores**  
✅ **Comentários detalhados sobre aroma, sabor e corpo**  

## 📂 Estrutura dos Dados  
Os arquivos estão disponíveis nos formatos **JSON** e **CSV**, permitindo a ingestão e análise no **Azure AI Search**.  
Exemplo de estrutura de um registro no conjunto de dados:  

```json
{
  "coffee_id": "12345",
  "brand": "Blue Mountain Coffee",
  "origin": "Jamaica",
  "rating": 4.8,
  "review": "Aroma incrível, notas de chocolate e final suave."
}

