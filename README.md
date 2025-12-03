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


Tempo de rollout:

Tempo decorrido entre a liberação/push da atualização de interface no backend e a disponibilização ao usuário final no aplicativo. No SDUI, o rollout é esperado como imediato; no tradicional, dependerá do processo de aprovação e atualização via App Store.

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

Destaca-se que, para o objetivo de desempenho, a principal variável observada será o tempo de resposta; para experiência do usuário, o principal indicador será o escore SUS (System Usability Scale).

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
O contrabalanceamento será obtido dividindo a amostra de modo que metade dos participantes execute primeiro o app SDUI e metade o Tradicional, mitigando o efeito de ordem (order effect) no experimento.

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
Além da análise global dos resultados, as métricas serão avaliadas separadamente por ordem de execução (SDUI primeiro/tradicional primeiro), de modo a identificar eventuais efeitos de aprendizagem ou fadiga ao longo das sessões.

## 12.2 Métodos estatísticos planejados

t-teste pareado; caso a normalidade não seja atendida, teste de Wilcoxon. Medidas descritivas também serão exploradas.

## 12.3 Tratamento de dados faltantes e outliers

Participantes que não concluírem ambas as etapas serão excluídos da análise. Outliers poderão ser removidos após discussão.

## 12.4 Plano de análise para dados qualitativos

As respostas abertas serão analisadas por codificação temática, agrupando categorias e triangulando com os dados quantitativos.
As evidências qualitativas, ao confirmarem, complementarem ou desafiarem os achados quantitativos, serão usadas para fortalecer as interpretações, contextualizar as descobertas e propor hipóteses para estudos futuros.

# 13. Avaliação de validade (ameaças e mitigação)

## 13.1 Validade de conclusão

As principais ameaças à validade de conclusão incluem:

* **Baixo poder estatístico:** devido ao tamanho limitado da amostra, pode ser difícil detectar efeitos reais.
  **Mitigação:** adoção de um desenho crossover intra-sujeito para maximizar a sensibilidade, e uso de análise descritiva complementar.
* **Violação de suposições estatísticas:** testes paramétricos, como o t-teste, exigem normalidade dos dados.
  **Mitigação:** aplicação de testes de normalidade (Shapiro-Wilk); caso as premissas não sejam atendidas, uso de testes não paramétricos (Wilcoxon).
* **Erros de medição:** inconsistências nos logs automáticos ou respostas imprecisas nos questionários.
  **Mitigação:** instrumentos revisados no piloto, instruções padronizadas e dupla checagem dos dados coletados.

## 13.2 Validade interna

Podem ocorrer ameaças como:

* **History:** eventos externos durante as sessões de teste que afetem o desempenho.
  **Mitigação:** realização dos testes em ambiente controlado e instrução para evitar distrações.
* **Maturation:** cansaço, tédio ou aprendizado dos participantes.
  **Mitigação:** sessões curtas, pausas obrigatórias entre testes e randomização da ordem dos aplicativos.
* **Selection:** características prévias dos participantes interferindo nos resultados.
  **Mitigação:** amostra homogênea quanto ao perfil, critérios claros de inclusão/exclusão e sorteio para ordem dos grupos.
* **Instrumentation:** qualquer mudança nos instrumentos durante a coleta.
  **Mitigação:** instrumentos e protocolo padronizados, não alterados após início da coleta.

## 13.3 Validade de constructo

Existe o risco de as métricas utilizadas não refletirem o que se pretende medir:

* **Medidas subjetivas de satisfação e usabilidade:** podem ser influenciadas por expectativas ou experiências anteriores.
  **Mitigação:** utilização de escalas validadas (SUS, NPS, Likert) e aplicação após cada uso, com instruções claras para interpretação das perguntas.
* **Medidas objetivas de desempenho:** uso exclusivo dos logs automáticos para reduzir erro humano, revisão dos dados em amostra do piloto.
* **Esforço de desenvolvimento:** entrevistas com roteiro padronizado para evitar ambiguidades.

## 13.4 Validade externa

A generalização dos resultados é limitada devido ao contexto:

* **Contexto acadêmico:** os participantes são majoritariamente estudantes e usuários não avançados que podem não representar o público geral de apps iOS.
  **Mitigação:** delimitação clara deste escopo nos resultados.
