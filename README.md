# 1. Identificação básica

## 1.1 Título do experimento

**Comparação Experimental entre Server-Driven UI e UI Tradicional em Aplicativos iOS: Desempenho e Experiência do Usuário**

## 1.2 ID / código

**1029366**

## 1.3 Versão do documento e histórico de revisão

**v1.0 – 21/11/2025 – Versão inicial**

## 1.4 Datas

* **Criação:** 21/11/2025
* **Última atualização:** 21/11/2025

## 1.5 Autor

**Ana Júlia Teixeira Cândido**

## 1.6 Responsável principal (PI / dono do experimento)

**Ana Júlia Teixeira Cândido**

## 1.7 Projeto / produto / iniciativa relacionada

**Trabalho de Conclusão de Curso (TCC) – Projeto de Pesquisa em Desenvolvimento Mobile – Aplicativos iOS e Arquiteturas Inovadoras**

---

# 2. Contexto e problema

## 2.1 Descrição do problema / oportunidade

O ritmo de atualização e personalização das interfaces dos aplicativos iOS é cada vez mais demandado, mas o modelo tradicional, onde toda a interface está embutida no app, torna o processo lento e pouco flexível. Nesse modelo, qualquer mudança exige nova versão, revisão da App Store e atualização pelo usuário — processos demorados e nem sempre garantidos.

A arquitetura Server-Driven UI (SDUI) promete resolver esses desafios permitindo que a interface seja modificada dinamicamente pelo backend, sem depender de atualizações completas do app. Porém, ainda permanecem dúvidas práticas sobre seu impacto em desempenho, experiência do usuário e complexidade técnica.

## 2.2 Contexto organizacional e técnico

O experimento será realizado em ambiente acadêmico, com recursos laboratoriais. Serão construídos dois protótipos equivalentes:

* **SDUI (server-driven)**
* **UI tradicional (client-driven)**

Ambos desenvolvidos em Swift com backend dedicado para o app SDUI.

## 2.3 Trabalhos e evidências prévias

* Estudos de casos de SDUI em empresas como iFood, Nubank, Spotify.
* Repositório UFMS – Explorando a arquitetura do Server Driven UI.
* Repositório Mackenzie – Aplicação de server driven UI para interfaces mobile iOS de e-commerce.

## 2.4 Referencial teórico essencial

### Arquitetura Client-Driven UI

Interface e lógica estão embutidas no app. Qualquer mudança exige nova release, aprovação e atualização pelo usuário — processo lento e pouco flexível.

### Server-Driven UI (SDUI)

Backend envia a definição da interface em tempo real (JSON, XML etc.). O app age como renderizador. Traz flexibilidade e dinamismo, mas pode introduzir latência ou problemas em redes instáveis, impactando o desempenho.

### Experiência do Usuário (UX)

Engloba satisfação, clareza, eficiência e facilidade de uso. Métricas como SUS (System Usability Scale), NPS e escalas Likert são usadas para avaliação subjetiva e padronizada.

### Desempenho

Inclui tempo de resposta, uso de recursos, número de erros e estabilidade geral. SDUI pode ser mais flexível para atualizações, contudo a dependência do servidor pode gerar impactos variáveis.

---

# 3. Objetivos e questões (Goal / Question / Metric)

## 3.1 Objetivo Geral (Goal – conforme template)

**Analyze iOS application interfaces built with Server-Driven UI and Traditional UI
for the purpose of evaluation and comparison
with respect to performance, user experience and update process
from the point of view of users, developers and decision-makers
in the context of academic prototypes developed for this experiment.**

## 3.2 Objetivos Específicos

* O1: Avaliar e comparar o desempenho das UIs SDUI e Tradicional.
* O2: Avaliar e comparar a experiência do usuário.
* O3: Comparar o processo de atualização/versionamento entre as arquiteturas.
* O4: Identificar vantagens, desvantagens e barreiras percebidas por desenvolvedores.

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
| O4       | Q4.3: SDUI melhora a flexibilidade?                        | % que confirma; Exemplos qualitativos |

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

Analisar interfaces de aplicativos móveis iOS (protótipos Server-Driven UI e UI Tradicional)
com o propósito de avaliação e comparação
com relação a desempenho, experiência do usuário e processo de atualização
do ponto de vista de usuários, desenvolvedores e tomadores de decisão
no contexto de desenvolvimento acadêmico e testes controlados com usuários.

## 4.2 Contexto do estudo

O estudo será realizado em ambiente acadêmico, utilizando laboratório universitário, com protótipos desenvolvidos por estudantes e testados por usuários recrutados com experiência básica/intermediária em iOS.

## 4.3 Premissas

* Protótipos deverão estar estáveis e funcionais.
* Backend SDUI deverá estar disponível, estável e responsivo.
* Os participantes estarão presentes nas datas combinadas.
* Todos os instrumentos e materiais serão previamente conferidos e validados.

## 4.4 Restrições

