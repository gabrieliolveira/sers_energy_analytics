**CP4 de SERS**

TURMA: 1CCPO

Integrantes:

Carlos Eduardo Affonso - RM 569676

Gabriel Oliveira Gusmão Florêncio dos Santos - RM 573747

Gustavo de Souza Abreu - RM 574080

Gabrieli de Lima Pettena de Oliveira - RM 569799

Igor Massone Monteiro - RM 573853

Temitope Kuku da Silva Ogunbanjo - RM 573772


# Análise de Dados de Carga Elétrica com API do ONS

##  Descrição da Atividade
Este projeto consiste na realização de um estudo prático de análise de dados aplicados ao setor elétrico brasileiro, desenvolvido para a disciplina de **Soluções em Energias Renováveis e Sustentáveis** do curso de **Ciência da Computação**.

O objetivo principal é avaliar o comportamento e a variabilidade da carga elétrica registrada no Sistema Interligado Nacional (SIN), especificamente na área de carga **SP (São Paulo)**. A atividade abrange desde o consumo automatizado de dados via API pública até a limpeza, transformação, cálculo de indicadores operacionais, geração de visualizações gráficas e síntese de um relatório técnico com suporte de Inteligência Artificial.

---

##  Etapas do Projeto

1. **Consulta à API e Extração dos Dados:** Obtenção dos registros semi-horários de carga verificada.
2. **Construção e Inspeção do DataFrame:** Mapeamento de colunas, identificação de tipos de dados e estruturação inicial.
3. **Tratamento e Organização:** Renomeação de atributos, verificação de valores nulos e padronização das colunas de data/hora (`datetime`) e carga (`numeric`).
4. **Cálculo de Indicadores:** Apuração de carga mínima, máxima (pico), média, mediana e amplitude.
5. **Análise por Recortes e Filtros:**
   - **Alta Demanda:** Registros com carga superior a 90% do valor máximo.
   - **Segundo Critério:** Registros com carga operando acima da média semanal.
6. **Visualização de Dados:** Construção de gráficos de séries temporais e distribuição do perfil de consumo.
7. **Relatório Técnico & Validação Crítica:** Elaboração de um parecer sintético validado criticamente para evitar falsas causalidades ou inferências sem respaldo nos dados.

---

##  Fonte dos Dados Analisados

Os dados utilizados neste projeto foram obtidos diretamente da API pública mantida pelo **Operador Nacional do Sistema Elétrico (ONS)**.

- **Portal de Dados Abertos do ONS:** [dados.ons.org.br](https://dados.ons.org.br/)
- **Conjunto de Dados:** Carga de Energia Verificada
- **Endpoint da API Utilizado:** `https://apicarga.ons.org.br/prd/cargaverificada`
- **Recorte Analisado:**
  - **Área de Carga:** `SP` (São Paulo)
  - **Período de Análise:** `01/08/2025` a `07/08/2025`
  - **Frequência da Medição:** Intervalos semi-horários (30 em 30 minutos)

---

##  Tecnologias e Bibliotecas Utilizadas

- **Linguagem:** Python 3
- **Manipulação e Análise de Dados:** `pandas`
- **Requisições HTTP / API:** `requests`
- **Visualização de Dados:** `matplotlib`, `seaborn`
- **Inteligência Artificial (Geração do Relatório):** `google-genai` (API Gemini)
- **Ambiente de Desenvolvimento:** Google Colab