* **Protótipos simplificados:** funcionalidades reduzidas podem não captar toda a complexidade de um app real.
* **Ambiente controlado:** laboratório difere de uso cotidiano.
  **Mitigação:** descrição transparente do contexto e recomendação de replicação em cenários reais.

## 13.5 Resumo das principais ameaças e estratégias de mitigação

| Tipo       | Ameaça                         | Mitigação                                                   |
| ---------- | ------------------------------ | ----------------------------------------------------------- |
| Conclusão  | Baixa amostra, erro de medição | Crossover, revisão de instrumentos, análise descritiva      |
| Interna    | Maturation, History, Selection | Randomização ordem, pausas, critérios claros                |
| Constructo | Métricas inadequadas           | Escalas validadas, logs automatizados                       |
| Externa    | Contexto acadêmico, protótipo  | Relato do escopo nos resultados, recomendação de replicação |

---

# 14. Ética, privacidade e conformidade

## 14.1 Questões éticas (uso de sujeitos, incentivos, etc.)

Não haverá pressão para participação: todos os participantes serão voluntários, podendo desistir a qualquer momento, sem prejuízo. Serão evitados incentivos financeiros – se houver, será para ressarcimento simbólico. O uso predominante de estudantes requer cuidado para que não haja coerção por parte de professores ou avaliação atrelada à participação. O risco de exposição é mínimo, pois os dados não conterão identificação pessoal além das informações básicas de perfil.

## 14.2 Consentimento informado

Todos os participantes irão receber, antes do início, informações claras sobre o objetivo, procedimentos, eventuais riscos e benefícios do experimento. O aceite será registrado por meio de assinatura de termo de consentimento livre e esclarecido, assegurando direito à desistência em qualquer etapa, conforme determinado pelas normas éticas universitárias.

## 14.3 Privacidade e proteção de dados

Serão coletadas apenas informações mínimas: faixa etária, nível de experiência em iOS, respostas a questionários e logs de uso dos apps/protótipos. Não será solicitado nome, matrícula ou informações sensíveis. Os dados serão anonimizados – cada sujeito e cada log receberão um código identificador. O acesso será restrito aos pesquisadores responsáveis e orientador. Os dados serão mantidos pelo tempo necessário à análise e defesa do TCC e, após isso, descartados de forma segura.

## 14.4 Aprovações necessárias

O projeto será submetido à aprovação do orientador e, se exigido, à Comissão de Ética em Pesquisa da instituição (CEP). No momento, encontra-se em etapa de elaboração inicial aguardando parecer do orientador responsável.

---

# 15. Recursos, infraestrutura e orçamento

## 15.1 Recursos humanos e papéis

* Autor do TCC: planejamento, condução do experimento, coleta e análise dos dados.
* Orientador: supervisão metodológica e ética, revisão do plano e dos materiais.
* Desenvolvedores (caso haja contribuição extra): adaptação dos protótipos para coleta de métricas, suporte técnico durante a operação.

## 15.2 Infraestrutura técnica necessária

* Sala de laboratório com dispositivos iOS (iPhones/iPads) disponíveis.
* Ambiente de rede estável para acesso ao backend.
* Computador para registro, backup dos dados e operação dos questionários.
* Servidor/backend SDUI dedicado (pode ser local ou remoto).
* Repositório em nuvem para armazenamento temporário dos dados.

## 15.3 Materiais e insumos

* Protótipos dos aplicativos finalizados e testados.
* Questionários impressos e/ou em Google Forms.
* Termos de consentimento impressos.
* Apostilas de orientação rápida, slides explicativos.
* Canetas/lápis, pranchetas ou notebooks/tablets para anotação dos participantes.

## 15.4 Orçamento e custos estimados

* Equipamentos: provavelmente fornecidos pela universidade.
* Impressão de materiais: estimativa de até R$100.
* Hospedagem do backend: uso de serviços gratuitos/acadêmicos.
* **Total: até R$200**, a serem custeados pela autora do TCC, sem fontes externas previstas.

---

# 16. Cronograma, marcos e riscos operacionais

## 16.1 Macrocronograma (até o início da execução)

