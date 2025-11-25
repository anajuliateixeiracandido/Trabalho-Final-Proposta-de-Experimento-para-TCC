# 1. Identificação básica

## 1.1 Título do experimento

**Comparação Experimental entre Server-Driven UI e UI Tradicional em Aplicativos iOS: Desempenho e Experiência do Usuário**

## 1.2 ID / código

**1029366**

## 1.3 Versão do documento e histórico de revisão

* **v1.0 – 21/11/2025** – Versão inicial

## 1.4 Datas

* **Criação:** 21/11/2025
* **Última atualização:** 21/11/2025

## 1.5 Autor

* Ana Júlia Teixeira Cândido

## 1.6 Responsável principal (PI / dono do experimento)

* Ana Júlia Teixeira Cândido

## 1.7 Projeto / produto / iniciativa relacionada

**Trabalho de Conclusão de Curso (TCC)** – Projeto de Pesquisa em Desenvolvimento Mobile – Aplicativos iOS e Arquiteturas Inovadoras

---

# 2. Contexto e problema

## 2.1 Descrição do problema / oportunidade

O ritmo de atualização e personalização das interfaces dos aplicativos iOS é cada vez mais demandado, mas o modelo tradicional, onde toda a interface está embutida no app, torna o processo lento e pouco flexível. Nesse modelo, qualquer mudança exige nova versão, revisão da App Store e atualização pelo usuário — processos demorados e nem sempre garantidos.

A arquitetura **Server-Driven UI (SDUI)** promete resolver esses desafios permitindo que a interface seja modificada dinamicamente pelo backend, sem depender de atualizações completas do app. Porém, ainda há dúvidas práticas sobre seu impacto em desempenho, experiência do usuário e complexidade técnica.

## 2.2 Contexto organizacional e técnico

O experimento será realizado em ambiente acadêmico. Serão construídos dois protótipos equivalentes:

* **SDUI (server-driven)**
* **UI tradicional (client-driven)**

Ambos feitos em Swift com backend dedicado ao SDUI.

## 2.3 Trabalhos e evidências prévias

* Estudos de casos de SDUI em empresas como *iFood*, *Nubank*, *Spotify*
* Repositório UFMS – *Explorando a arquitetura do Server Driven UI*
* Repositório Mackenzie – *Aplicação de server driven UI para interfaces mobile iOS de e-commerce*

## 2.4 Referencial teórico essencial

### Arquitetura Client-Driven UI

Interface e lógica estão embutidas no app. Qualquer mudança exige nova release, aprovação e atualização pelo usuário — processo lento e pouco flexível.

### Server-Driven UI (SDUI)

Backend envia a definição da interface em tempo real (JSON, XML etc.). O app age como renderizador. Traz flexibilidade, mas pode introduzir latência ou problemas em redes ruins.

### Experiência do Usuário (UX)

Inclui aspectos subjetivos e objetivos (satisfação, clareza, eficiência). Pode ser avaliada por métricas e escalas como **SUS**.

### Desempenho

Envolve tempo de resposta, uso de recursos, erros e estabilidade. SDUI pode ser mais flexível, mas depender do servidor pode gerar impactos variáveis.

---

# 3. Objetivos e questões (Goal / Question / Metric)

## 3.1 Objetivo Geral (Goal – conforme template)

**Analyze** iOS application interfaces built with Server-Driven UI and Traditional UI
**for the purpose of** evaluation and comparison
**with respect to** performance, user experience and update process
**from the point of view of** users, developers and decision-makers
**in the context of** academic prototypes developed for this experiment.

## 3.2 Objetivos Específicos

* **O1:** Avaliar e comparar o desempenho das UIs SDUI e Tradicional.
* **O2:** Avaliar e comparar a experiência do usuário.
* **O3:** Comparar o processo de atualização/versionamento entre as arquiteturas.
* **O4:** Identificar vantagens, desvantagens e barreiras percebidas por desenvolvedores.

## 3.3 Tabela GQM

| Objetivo | Pergunta (Q)                                               | Métrica                               |
| -------- | ---------------------------------------------------------- | ------------------------------------- |
| O1       | Q1.1: Qual o tempo médio de resposta das interfaces?       | Tempo de resposta (ms); Desvio padrão |
| O1       | Q1.2: Qual a taxa de erros/exceções?                       | Taxa de erros (%); Nº de erros        |
| O1       | Q1.3: Qual o consumo de recursos?                          | CPU (%); Memória (MB)                 |
| O2       | Q2.1: Qual o nível de satisfação dos usuários?             | Likert (1–5); NPS                     |
| O2       | Q2.2: Qual a percepção de facilidade de uso?               | SUS; Tempo para tarefas               |
| O2       | Q2.3: Diferença percebida de fluidez?                      | Likert (1–5); Interrupções            |
| O3       | Q3.1: Tempo total para atualizar a UI em cada arquitetura? | Horas/dias; Taxa de adesão            |
| O3       | Q3.2: Esforço dos devs para modificar a UI?                | Horas; Nº de etapas                   |
| O3       | Q3.3: Percentual de usuários atualizados?                  | % usuários; Nº de versões simultâneas |
| O4       | Q4.1: Vantagens percebidas pelos devs?                     | Frequência de temas; Likert           |
| O4       | Q4.2: Barreiras técnicas encontradas?                      | Nº de barreiras; Dificuldade (1–5)    |
| O4       | Q4.3: SDUI melhora a flexibilidade?                        | % que confirma; Exs qualitativos      |

