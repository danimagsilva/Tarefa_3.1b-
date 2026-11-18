# Tarefa_3.1b-
Tarefa 3.1B, da Unidade Curricular de Desenvolvimento Avançado Web - MEIW

# Projeto Animalec — Back-office (Tarefa 3.1b)

## 1. Contextualização e Objetivo
Este repositório contém o planeamento, a conceção visual e a prototipagem funcional da extensão do **Back-office (Página de Administração)** da plataforma **Animalec** (baseada no Capítulo A.3 do livro recomendado). 

Além das entidades base já previstas no sistema (*Animais*, *Utilizadores*, *Quizzes* e *Questões*), este trabalho introduz e integra duas novas entidades de gestão:
* **Sponsors (Patrocinadores):** Organizações ou particulares que se identificam com os animais e apoiam financeiramente ou logisticamente a plataforma/espécies.
* **Experts (Especialistas):** Cientistas, biólogos ou consultores especializados em determinadas espécies ou famílias de animais.

---

## 2. Planeamento e Modelação das Novas Entidades

Para garantir que o Back-office recolhe a informação necessária e suficiente para gerir cada entidade, foram definidos os seguintes atributos e operações CRUD (*Create, Read, Update, Delete*):

### 2.1. Entidade: Patrocinadores (`Sponsors`)
| Campo | Tipo de Dado | Descrição / Finalidade |
| :--- | :--- | :--- |
| **Nome / Organização** | Texto (Obrigatório) | Identificação oficial da empresa, ONG ou particular. |
| **Tipo de Entidade** | Seleção (`Empresa`, `ONG`, `Particular`) | Classificação para efeitos de gestão e comunicação. |
| **Animal / Espécie Associada** | Texto / Relação | Espécie ou animal específico que o patrocinador apoia. |
| **Email de Contacto** | Email (Obrigatório) | Canal direto de comunicação com o patrocinador. |
| **Nível de Apoio** *(opcional)* | Seleção (`Ouro`, `Prata`, `Bronze`) | Escalão de patrocínio atribuído. |
| **Estado** *(opcional)* | Booleano (`Ativo` / `Inativo`) | Controlo de visibilidade na página pública. |

### 2.2. Entidade: Especialistas (`Experts`)
| Campo | Tipo de Dado | Descrição / Finalidade |
| :--- | :--- | :--- |
| **Nome Completo** | Texto (Obrigatório) | Nome e título profissional do especialista. |
| **Especialidade / Família** | Texto (Obrigatório) | Área científica de atuação (ex.: *Felinos*, *Aves*, *Répteis*). |
| **Instituição / Afiliação** | Texto (Obrigatório) | Universidade, centro de investigação ou entidade de origem. |
| **Email Profissional** | Email (Obrigatório) | Contacto para validação científica de conteúdos e quizzes. |
| **Grau Académico** *(opcional)* | Texto / Seleção | Qualificação científica (ex.: *Doutoramento*, *Mestrado*). |
| **Notas / Biografia** *(opcional)* | Texto Longo | Breve resumo do currículo ou áreas de investigação. |

---

## 3. Estrutura do Repositório

Os artefactos produzidos encontram-se organizados por fase de conceção e dispositivo alvo:

```text
Tarefa_3.1b/
├── README.md                  # Documentação geral do projeto
├── wireframes/
│   ├── desktop/               # Esquemas de baixa fidelidade para browser (.drawio / .png)
│   └── mobile/                # Esquemas de baixa fidelidade para dispositivos móveis (.drawio / .png)
├── mockups/
│   ├── desktop/               # Representações visuais de alta fidelidade para browser (.drawio / .png)
│   └── mobile/                # Representações visuais de alta fidelidade para mobile (.drawio / .png)
└── prototipo/
    └── index.html             # Protótipo interativo do Back-office em HTML5 semântico
```

---

## 4. Processo de Prototipagem e Decisões de Design

O desenvolvimento seguiu uma abordagem progressiva e complementar entre os três níveis de representação:

1. **Wireframes (Baixa Fidelidade):** Desenvolvidos na ferramenta **draw.io**, focados exclusivamente na arquitetura de informação, hierarquia de conteúdos e fluxo de navegação. Na versão *mobile*, optou-se por adaptar o menu horizontal/lateral para navegação simplificada e converter tabelas extensas em blocos empilhados.
2. **Mockups (Alta Fidelidade):** Evolução visual dos wireframes com aplicação da paleta cromática associada ao projeto Animalec (tons de verde escuro, verde natural e fundos neutros), tipografia legível, ícones funcionais e dados de exemplo realistas.
3. **Protótipo Funcional (HTML5):** Implementação navegável da Página de Administração onde as novas entidades estão integradas no menu principal e no painel de controlo (*dashboard*), permitindo testar a adição e remoção dinâmica de registos.

### Contributo da Semântica HTML5
A estruturação do protótipo recorre às etiquetas semânticas do **HTML5** para reforçar a clareza estrutural e a acessibilidade:
* `<header>` e `<footer>`: Delimitam o cabeçalho de identificação da área administrativa e o rodapé institucional.
* `<nav>`: Agrupa os controlos de navegação entre módulos (*Animais*, *Utilizadores*, *Quizzes*, *Sponsors* e *Experts*).
* `<main>`: Envolve o conteúdo principal ativo em cada vista.
* `<section>` e `<article>`: Separam logicamente cada módulo de gestão, os cartões do painel inicial, os formulários de criação e as tabelas de listagem.

---

## 5. Como Testar o Protótipo

Não é necessária a instalação de dependências ou servidor dedicado para testar o protótipo:

1. Clonar ou descarregar este repositório:
   ```bash
   git clone <URL-DO-TEU-REPOSITORIO>
   ```
2. Aceder à pasta `prototipo/`.
3. Abrir o ficheiro `index.html` diretamente em qualquer navegador web moderno (Chrome, Firefox, Edge ou Safari).
4. Utilizar a barra de navegação ou os cartões do painel principal para explorar as secções **Patrocinadores (Sponsors)** e **Especialistas (Experts)** e testar o formulário de registo e remoção.

---

## 6. Autor
* **Nome:** [Daniel Silva]
* **Número de Aluno:** [58727]
* **Unidade Curricular:** [Desenvolvimento Avançado Web]