| Etapa                                | Data prevista |
| ------------------------------------ | ------------- |
| Conclusão do plano                   | 05/12/2025    |
| Aprovação e ajustes                  | 08/12/2025    |
| Desenvolvimento final dos protótipos | 15/12/2025    |
| Execução do piloto                   | 17/12/2025    |
| Coleta principal                     | 20–22/12/2025 |
| Análise e redação                    | 23–30/12/2025 |

## 16.2 Dependências entre atividades

* Execução do piloto depende do término dos protótipos e do plano aprovado.
* Treinamento dos participantes depende do agendamento da coleta.
* Coleta principal ocorre somente após ajustes pós-piloto e treinamento.

## 16.3 Riscos operacionais e plano de contingência

* Baixa participação: ampliar o recrutamento, buscar outros cursos.
* Instabilidade dos protótipos ou backend: preparação de backups dos protótipos e plano B de rede local.
* Doença ou indisponibilidade dos envolvidos: marcar datas alternativas e dividir tarefas entre orientador e autora.

---

# 17. Governança do experimento

## 17.1 Papéis e responsabilidades formais

* Autora (PI): responsável pelo planejamento, execução, registro, análise dos dados, e redação do relatório.
* Orientador: apoia nos aspectos éticos, metodológicos e valida as etapas.
* Desenvolvedores auxiliares (se houver): suporte nos protótipos.

## 17.2 Ritos de acompanhamento pré-execução

* Checkpoints semanais com o orientador via reuniões ou e-mails.
* Revisão obrigatória do plano final e do protocolo piloto antes da coleta.
* Feedback pós-piloto para revisão das etapas se necessário.

## 17.3 Processo de controle de mudanças no plano

* Qualquer alteração significativa deverá ser documentada por e-mail e aprovada pelo orientador.
* Mudanças são registradas no histórico de versões do plano e comunicadas formalmente a todos os envolvidos antes da adoção.

---

# 18. Plano de documentação e reprodutibilidade

## 18.1 Repositórios e convenções de nomeação

Todos os documentos, instrumentos, planilhas e scripts serão armazenados em repositório Google Drive acadêmico protegido.
Nomeação: **“TCC_SDUI_Nome_Documento_DataVersão”.**

## 18.2 Templates e artefatos padrão

* Questionário de satisfação e SUS (Google Forms).
* Planilhas de registro de logs.
* Termo de consentimento padrão da universidade.
* Roteiro de entrevistas semi-estruturadas.
* Checklists para execução do experimento.

## 18.3 Plano de empacotamento para replicação futura

* Todos os documentos, questionários, scripts de coleta/análise e guias serão organizados em uma pasta **“Reprodutibilidade”**, facilitando uso por outros alunos/equipes.
* Relatório final descrevendo limitações, recomendações e instruções para replicação.

---

# 19. Plano de comunicação

## 19.1 Públicos e mensagens-chave pré-execução

* Participantes: objetivos, escopo, datas, procedimentos e direitos.
* Orientador: versão final do plano, datas dos marcos, eventuais ajustes.
* Equipe de laboratório: datas reservadas, recursos necessários.
* Desenvolvedores (se houver): prazos, escopo, formato dos dados exigidos.

## 19.2 Canais e frequência de comunicação

* E-mail para convites oficiais, updates e documentação.
* Mensagens por grupos de WhatsApp dos cursos para recrutamento.
* Reuniões presenciais com orientador e equipe antes dos marcos do cronograma.

## 19.3 Pontos de comunicação obrigatórios

* Aprovação final do plano.
* Conclusão do piloto/ajustes necessários.
* Mudanças relevantes na logística.
* Divulgação dos resultados preliminares e publicação do relatório final.

---

# 20. Critérios de prontidão para execução (Definition of Ready)

## 20.1 Checklist de prontidão (itens que devem estar completos)

* Plano do experimento aprovado pelo orientador.
* Instrumentos e protótipos concluídos e revisados pelo menos 3 dias antes do piloto.
* Aprovação ética formalizada/documentada se aplicável.
* Agenda dos participantes confirmada.
* Materiais impressos ou digitais prontos (questionários, consentimentos, guiões).

## 20.2 Aprovações finais para iniciar a operação

* Aval do orientador via e-mail ou assinatura em ata/documento digital.
* Caso exija, aprovação do CEP/universidade registrada em cópia para arquivo.
