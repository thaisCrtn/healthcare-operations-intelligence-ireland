# Healthcare Operations Intelligence Ireland

**Análise de Home Care, Nursing Homes, Cuidadores Familiares e Políticas Públicas na Irlanda**

- **Status do projeto:** Em desenvolvimento
- **País:** Irlanda
- **Período de análise:** A definir

---

## 1. Visão geral do projeto

Este projeto investiga o sistema de cuidados de longa duração da Irlanda, com foco em três grupos principais:

- Pessoas que recebem cuidados domiciliares (Home Care).
- Pessoas que residem em instituições de cuidados de longa duração (Nursing Homes).
- Cuidadores familiares não remunerados (Unpaid Family Carers).

O objetivo é compreender como os serviços estão distribuídos, como a demanda está evoluindo e quais desafios afetam as pessoas que recebem e prestam cuidados.

As políticas governamentais, o financiamento público e a regulamentação serão considerados como dimensões transversais da análise.

O projeto utiliza dados públicos e aplica metodologias de Análise de Dados, incluindo coleta, limpeza, análise exploratória, estatística descritiva, consultas SQL e visualização de dados.

## 2. Pergunta central da pesquisa

**Como o sistema de cuidados de longa duração da Irlanda responde ao crescimento da demanda por meio de Home Care, Nursing Homes e cuidados familiares não remunerados?**

### 2.1 Pergunta específica — Home Care

A oferta de Home Support está acompanhando as mudanças na demanda por cuidados na Irlanda?

### 2.2 Perguntas complementares

- Como evoluiu a quantidade de horas de Home Support disponibilizadas?
- Como mudou o número de pessoas aguardando atendimento?
- Existem diferenças entre pessoas aguardando um novo pacote e pessoas aguardando horas adicionais?
- Como a população idosa está evoluindo nas diferentes faixas etárias?
- Existe associação entre envelhecimento populacional, independência funcional e indicadores de Home Support?

## 3. Escopo do projeto

O projeto está organizado em cinco áreas de análise:

1. Operações de Home Care.
2. Inteligência sobre Nursing Homes.
3. Cuidadores familiares não remunerados.
4. Demanda por cuidados de longa duração e demografia.
5. Saúde e bem-estar dos cuidadores.

Políticas governamentais, financiamento e regulamentação serão investigados como uma dimensão transversal.

## 4. Fontes de dados

O projeto priorizará fontes oficiais da Irlanda, incluindo:

- Health Service Executive (HSE).
- Central Statistics Office (CSO).
- Health Information and Quality Authority (HIQA).
- Department of Health.
- National Treatment Purchase Fund (NTPF), quando relevante.

Cada conjunto de dados será documentado em `data_sources.md`, incluindo instituição responsável, data de publicação, período, indicadores, formato e limitações conhecidas.

## 5. Metodologia

O projeto seguirá as seguintes etapas:

1. Compreensão do problema.
2. Coleta de dados.
3. Limpeza e preparação dos dados.
4. Análise exploratória de dados (EDA).
5. Análise estatística e descritiva.
6. Análise utilizando SQL.
7. Visualização de dados.
8. Interpretação dos resultados e recomendações.

## 6. Análise de Home Care

### 6.1 Dados iniciais

A investigação inicial utiliza as respostas parlamentares do HSE PQ 15085/26 e PQ 15086/26, publicadas em 6 de março de 2026.

O documento apresenta dados mensais de janeiro a dezembro de 2025.

Indicadores disponíveis:

- Pessoas aguardando um novo pacote de Home Support.
- Pessoas aguardando horas adicionais de Home Support.
- Horas diretas de Home Support entregues.
- Horas indiretas de Home Support entregues.

### 6.2 Resultados preliminares

Entre janeiro e dezembro de 2025:

- O total de pessoas aguardando atendimento aumentou de 4.805 para 5.600, aproximadamente 16,5%.
- O total de horas entregues aumentou de 2.052.567 para 2.221.377, aproximadamente 8,2%.
- As horas diretas diminuíram aproximadamente 5,1%.
- As horas indiretas aumentaram aproximadamente 15,2%.

Essas comparações são preliminares e representam os valores de dois meses específicos. Não devem ser interpretadas isoladamente como explicação completa da demanda ou do desempenho anual do serviço.

### 6.3 Interpretação inicial

O aumento das horas de Home Support, acompanhado pelo crescimento da lista de espera, sugere que a expansão da oferta pode não estar acompanhando o crescimento da demanda registrada.

