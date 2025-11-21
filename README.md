# 1. Identificação básica

## 1.1 Título do experimento

**Comparação Experimental entre Server-Driven UI e UI Tradicional em Aplicativos iOS: Desempenho e Experiência do Usuário**

## 1.2 ID / código
**1029366**

## 1.3 Versão do documento e histórico de revisão

* **v1.0 – 21/11/2025** – Versão inicial

## 1.4 Datas (criação, última atualização)

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

O ritmo de atualização e personalização das interfaces dos aplicativos iOS é cada vez mais demandado, mas o modelo tradicional, onde toda a interface está embutida no app, torna o processo lento e pouco flexível. Nessas arquiteturas, qualquer modificação visual ou estrutural exige uma nova versão do aplicativo, passando por etapas burocráticas como versionamento, build, submissão para aprovação na App Store e posterior publicação. Esse fluxo pode ser demorado, sobretudo devido aos processos de validação da loja. Além disso, mesmo após disponibilizar a atualização, não há garantia de que o usuário irá de fato baixar a nova versão, o que pode deixar parte da base desatualizada e prejudicar a padronização da experiência.

O modelo Server-Driven UI (SDUI) promete resolver esses desafios, permitindo alterações dinâmicas e personalizadas diretamente pelo backend, sem necessidade de update completo do app. Com isso, é possível contornar limitações de versionamento, acelerar o tempo de resposta às demandas de negócio e garantir que todos os usuários recebam rapidamente as mudanças na interface. Porém, ainda há dúvidas sobre o impacto real do SDUI no desempenho e na experiência do usuário em comparação com o modelo tradicional, principalmente em cenários de latência e conectividade.

## 2.2 Contexto organizacional e técnico

O experimento será realizado em ambiente acadêmico, com o estudante, professores e desenvolvedores convidados. Serão utilizados dois protótipos idênticos em funcionalidade:

* um construído em **SDUI** (server-driven)
* outro **client-driven (UI tradicional)**

Ambos desenvolvidos em Swift, utilizando Xcode e backend específico para o app SDUI.

## 2.3 Trabalhos e evidências prévias (internos e externos)

* Casos de uso do SDUI em empresas como *iFood*, *Nubank* e *Spotify* 
* https://repositorio.ufms.br/handle/123456789/7963: Explorando a arquitetura do Server Driven UI
* https://dspace.mackenzie.br/handle/10899/31160: Aplicação de server driven UI para interfaces mobile ios de e-commerce

## 2.4 Referencial teórico e empírico essencial

### Arquitetura Client-Driven UI

Na abordagem **client-driven UI**, toda a estrutura da interface, lógicas de navegação e visualização são implementadas diretamente no código do aplicativo. Qualquer modificação exige uma nova versão, que precisa ser processada pelo ciclo de desenvolvimento (build, review, publicação) e, posteriormente, instalada pelo usuário. Isso pode causar lentidão no processo de evolução do produto e dificuldades para garantir que todos os usuários estejam na versão mais atual, impactando negativamente a experiência e a uniformidade da base.

### Server-Driven UI (SDUI)

**SDUI** é um paradigma arquitetural emergente no desenvolvimento mobile, no qual a definição da interface (composição, propriedades e até comportamentos básicos) é enviada pelo servidor em tempo real, tipicamente via estruturas como JSON ou XML. O aplicativo no dispositivo atua como um “renderizador” dessas instruções vindas do backend, exibindo a UI conforme definida remotamente.

### Experiência do Usuário (UX)

A **Experiência do Usuário (UX)** engloba aspectos subjetivos e objetivos da interação do usuário com o aplicativo, incluindo facilidade de uso, tempo para completar tarefas, satisfação geral, clareza das instruções, velocidade, sensação de controle e confiança. A avaliação de UX pode ser realizada tanto por métricas objetivas (tempo de resposta, sucesso nas tarefas) quanto por escalas de validação subjetivas, como o **SUS (System Usability Scale)**.

### Desempenho

No contexto de apps móveis, **desempenho** é avaliado por meio do tempo de resposta das interfaces, consumo de recursos, taxa de sucesso nas operações e estabilidade. Embora SDUI otimize atualizações e permita maior flexibilidade, também pode introduzir desafios de performance relacionados ao tempo de comunicação entre o app e o servidor, especialmente em redes móveis instáveis.
Aqui está o texto formatado corretamente em **Markdown**, pronto para copiar e colar:

# 3. Objetivos e questões (Goal / Question / Metric)

## 3.1 Objetivo geral

**Analisar e comparar, sob a perspectiva de usuários e desenvolvedores, o desempenho e a experiência do usuário em aplicativos iOS com arquitetura Server-Driven UI versus UI Tradicional.**


## 3.2 Objetivos específicos (sugestão aprimorada)

* **O1:** Medir a diferença de tempo de resposta e sucesso nas tarefas entre SDUI e UI tradicional.
* **O2:** Avaliar a satisfação e facilidade de uso percebidas por usuários finais em ambos os modelos.
* **O3:** Relatar vantagens e dificuldades percebidas por desenvolvedores e gestores acerca da manutenção, atualização (versionamento) e adoção dos modelos SDUI e tradicional.


## 3.3 GQM – Goal / Question / Metric

### **Goal**

Avaliar e comparar as arquiteturas **Server-Driven UI** e **UI Tradicional** em aplicativos iOS, a fim de compreender impactos sobre desempenho, experiência do usuário e eficiência de atualização, do ponto de vista de usuários finais e desenvolvedores, no contexto de protótipos acadêmicos.


### **Questions e Métricas**

#### **Q1: Existe diferença significativa de desempenho (tempo de resposta)?**

* **Métrica:** Tempo de resposta (ms) — coleta automatizada

#### **Q2: Usuários percebem diferença de satisfação/facilidade de uso?**

* **Métricas:**

  * Satisfação (Likert 1–5)
  * Facilidade de uso (SUS)

#### **Q3: O SDUI permite atualização de interface mais rápida e acessível?**

* **Métricas:**

  * Tempo para atualizar interface (horas/dias)
  * Esforço de manutenção (horas gastas)