## 3.4 Tabela Descritiva das Métricas

| Métrica                   | Descrição                        | Unidade     |
| ------------------------- | -------------------------------- | ----------- |
| Tempo de resposta         | Tempo médio por ação             | ms          |
| Desvio padrão             | Variação dos tempos              | ms          |
| Taxa de erros             | Proporção de erros               | %           |
| Nº absoluto de erros      | Total de erros                   | Contagem    |
| Uso de CPU                | Uso do processador               | %           |
| Uso de memória            | Memória consumida                | MB          |
| Satisfação pós-tarefa     | Avaliação do usuário             | Likert 1–5  |
| NPS                       | Net Promoter Score               | –100 a +100 |
| SUS                       | Avaliação de usabilidade padrão  | 0–100       |
| Tempo para tarefa         | Duração da tarefa                | min         |
| Avaliação de fluidez      | Percepção de fluidez             | Likert 1–5  |
| Interrupções              | Travamentos ou falhas            | Contagem    |
| Tempo de rollout          | Tempo até a UI chegar ao usuário | h/dias      |
| Taxa de adesão            | Usuários com UI atualizada       | %           |
| Esforço em horas          | Esforço dos devs                 | h           |
| Nº de etapas              | Passos para concluir alteração   | Contagem    |
| % de usuários atualizados | Cobertura da nova UI             | %           |
| Nº de versões simultâneas | Fragmentação pós-update          | Contagem    |
| Frequência de menções     | Citações em entrevistas          | Contagem    |
| Escala de concordância    | Concordância com afirmativas     | Likert 1–5  |
| Nº de barreiras           | Problemas relatados              | Contagem    |
| Dificuldade média         | Grau médio de dificuldade        | Likert 1–5  |
| % que confirma ganho      | Percepção de flexibilidade       | %           |
| Exemplos qualitativos     | Evidências textuais              | Texto       |

---

# 4. Escopo e contexto do experimento

## 4.1 Escopo funcional / de processo

### Incluído

* Análise e comparação de dois protótipos iOS (SDUI e Tradicional).
* Execução de tarefas usuais pelos participantes.
* Coletas objetivas e subjetivas (UX, desempenho etc.).
* Avaliação do processo de atualização das UIs.
* Entrevistas com desenvolvedores.

### Excluído

* Aplicativos reais de produção.
* Análise em escala industrial.
* Métricas de longo prazo (retenção, conversão etc.).

### Template 

*Analisar interfaces de aplicativos móveis iOS (protótipos Server-Driven UI e UI Tradicional)
com o propósito de avaliação e comparação
com relação a desempenho, experiência do usuário e processo de atualização
do ponto de vista de usuários, desenvolvedores e tomadores de decisão
no contexto de desenvolvimento acadêmico e testes controlados com usuários.*

## 4.2 Contexto do estudo

Estudo em ambiente acadêmico, com protótipos desenvolvidos por estudantes e testados por usuários com experiência básica em iOS, em laboratório controlado.

## 4.3 Premissas

* Protótipos estáveis.
* Backend SDUI disponível.
* Participantes presentes e instrumentos validados.

## 4.4 Restrições

* Tempo reduzido.
* Poucos devices e participantes.
* Dependência de infraestrutura de rede e laboratório.
* Sem integração com apps reais.

## 4.5 Limitações previstas

* Baixa amostra reduz validez externa.
* Protótipos simples.
* Perfil limitado dos usuários.

---

# 5. Stakeholders e impacto esperado

## 5.1 Stakeholders principais

* Usuários/testadores
* Desenvolvedores
* Professores orientadores
* Tomadores de decisão acadêmicos
* Empresas potenciais interessadas

## 5.2 Interesses e expectativas

* **Usuários:** usabilidade e rapidez
* **Desenvolvedores:** entender impactos técnicos
* **Professores:** resultados confiáveis para pesquisa
* **Empresas:** evidências práticas sobre SDUI

## 5.3 Impactos potenciais

* Geração de conhecimento aplicável
* Influência na escolha de arquitetura
* Possível impacto em cronogramas acadêmicos

---

# 6. Riscos de alto nível, premissas e critérios de sucesso

## 6.1 Riscos

* Atrasos no desenvolvimento
* Instabilidade dos protótipos
* Falta de engajamento dos participantes
* Problemas no backend SDUI

## 6.2 Critérios de sucesso (go / no-go)

* Coleta concluída conforme protocolo
* Mínimo 10 usuários e 2 desenvolvedores
* Protótipos disponíveis durante todo o experimento

## 6.3 Critérios de parada antecipada

* Falha grave de infraestrutura
* Número insuficiente de participantes
* Impedimentos institucionais ou éticos