* Tempo reduzido para coleta de dados e execução dos testes.
* Limitação de dispositivos e de participantes.
* Dependência da infraestrutura de rede/laboratório disponível.
* Não utilização de apps reais ou de larga escala.

## 4.5 Limitações previstas

* Amostra pequena pode reduzir validez externa.
* Protótipos de escopo restrito e contexto simplificado.
* Perfil dos participantes representa apenas parcela dos usuários reais.

---

# 5. Stakeholders e impacto esperado

## 5.1 Stakeholders principais

* Usuários/testadores dos protótipos
* Desenvolvedores/prototipadores
* Professores e orientadores do projeto
* Tomadores de decisão acadêmicos
* Empresas/organizações interessadas em SDUI

## 5.2 Interesses e expectativas

* Usuários: obter experiência fluida e rápida.
* Desenvolvedores: entender e quantificar impactos arquiteturais.
* Professores: gerar dados empíricos confiáveis e replicáveis.
* Empresas: avaliar prós/contras da adoção de SDUI no mercado.

## 5.3 Impactos potenciais

* Geração de conhecimento prático sobre tema relevante.
* Subsídio à tomada de decisão sobre arquiteturas em projetos reais.
* Possível influência em ementas de disciplinas de desenvolvimento mobile.

---

# 6. Riscos de alto nível, premissas e critérios de sucesso

## 6.1 Riscos

* Atrasos no desenvolvimento/depuração dos protótipos.
* Instabilidade dos sistemas/acesso ao backend SDUI durante testes.
* Baixa adesão ou engajamento dos participantes.
* Problemas éticos ou logísticos que inviabilizem a coleta.

## 6.2 Critérios de sucesso (go / no-go)

* Coleta concluída de acordo com o protocolo estabelecido.
* Participação ≥ 10 usuários e ≥ 2 desenvolvedores.
* Ambos protótipos disponíveis e funcionando na íntegra para todos os participantes.

## 6.3 Critérios de parada antecipada

* Falhas graves de infraestrutura ou sistemas não solucionadas até a data de início.
* Número de participantes insuficiente para rodar a comparação.
* Bloqueios/reprovações éticas ou institucionais.

---

# 7. Modelo conceitual e hipóteses

## 7.1 Modelo conceitual do experimento

O modelo conceitual assume que o tipo de arquitetura de interface implementada em aplicativos iOS (SDUI ou tradicional) pode influenciar as respostas dos usuários e dos desenvolvedores, tanto em variáveis objetivas (desempenho técnico, recurso consumido, rapidez de atualização) quanto subjetivas (satisfação, facilidade, percepção de inovação). O principal fator manipulado é a “arquitetura da interface”, mantendo outras condições similares, permitindo avaliar, de modo sistematizado e controlado, os reais impactos dessa escolha.

## 7.2 Hipóteses formais (H0, H1)

* **H0₁ (Desempenho):** Não há diferença significativa no desempenho das interfaces SDUI e Tradicional.
  **H1₁:** Existe diferença significativa nesses indicadores.
* **H0₂ (Experiência do Usuário):** Não há diferença significativa em satisfação, facilidade de uso e fluidez percebida.
  **H1₂:** Existe diferença significativa nesses aspectos.
* **H0₃ (Processo de Atualização):** Não há diferença relevante no esforço e tempo para atualização entre as duas arquiteturas.
  **H1₃:** O SDUI apresenta diferença significativa (positiva ou negativa).

## 7.3 Nível de significância e considerações de poder

Será adotado nível de significância α = 0,05. Considerando a amostra pequena típica de experimentos acadêmicos (10–20 participantes), reconhece-se que o poder estatístico pode ser inferior a 80%. Isso será assumido como limitação e, se necessário, resultados marginais serão também discutidos com base no efeito prático e não apenas no critério estritamente estatístico.

---

# 8. Variáveis, fatores, tratamentos e objetos de estudo

## 8.1 Objetos de estudo

Os principais objetos de estudo são os protótipos equivalentes de aplicativos iOS – um utilizando SDUI e outro interface tradicional – abrangendo os módulos de UI, tarefas implementadas (cadastro, busca, compra), casos de teste simulando fluxos reais e o próprio processo operacional para publicação de modificações.

## 8.2 Sujeitos / participantes (visão geral)

Participam do estudo usuários (alunos e convidados com experiência básica/intermediária em iOS), além de desenvolvedores dos protótipos, que colaboram na etapa de atualização e respondem entrevistas sobre o esforço e desafios técnicos.

## 8.3 Variáveis independentes (fatores) e seus níveis

| Fator             | Níveis             | Descrição                                                                             |
| ----------------- | ------------------ | ------------------------------------------------------------------------------------- |
| Arquitetura da UI | SDUI / Tradicional | Interface dinâmica controlada pelo backend / Interface fixa, embarcada no app cliente |

## 8.4 Tratamentos (condições experimentais)

