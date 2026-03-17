# 🛡️ Caderno Temático: Segurança da Informação & Cibersegurança
### Projeto DIO — Aprendizagem Ativa com NotebookLM

> **Repositório:** `miniguia-estudos-ciberseguranca`
> **Nível:** Intermediário
> **Plataforma de Curadoria:** Google NotebookLM
> **Última atualização:** Março de 2026

---

## 📌 Contexto e Objetivos

### Por que Cibersegurança?

Em um mundo onde dados valem mais do que petróleo, proteger sistemas, redes e informações deixou de ser responsabilidade exclusiva de especialistas e passou a ser uma competência transversal essencial. Ataques de ransomware, engenharia social, exploração de vulnerabilidades e vazamentos de dados são realidades diárias — e entender como funcionam (tanto do lado do ataque quanto da defesa) é o que separa profissionais reativos de profissionais estratégicos.

Este caderno temático foi construído com foco no nível **intermediário**: pressupõe familiaridade com redes, sistemas operacionais e conceitos básicos de segurança, e avança para tópicos como modelagem de ameaças, criptografia aplicada, análise de vulnerabilidades e frameworks de defesa.

### Objetivos de Estudo

| # | Objetivo | Status |
|---|----------|--------|
| 1 | Dominar os fundamentos de criptografia simétrica, assimétrica e hashing | ✅ Concluído |
| 2 | Compreender o ciclo de vida de um ataque (Kill Chain & MITRE ATT&CK) | ✅ Concluído |
| 3 | Aplicar modelagem de ameaças com o framework STRIDE | ✅ Concluído |
| 4 | Entender os principais tipos de vulnerabilidades (OWASP Top 10) | ✅ Concluído |
| 5 | Construir glossário técnico consolidado para revisão futura | ✅ Concluído |
| 6 | Mapear ferramentas essenciais de segurança ofensiva e defensiva | 🔄 Em progresso |

---

## 📚 Curadoria de Fontes

Foram selecionadas **5 fontes abertas** de alta qualidade, disponíveis gratuitamente, inseridas no NotebookLM para análise cruzada:

### Fonte 1 — OWASP Top 10 (2021)
- **Tipo:** Documentação Web / PDF
- **Autores:** Open Web Application Security Project (OWASP)
- **Link:** [https://owasp.org/www-project-top-ten/](https://owasp.org/www-project-top-ten/)
- **Por que escolhi:** O guia mais referenciado do mundo em segurança de aplicações web. Cobre as 10 categorias de risco mais críticas com exemplos reais, cenários de ataque e contramedidas. Essencial para qualquer profissional de AppSec.

### Fonte 2 — NIST Cybersecurity Framework (CSF 2.0)
- **Tipo:** PDF Oficial
- **Autores:** National Institute of Standards and Technology (NIST)
- **Link:** [https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf](https://nvlpubs.nist.gov/nistpubs/CSWP/NIST.CSWP.29.pdf)
- **Por que escolhi:** Framework de referência global para gestão de riscos em cibersegurança. A versão 2.0 adiciona a função "Govern" e é amplamente adotada por organizações públicas e privadas.

### Fonte 3 — The Web Application Hacker's Handbook (Capítulos selecionados)
- **Tipo:** PDF parcial (caps. 1, 2, 3 e 7)
- **Autores:** Stuttard & Pinto
- **Link:** [https://archive.org/details/TheWebApplicationHackersHandbook](https://archive.org/details/TheWebApplicationHackersHandbook)
- **Por que escolhi:** Abordagem técnica e prática sobre como atacantes exploram aplicações web. Complementa o OWASP com perspectiva ofensiva — essencial para pentesters.

### Fonte 4 — Computer Security: Art and Science (Capítulos selecionados)
- **Tipo:** PDF parcial (caps. 1, 4, 9 e 13)
- **Autores:** Matt Bishop
- **Link:** [https://www.cs.ucdavis.edu/~bishop/secbook/](https://www.cs.ucdavis.edu/~bishop/secbook/)
- **Por que escolhi:** Visão teórica sólida sobre fundamentos de segurança — políticas, controle de acesso, criptografia e verificação formal. Essencial para consolidar a base conceitual.

### Fonte 5 — MITRE ATT&CK Framework (Enterprise)
- **Tipo:** Documentação Web + PDF exportado
- **Autores:** MITRE Corporation
- **Link:** [https://attack.mitre.org/](https://attack.mitre.org/)
- **Por que escolhi:** A base de conhecimento mais completa sobre táticas, técnicas e procedimentos (TTPs) usados por atacantes reais. Imprescindível para blue team e threat hunting.

---

## 🧪 Engenharia de Prompts e "Cicatrizes"

---

### Sessão 1 — Criptografia Aplicada

#### Prompt Inicial (v1) ❌
```
Me explique criptografia.
```
**Problema:** Resposta extremamente genérica. O NotebookLM apresentou um resumo básico sem referenciar os documentos carregados nem abordar aspectos práticos de uso.

#### Prompt Refinado (v2) ✅
```
Com base nos documentos carregados (especialmente Bishop e NIST CSF),
explique a diferença entre criptografia simétrica (AES) e assimétrica (RSA/ECC)
em termos de: (1) funcionamento matemático simplificado, (2) casos de uso ideais,
(3) vulnerabilidades conhecidas de cada abordagem e (4) como o TLS combina
os dois modelos na prática.
```
**Resultado:** Resposta estruturada em 4 partes com referências diretas ao capítulo de criptografia do Bishop e ao componente "Protect" do NIST CSF. Incluiu handshake TLS explicado passo a passo.

**Aprendizado 🎯:** Especificar quais fontes usar + estrutura de resposta desejada + nível técnico transforma uma resposta genérica em conteúdo realmente utilizável.

---

### Sessão 2 — OWASP Top 10

#### Prompt Inicial (v1) ❌
```
Quais são as vulnerabilidades mais comuns em aplicações web?
```
**Problema:** Listou vulnerabilidades genéricas sem usar a estrutura do OWASP Top 10 que estava nos documentos carregados.

#### Prompt Refinado (v2) ✅
```
Com base no documento OWASP Top 10 (2021) carregado, para cada uma das
10 categorias de risco forneça: (1) nome e código da categoria,
(2) descrição técnica do risco em 2 frases, (3) exemplo concreto de vetor
de ataque, (4) contramedida principal recomendada pelo OWASP.
Formate como tabela compacta.
```
**Resultado:** Tabela completa das 10 categorias com código (ex: A01:2021), vetores e contramedidas diretamente referenciadas no documento.

**Aprendizado 🎯:** Para documentos com estrutura própria, referenciar essa estrutura no prompt faz o NotebookLM seguir o "template" do documento.

---

### Sessão 3 — MITRE ATT&CK

#### Prompt Inicial (v1) ❌
```
O que é o MITRE ATT&CK?
```
**Problema:** Definição superficial em um parágrafo. Não aproveitou a riqueza do framework exportado como fonte.

#### Prompt Refinado (v2) ✅
```
Com base no documento MITRE ATT&CK carregado, trace o caminho completo
de um ataque de ransomware usando as táticas do framework Enterprise,
desde o acesso inicial até o impacto. Para cada tática, cite ao menos
uma técnica específica (com ID) e como um blue team poderia detectá-la.
```
**Resultado:** Narrativa completa de um ataque end-to-end mapeada ao MITRE ATT&CK — da Tática TA0001 (Initial Access) até TA0040 (Impact) — com técnicas reais como T1566.001 e recomendações de detecção via SIEM/EDR.

**Aprendizado 🎯:** Pedir uma narrativa orientada a caso de uso real é muito mais eficaz do que pedir "explique o framework".

---

### Sessão 4 — Modelagem STRIDE

#### Prompt ✅ (funcionou bem desde a v1)
```
Com base nos documentos carregados, aplique o framework STRIDE para modelar
as ameaças de um sistema de autenticação com login por e-mail e senha.
Para cada letra do acrônimo (Spoofing, Tampering, Repudiation, Information
Disclosure, Denial of Service, Elevation of Privilege), descreva: o tipo de
ameaça, um ataque concreto possível e uma contramedida técnica.
```
**Resultado:** Análise STRIDE completa com ameaças realistas (ex: credential stuffing para Spoofing, SQL injection para Tampering) e contramedidas específicas (MFA, prepared statements, rate limiting).

---

### 🔥 Troubleshooting — Principais Dificuldades

| Problema Encontrado | Causa Provável | Solução Aplicada |
|---------------------|----------------|------------------|
| Respostas sem citar documentos carregados | Prompt sem direcionamento de fonte | Adicionar "com base no documento X carregado" explicitamente |
| Confusão entre termos similares (ex: autenticação vs. autorização) | Falta de diferenciação no prompt | Usar "compare e contraste X vs Y" com critérios explícitos |
| Alucinação em CVEs específicos | Dados dinâmicos fora das fontes carregadas | Adicionar "cite apenas CVEs mencionados nos documentos carregados" |
| Respostas longas e sem foco prático | Perguntas abertas demais | Limitar com "em no máximo 3 parágrafos" ou "formate como tabela" |
| PDF do NIST pouco aproveitado (arquivo grande) | NotebookLM priorizou partes iniciais | Referenciar seções específicas: "na seção Protect do NIST CSF..." |

---

## 📖 Miniguia de Estudo — Entrega Final

---

### PARTE 1 — Resumos Estruturados

#### 🔹 A Tríade CIA — Base da Segurança da Informação

| Pilar | Definição | Ameaças | Contramedidas |
|-------|-----------|---------|---------------|
| **Confidencialidade** | Acesso apenas por quem tem autorização | Interceptação, credential theft | Criptografia, MFA, controle de acesso |
| **Integridade** | Dados não alterados sem autorização | Tampering, MITM, SQL injection | SHA-256, assinaturas digitais, checksums |
| **Disponibilidade** | Sistemas acessíveis quando necessários | DDoS, ransomware, falhas de HW | Redundância, backups, rate limiting |

Além da tríade clássica, frameworks modernos adicionam **Autenticidade** (garantia de identidade) e **Não-repúdio** (impossibilidade de negar uma ação realizada).

---

#### 🔹 Criptografia Aplicada

**Simétrica (AES-256):** Uma única chave para cifrar/decifrar. Muito rápida. Problema: distribuição segura da chave. Uso: disco, VPNs, bancos de dados.

**Assimétrica (RSA/ECC):** Par de chaves pública/privada. Resolve o problema de distribuição. Lenta para grandes volumes. Uso: TLS, SSH, assinaturas, PKI.

**TLS na prática:** Handshake assimétrico (troca de chave de sessão) → comunicação com chave simétrica (velocidade). O melhor dos dois mundos.

**Hashing (SHA-256, bcrypt):** Função de mão única. Mesmo input → mesmo hash. Qualquer alteração muda completamente o output. Uso: senhas, integridade de arquivos, assinaturas.

---

#### 🔹 Ciclo de Vida de um Ataque: Kill Chain + MITRE ATT&CK

```
Reconnaissance → Weaponization → Delivery → Exploitation
→ Installation → C2 (Command & Control) → Actions on Objectives
```

| Fase Kill Chain | Tática ATT&CK | Técnicas Comuns |
|----------------|---------------|-----------------|
| Reconnaissance | TA0043 | T1595 (Active Scanning), T1589 (Gather Victim Identity) |
| Initial Access | TA0001 | T1566 (Phishing), T1190 (Exploit Public-Facing App) |
| Execution | TA0002 | T1059 (Scripting Interpreter), T1204 (User Execution) |
| Persistence | TA0003 | T1053 (Scheduled Task), T1136 (Create Account) |
| Privilege Escalation | TA0004 | T1068 (Exploit for PrivEsc), T1548 (Abuse Elevation) |
| Lateral Movement | TA0008 | T1021 (Remote Services), T1550 (Alternate Auth Material) |
| Impact | TA0040 | T1486 (Data Encrypted for Impact), T1498 (DoS) |

---

#### 🔹 OWASP Top 10 (2021)

| Código | Categoria | Contramedida-chave |
|--------|-----------|-------------------|
| A01 | Broken Access Control | Deny by default, validação server-side |
| A02 | Cryptographic Failures | TLS obrigatório, AES-256, bcrypt |
| A03 | Injection | Prepared statements, ORMs, input validation |
| A04 | Insecure Design | Threat modeling, secure design patterns |
| A05 | Security Misconfiguration | Hardening, CIS Benchmarks |
| A06 | Vulnerable Components | SCA, patch management automatizado |
| A07 | Auth Failures | MFA, session management seguro |
| A08 | Software Integrity Failures | Assinaturas digitais, SBOM |
| A09 | Logging & Monitoring Failures | SIEM, alertas em tempo real |
| A10 | SSRF | Allowlist de URLs, desabilitar redirecionamentos |

---

#### 🔹 NIST CSF 2.0 — As 6 Funções

```
GOVERN → IDENTIFY → PROTECT → DETECT → RESPOND → RECOVER
```

| Função | O que cobre | Exemplo prático |
|--------|------------|-----------------|
| **Govern** | Estratégia, políticas, papéis | Política de segurança, definição de CISO |
| **Identify** | Inventário de ativos, riscos | Mapeamento de sistemas críticos |
| **Protect** | Controles, criptografia, treinamento | MFA, firewalls, segmentação de rede |
| **Detect** | Monitoramento, anomalias | SIEM, IDS/IPS, threat intelligence |
| **Respond** | Planos de resposta, contenção | Runbooks, isolamento de sistemas |
| **Recover** | Restauração, lições aprendidas | RTO/RPO, postmortem, melhoria contínua |

---

### PARTE 2 — Glossário Técnico

| Termo | Definição | Fonte |
|-------|-----------|-------|
| **APT** | Advanced Persistent Threat — ator sofisticado (geralmente estado-nação) com presença prolongada em redes-alvo | MITRE ATT&CK |
| **Attack Surface** | Conjunto de pontos de entrada (portas, APIs, usuários) exploráveis por um atacante | Bishop |
| **Blue Team** | Time de defesa ativa — monitoramento, detecção e resposta a incidentes | NIST CSF |
| **CVSS** | Common Vulnerability Scoring System — sistema de pontuação de severidade de vulnerabilidades (0-10) | OWASP |
| **Defense in Depth** | Múltiplas camadas de controles de segurança — se uma falha, outra compensa | Bishop + NIST |
| **Exploit** | Código/técnica que aproveita uma vulnerabilidade para executar ações não autorizadas | MITRE ATT&CK |
| **Hardening** | Reduzir a superfície de ataque removendo serviços desnecessários e aplicando configurações seguras | NIST CSF |
| **IOC** | Indicator of Compromise — artefato (hash, IP, domínio) que indica comprometimento | MITRE ATT&CK |
| **Least Privilege** | Princípio de conceder apenas permissões mínimas necessárias para cada usuário/processo | Bishop |
| **MITM** | Man-in-the-Middle — atacante se posiciona entre duas partes para interceptar/modificar comunicações | Stuttard & Pinto |
| **Payload** | Parte do código malicioso que executa a ação danosa (distinto do vetor de entrega) | MITRE ATT&CK |
| **Pentesting** | Teste de penetração controlado para identificar vulnerabilidades antes de atacantes reais | Stuttard & Pinto |
| **Red Team** | Time que simula adversários reais para testar a eficácia dos controles de segurança | MITRE ATT&CK |
| **SIEM** | Security Information and Event Management — plataforma que centraliza e correlaciona logs em tempo real | NIST CSF |
| **TTP** | Tactics, Techniques, and Procedures — descrição do comportamento de atacantes no MITRE ATT&CK | MITRE ATT&CK |
| **Threat Modeling** | Processo estruturado de identificar ameaças e contramedidas durante o design de um sistema | Bishop |
| **Zero-Day** | Vulnerabilidade desconhecida pelo fabricante, para a qual ainda não existe patch disponível | OWASP + MITRE |
| **XSS** | Cross-Site Scripting — injeção de scripts maliciosos em páginas web executados no navegador da vítima | OWASP A03 |
| **CSRF** | Cross-Site Request Forgery — força o navegador de uma vítima autenticada a executar ações não intencionadas | OWASP |
| **Pivoting** | Usar um sistema comprometido como ponto de entrada para atacar outros sistemas na rede interna | MITRE ATT&CK |

---

### PARTE 3 — Prompts Reutilizáveis

#### 🔁 Para Análise de Vulnerabilidade
```
Com base nos documentos carregados, analise a vulnerabilidade [NOME/CVE/CATEGORIA]
nos seguintes aspectos:
1. Mecanismo técnico de funcionamento
2. Vetor de ataque típico (passo a passo simplificado)
3. Sistemas/configurações afetados
4. Contramedidas preventivas e corretivas
5. Referência MITRE ATT&CK (tática + técnica ID) se aplicável
```

#### 🔁 Para Modelagem de Ameaças (STRIDE)
```
Aplique o framework STRIDE para modelar as ameaças de [SISTEMA/COMPONENTE].
Para cada categoria (Spoofing, Tampering, Repudiation, Information Disclosure,
Denial of Service, Elevation of Privilege):
- Descreva a ameaça específica para este contexto
- Cite um ataque concreto possível
- Proponha uma contramedida técnica implementável
```

#### 🔁 Para Mapeamento no MITRE ATT&CK
```
Com base no documento MITRE ATT&CK carregado, trace o caminho de um ataque
de [TIPO: ransomware / APT / insider threat / supply chain].
Para cada tática utilizada:
- Identifique a tática (TA####) e nome
- Cite a técnica mais provável (T#### com nome)
- Descreva como um blue team poderia detectar essa atividade
```

#### 🔁 Para Revisão de Controles (NIST CSF)
```
Com base no NIST CSF e nos demais documentos carregados, avalie os controles
de segurança para [TIPO DE SISTEMA: aplicação web / API REST / cloud].
Para cada função do NIST (Govern, Identify, Protect, Detect, Respond, Recover):
- Identifique o controle mais crítico
- Descreva como implementá-lo
- Indique o risco mitigado
```

#### 🔁 Para Estudo de Caso de Incidente
```
Com base nos documentos carregados, analise o seguinte cenário de incidente:
[DESCREVA O CENÁRIO].
Responda:
1. Quais categorias do OWASP Top 10 foram potencialmente exploradas?
2. Qual sequência de táticas MITRE ATT&CK melhor descreve o ataque?
3. Quais controles do NIST CSF falharam?
4. Que ações de resposta e recuperação deveriam ser tomadas?
```

#### 🔁 Para Autoavaliação Técnica
```
Com base em todo o material carregado sobre [SUBTÓPICO DE SEGURANÇA],
crie 8 questões de nível intermediário-avançado:
- 3 questões conceituais (4 alternativas + gabarito comentado)
- 3 questões de aplicação prática (cenário + solução esperada)
- 2 questões "pegadinha" baseadas em erros comuns de profissionais
```

---

## 🤔 Reflexões Finais

Este projeto evidenciou que aprender cibersegurança com IA exige **disciplina de prompt** acima de tudo. Ao contrário de outras áreas, em segurança uma resposta imprecisa pode ser perigosa — ela pode omitir contramedidas críticas ou simplificar demais vetores de ataque.

**Aprendizados principais:**
1. Referenciar fontes específicas no prompt faz toda a diferença
2. Pedir "trace o caminho de um ataque real" gera mais aprendizado do que "explique o conceito X"
3. Documentar os prompts que falharam é tão valioso quanto registrar os que funcionaram
4. A combinação OWASP + MITRE + NIST cria uma visão 360° que nenhum documento sozinho fornece

---

*Projeto desenvolvido como parte do desafio prático da [DIO — Digital Innovation One](https://www.dio.me)*
