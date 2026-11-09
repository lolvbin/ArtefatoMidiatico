# Processos de Testes de Software para o Desenvolvimento Web: Conceitos Básicos sobre Segurança dos Dados

> Repositório oficial do manuscrito acadêmico e artefato midiático (infográfico) desenvolvido para a Unidade Curricular de Processos de Testes e Segurança de Software.

---

## 📌 Sobre o Projeto

Este estudo analisa a integração e a aplicação sinérgica de ferramentas de **Teste Estático (SAST)** e **Teste Dinâmico (DAST)** ao longo do **Ciclo de Vida de Desenvolvimento Seguro (CVDS)**. O foco principal é mitigar vulnerabilidades críticas do **OWASP Top 10** — tais como *SQL Injection* (SQLi), *Cross-Site Scripting* (XSS) e *Sequestro de Sessão* —, reduzindo riscos ocultos no código-fonte sob o conceito de **Shift-Left** e o modelo de **Confiança Zero (Zero Trust)**.

---

## 🎨 Artefato Midiático (Infográfico)

O artefato conceitual e prático deste projeto consiste em um **Infográfico Modular de Defesa Cibernética**, desenhado no Figma e estruturado no modelo de 3 passos por vulnerabilidade (*Ameaça/Risco ➔ Nível de Teste & Ferramenta ➔ Contramedida Técnica*).

```text
+-----------------------------------------------------------------------------------+
|                            FLUXO DE DEFESA CIBERNÉTICA                            |
+------------------------------+-------------------------------+--------------------+
| 1. AMEAÇA / RISCO OCULTO     | 2. ESTRATÉGIA SAST / DAST     | 3. CONTRAMEDIDA    |
| (Ex: SQL Injection, XSS)     | (Ex: SonarQube, OWASP ZAP)    | (Prepared Stmts)   |
+------------------------------+-------------------------------+--------------------+
```

- **Visualização da Arte:** Disponível na pasta [`/artefato-midiatico`](./artefato-midiatico/).
- **Projeto no Figma:** Link do projeto no Figma.

---

## 📊 Matriz Mapeada de Vulnerabilidades & Testes (Tabela 1)

| Risco | Vulnerabilidade (OWASP Top 10) | Nível de Teste (CVDS) | Abordagem & Ferramentas | Diretriz Técnica de Prevenção |
| :---: | :--- | :---: | :---: | :--- |
| **(1)** | **SQL Injection (SQLi)** | Unidade / Integração | SAST (SonarQube, Checkmarx) | *Prepared Statements* e Consultas Parametrizadas |
| **(2)** | **XSS Refletido & Armazenado** | Sistema / Runtime | DAST (OWASP ZAP, Burp Suite) | Sanitização/Encode de saídas HTTP |
| **(3)** | **DOM-Based XSS** | Unidade (*Client-Side*) | SAST especializado em JS | Context-Aware Output Encoding na DOM |
| **(4)** | **Sequestro de Sessão** | Integração / Sistema | DAST (Análise de Requisições) | Flags `HttpOnly`, `Secure` e `SameSite` nos Cookies |
| **(5)** | **Quebra de Controle de Acesso** | Integração | SAST + DAST | Validação Server-Side de Autorização (RBAC/ABAC) |

---

## 🔬 Metodologia Científica

A pesquisa adota uma abordagem qualitativa descritivo-exploratória estruturada via:
1. **Modelo 5W1H:** Mapeamento sistemático de escopo (*What, Why, Who, Where, When, How*).
2. **Revisão Integrativa da Literatura (*Snowballing*):** Seleção a partir de um *Seed Set* acadêmico, aplicando buscas *Backward* (referências) e *Forward* (citações) com critérios formais de inclusão e exclusão.

---

## 📂 Estrutura do Repositório

```text
├── artigo/                # Manuscrito acadêmico (Docx e PDF - P2)
├── artefato-midiatico/    # Imagens do Infográfico e links do Figma
├── entregas-uchub/        # Documentos da Sprint 1 (Pré-Projeto e Canvas)
├── slides/                # Apresentações de apoio para defesa/banca
└── README.md              # Documentação principal
```

---

## 👥 Integrantes da Squad & Autoria

| Nome Completo | RA | Curso | E-mail Institucional |
| :--- | :---: | :---: | :--- |
| **Vitor Lobo de Faria Ribeiro** | `326116898` | Análise e Dev. de Sistemas | `326116898@ulife.com.br` |
| **Anna Clara dos Santos Nascimento** | `326117021` | Ciência da Computação | `326117021@ulife.com.br` |
| **Lucas da Cruz Dias** | `326118818` | Análise e Dev. de Sistemas | `326118818@ulife.com.br` |
| **Cleyton Fernandes Martins** | `326119164` | Análise e Dev. de Sistemas | `326119164@ulife.com.br` |

- **Orientador:** Prof. Junio Soares Dias
- **Instituição:** Centro Universitário UNA — Campus Belo Horizonte / Ânima Hub

---

## 📜 Licença

Este projeto está sob a licença MIT.