| Grupo | Ordem de Uso       | Descrição                                               |
| ----- | ------------------ | ------------------------------------------------------- |
| A     | SDUI → Tradicional | Participante começa pelo SDUI, depois usa o tradicional |
| B     | Tradicional → SDUI | Ordem invertida: tradicional primeiro, depois SDUI      |

## 8.5 Variáveis dependentes

| Variável                  | Descrição                       |
| ------------------------- | ------------------------------- |
| Tempo de resposta         | Tempo médio para cada ação      |
| Taxa de erros             | Proporção de falhas/erros       |
| Uso de CPU/memória        | Consumo de recursos do aparelho |
| Satisfação do usuário     | Escala Likert, NPS              |
| Usabilidade (SUS)         | Escore SUS pós-tarefa           |
| Tempo/esforço para update | Total de horas/etapas           |
| Facilidade/fluidez        | Avaliação subjetiva             |

## 8.6 Variáveis de controle / bloqueio

Serão mantidos constantes: tarefas, dispositivos, ambiente, tutorial inicial, tipo de conexão, script operacional e tempo disponível para execução.

## 8.7 Possíveis variáveis de confusão conhecidas

| Tipo         | Nome da Variável              | Descrição                     |
| ------------ | ----------------------------- | ----------------------------- |
| Independente | Arquitetura da UI             | SDUI ou Tradicional           |
| Dependente   | Tempo de resposta             | Tempo médio                   |
| Dependente   | Taxa de erros                 | Proporção de tarefas com erro |
| Dependente   | Uso de CPU/memória            | Consumo de recursos           |
| Dependente   | Satisfação/Facilidade/Fluidez | Pontuação subjetiva           |
| Dependente   | Esforço/Tempo update          | Horas/etapas                  |
| Controle     | Tutorial, ambiente, tarefas   | Condições idênticas           |
| Confusão     | Experiência prévia, motivação | Diferenças individuais        |

---

# 9. Desenho experimental

## 9.1 Tipo de desenho

O design escolhido é o crossover randomizado, no qual todos executam ambos os protótipos e a ordem inicial é sorteada. Tal formato reduz diferenças individuais e permite comparações intra-sujeito, sendo especialmente adequado para amostras reduzidas.

## 9.2 Randomização e alocação

O sorteio de ordem será feito manualmente ou por software, buscando uma distribuição homogênea entre os grupos A e B.

## 9.3 Balanceamento e contrabalanço

A divisão dos participantes entre as ordens de uso garante controle do viés de aprendizagem ou cansaço.

## 9.4 Número de grupos e sessões

Serão dois grupos (A e B). Cada participante executará duas sessões.

---

# 10. População, sujeitos e amostragem

## 10.1 População-alvo

Busca-se representar usuários reais ou potenciais de aplicativos iOS.

## 10.2 Critérios de inclusão de sujeitos

* Idade ≥ 18 anos
* Experiência mínima com iOS
* Disponibilidade
* Consentimento formal
* Ausência de impedimentos graves

## 10.3 Critérios de exclusão

* Recusa de consentimento
* Ausência não justificada
* Membro da equipe de desenvolvimento

## 10.4 Tamanho da amostra planejado

10 a 20 participantes + desenvolvedores (mínimo 2).

## 10.5 Método de seleção / recrutamento

Amostragem por conveniência.

## 10.6 Treinamento e preparação

Tutorial oral/impresso, explicação das tarefas, exemplos de perguntas.

---

# 11. Instrumentação e protocolo operacional

## 11.1 Instrumentos de coleta

* Questionários estruturados
* Escala SUS
* Logs automáticos
* Planilhas digitais
* Entrevista semiestruturada

## 11.2 Materiais de suporte

* Instruções impressas e digitais
* Slides
* Roteiro de tarefas

## 11.3 Procedimento experimental
<img width="871" height="685" alt="image" src="https://github.com/user-attachments/assets/8770549e-63ef-450d-a021-6021e7e00872" />


## 11.4 Plano de piloto

Será conduzida uma rodada piloto com dois participantes e pelo menos um desenvolvedor, visando encontrar falhas e ajustar o protocolo antes da coleta real.

---

# 12. Plano de análise de dados (pré-execução)

## 12.1 Estratégia geral de análise

Os dados serão organizados em planilhas e analisados para responder ao GQM. Serão comparadas médias, distribuições e variações entre SDUI e UI tradicional. Visualizações como boxplots e histogramas serão utilizadas.

## 12.2 Métodos estatísticos planejados

t-teste pareado; caso a normalidade não seja atendida, teste de Wilcoxon. Medidas descritivas também serão exploradas.

## 12.3 Tratamento de dados faltantes e outliers

Participantes que não concluírem ambas as etapas serão excluídos da análise. Outliers poderão ser removidos após discussão.

## 12.4 Plano de análise para dados qualitativos

As respostas abertas serão analisadas por codificação temática, agrupando categorias e triangulando com os dados quantitativos.
