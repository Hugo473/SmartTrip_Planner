# ✈️ SmartTrip Planner – Planejador Inteligente de Viagens com IA

O **SmartTrip Planner** é um sistema inteligente que utiliza agentes autônomos com IA (baseados no Gemini da Google) para ajudar usuários a planejarem roteiros de viagem personalizados, com base nas datas e destino informados. 

Ele é capaz de:

- 🔍 Buscar passeios e atrações atualizadas com o Google Search
- 📍 Sugerir hospedagens populares com preços e localização
- 🛫 Indicar o aeroporto mais próximo (caso a cidade não tenha)
- 🧭 Criar roteiros otimizados por dia, considerando logística e variedade
- ✍️ Redigir um resumo final narrativo para o viajante
- 💰 Apresentar estimativas de gastos com passeios, alimentação e transporte

---

## 🚀 Tecnologias utilizadas

- Python 3.11+
- Google Generative AI (Gemini)
- Google ADK (Agent Developer Kit)
- IPython / Google Colab
- Pandas (para visualização opcional)
- Markdown para visualização no notebook

---

## 🧠 Arquitetura de Agentes

| Agente           | Função                                                                 |
|------------------|------------------------------------------------------------------------|
| `agente_buscador`     | Pesquisa atrações, hospedagens e aeroporto mais próximo usando Google Search |
| `agente_planejador`   | Organiza as atrações em um roteiro diário otimizado                |
| `agente_redator`      | Redige um texto final personalizado com narrativa inspiradora       |

---

## 🖼️ Exemplo de Execução

```python
destino = "Gramado"
data_inicio = "01/12/2025"
data_fim = "07/12/2025"

lancamentos_buscados = agente_buscador(destino, data_inicio, data_fim)
plano_de_post = agente_planejador(destino, data_inicio, data_fim, lancamentos_buscados)
rascunho_de_post = agente_redator(destino, data_inicio, data_fim, plano_de_post)
# SmartTrip_Planner
