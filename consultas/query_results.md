# 🔍 Resultados das Consultas

📄 Este arquivo documenta os insights encontrados a partir das consultas feitas no Azure AI Search.

- ☕ Pesquisa por avaliações positivas de café
- ⭐ Filtragem por classificações acima de 4 estrelas
- 📍 Localização dos cafés mais bem avaliados
- 🏷️ Busca por cafés com palavras-chave específicas
- ⏳ Ordenação por data das avaliações mais recentes

## ☕ 1. Cafés Mais Bem Avaliados

🔍 Consulta:

```json
{
  "search": "Melhor café",
  "filter": "rating gt 4.5",
  "top": 5
}
```
✅ Os cafés melhor avaliados apresentaram notas de frutas vermelhas e chocolate em suas descrições.

✅ Marcas como Blue Mountain Coffee e Ethiopian Sidamo apareceram no topo da lista.

## 🍫 2. Cafés com Notas de Chocolate

🔍Consulta:

```json
{
  "search": "Notas de chocolate",
  "filter": "review eq 'chocolate'",
  "top": 10
}
```

- A maioria dos cafés mencionando chocolate vieram de origens sul-americanas. 
- Palavras associadas frequentemente: "encorpado", "cremoso", "aveludado".

## 🌍 3. Cafés de Origem Etíope

🔍 Consulta:

```json
{
  "search": "Cafés de origem etíope",
  "filter": "origin eq 'Ethiopia'",
  "top": 5
}
```

- Os cafés etíopes geralmente possuem notas florais e cítricas. 
- Origem mais comum nos cafés premium do conjunto de dados.

## 📌 Conclusão 

A indexação no Azure AI Search permitiu identificar padrões interessantes sobre cafés, incluindo:

### 🔎 **Descobertas Chave**  
- ☕ **Os cafés mais bem avaliados** – Identificamos quais características contribuem para altas avaliações.  
- 🍫 **Perfis de sabor preferidos (características de sabor)** – Descobrimos notas sensoriais mais apreciadas pelos consumidores.  
- 🌍 **Tendências por origem** – Mapear padrões regionais ajuda a entender preferências culturais no consumo de café.  

Com a aplicação de filtros avançados e técnicas de pesquisa refinadas, podemos expandir essas análises para auxiliar produtores, cafeterias e até plataformas de e-commerce a oferecerem recomendações personalizadas.  

