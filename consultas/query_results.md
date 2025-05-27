# 🔍 Resultados das Consultas

📄 Este arquivo documenta os insights encontrados a partir das consultas feitas no Azure AI Search.

## ☕ 1. Cafés Mais Bem Avaliados

🔍 Consulta:

json
{
  "search": "Melhor café",
  "filter": "rating gt 4.5",
  "top": 5
}

✅ Os cafés melhor avaliados apresentaram notas de frutas vermelhas e chocolate em suas descrições.

✅ Marcas como Blue Mountain Coffee e Ethiopian Sidamo apareceram no topo da lista.

## 🍫 2. Cafés com Notas de Chocolate

🔍Consulta:

json
{
  "search": "Notas de chocolate",
  "filter": "review eq 'chocolate'",
  "top": 10
}

- A maioria dos cafés mencionando chocolate vieram de origens sul-americanas. 
- Palavras associadas frequentemente: "encorpado", "cremoso", "aveludado".

## 🌍 3. Cafés de Origem Etíope

🔍 Consulta:

json
{
  "search": "Cafés de origem etíope",
  "filter": "origin eq 'Ethiopia'",
  "top": 5
}

- Os cafés etíopes geralmente possuem notas florais e cítricas. 
- Origem mais comum nos cafés premium do conjunto de dados.

## 📌 Conclusão 

A indexação no Azure AI Search permitiu identificar padrões interessantes sobre cafés, incluindo:
- ☕ Os mais bem avaliados 
- 🍫 Características de sabor
- 🌍 Tendências por origem 

🔎 Essas análises podem ser ampliadas com novos filtros e técnicas de busca!