Será necessário investigar outros fatores para compreender esse comportamento.

### 6.4 Limitações dos dados

- A lista de espera está disponível por região de saúde.
- As horas entregues no documento selecionado estão apresentadas em nível nacional.
- A lista de espera não representa todas as pessoas que podem precisar de cuidados.
- O documento não apresenta o tempo individual de espera.
- Não há informação sobre a quantidade total de horas necessárias, mas não entregues.

## 7. Análise demográfica e independência funcional

### 7.1 Objetivo

Investigar se as mudanças na composição etária e no nível de independência funcional da população idosa estão associadas às mudanças na oferta e na demanda registrada por Home Support.

### 7.2 Faixas etárias

A análise considerará inicialmente:

- 65 a 74 anos.
- 75 a 84 anos.
- 85 anos ou mais.

As faixas serão comparadas ao longo do tempo, conforme a disponibilidade e a consistência dos dados.

### 7.2.1 Crescimento populacional e necessidade de cuidados de longa duração

A análise dos dados do Central Statistics Office (CSO), referentes ao período de 2020 a 2025, demonstra um crescimento nas três faixas etárias estudadas. O aumento mais expressivo ocorreu entre a população com 85 anos ou mais, que cresceu aproximadamente 27% no período.

Esse crescimento pode indicar uma expansão da demanda potencial por serviços de cuidados de longa duração (*Long-Term Care*), incluindo Home Support e Nursing Homes.

Entretanto, é importante destacar que a idade, isoladamente, não determina a necessidade de cuidados. Pessoas com a mesma idade podem apresentar níveis muito diferentes de independência funcional e capacidade para realizar atividades cotidianas.

Portanto, o envelhecimento populacional deve ser considerado um indicador demográfico relevante, mas não suficiente para estimar a necessidade efetiva de cuidados.

**Próxima etapa da análise:** investigar indicadores de independência funcional para compreender melhor a relação entre envelhecimento, capacidade de realizar atividades diárias e necessidade de serviços de cuidados de longa duração.

### 7.3 Independência funcional

A idade, isoladamente, não determina a necessidade de Home Support.

Duas pessoas da mesma faixa etária podem apresentar níveis muito diferentes de independência e necessidade de assistência.

Por isso, será investigada a disponibilidade de indicadores relacionados à capacidade de realizar atividades da vida diária, como:

- Tomar banho.
- Vestir-se.
- Alimentar-se.
- Preparar refeições.
- Caminhar e se locomover.
- Realizar atividades domésticas.

Esses indicadores poderão ajudar a compreender melhor a necessidade potencial de cuidados.

### 7.4 Indicadores propostos

- População por faixa etária.
- Variação percentual de cada faixa etária.
- Indicadores de limitações funcionais, caso disponíveis.
- Horas de Home Support por pessoa da população com 65 anos ou mais.
- Horas de Home Support por pessoa em cada faixa etária, se os dados forem compatíveis.

### 7.5 Considerações analíticas

O indicador de horas de Home Support por pessoa idosa representa uma relação entre a oferta de serviços e o tamanho da população. Não representa a quantidade de horas recebidas individualmente por cada pessoa.

A análise de independência funcional também dependerá da disponibilidade de dados públicos compatíveis.

Qualquer relação identificada entre idade, independência funcional e Home Support será interpretada como associação, e não como prova de causalidade.

## 8. Análise de Nursing Homes

A desenvolver após a avaliação das fontes e da disponibilidade dos dados.

## 9. Análise de cuidadores familiares não remunerados

A desenvolver após a avaliação das fontes e da disponibilidade dos dados.

## 10. Saúde e bem-estar dos cuidadores

A desenvolver após a avaliação das fontes e da disponibilidade dos dados.

## 11. Políticas públicas, financiamento e regulamentação

A desenvolver como dimensão transversal das cinco áreas de análise.

## 12. Resultados finais e recomendações

A preencher após a conclusão das análises.

## 13. Limitações gerais do projeto

Serão documentadas as limitações relacionadas à disponibilidade dos dados, diferenças de definição, cobertura geográfica, períodos, valores ausentes e comparabilidade entre fontes.

## 14. Conclusão

A preencher após a conclusão das investigações.

## 15. Referências

- Health Service Executive (HSE). Parliamentary Questions PQ 15085/26 e PQ 15086/26. Publicadas em 6 de março de 2026.
- Outras fontes oficiais serão adicionadas ao longo do projeto.