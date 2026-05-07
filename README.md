# 🎬 Rede de Cinemas – Sistema de Gerenciamento

Projeto acadêmico desenvolvido na disciplina de **Engenharia de Software**, com o objetivo de modelar e implementar um sistema de informação para gerenciamento de uma rede de cinemas com múltiplas unidades.

---

## 📋 Sobre o projeto

O sistema centraliza o controle de filmes em cartaz, sessões, registro de público e geração de relatórios, garantindo confiabilidade e facilidade de evolução.

**Principais funcionalidades:**
- Cadastro de cinemas, salas e filmes
- Controle de sessões com validação de conflito de horário
- Registro diário de público por sessão
- Relatórios de público por sessão, filme e cinema
- Consulta de elenco, diretores e gêneros

---

## 📁 Estrutura do repositório

```
cinema/
├── README.md
├── requisitos/
│   ├── requisitos-funcionais.md
│   ├── regras-de-negocio.md
│   └── requisitos-nao-funcionais.md
└── diagramas/
    ├── UC.md
    ├── classes.md
    ├── atividades.md
    ├── sequencias.md
    ├── casos-de-uso.puml
    ├── diagrama-classes.puml
    ├── atividade-cadastrar-sessao.puml
    ├── atividade-registrar-publico.puml
    ├── atividade-gerar-relatorio.puml
    ├── sequencia-cadastrar-sessao.puml
    ├── sequencia-registrar-publico.puml
    └── sequencia-gerar-relatorio.puml
```

---

## 📐 Diagramas UML

### Casos de Uso
Visão geral dos atores **Funcionário/Administrador** e **Espectador** e suas interações com o sistema.
→ [`diagramas/UC.md`](diagramas/UC.md)

### Diagrama de Classes
Entidades do domínio com atributos e relacionamentos.
→ [`diagramas/classes.md`](diagramas/classes.md)

### Diagramas de Atividade
Fluxos dos principais casos de uso: cadastrar sessão, registrar público e gerar relatório.
→ [`diagramas/atividades.md`](diagramas/atividades.md)

### Diagramas de Sequência
Interação entre as camadas View, Controller, Service e Repository com persistência em SQLite.
→ [`diagramas/sequencias.md`](diagramas/sequencias.md)

---

## 📄 Requisitos

| Documento | Descrição |
|---|---|
| [`requisitos-funcionais.md`](requisitos/RF.md) | RF01 a RF11 |
| [`regras-de-negocio.md`](requisitos/RN.md) | RN01 a RN08 |
| [`requisitos-nao-funcionais.md`](requisitos/RNF.md) | RNF01 a RNF05 |

---

## 🔗 Rastreabilidade

| Caso de Uso | Requisito | Regra de Negócio |
|---|---|---|
| Cadastrar Sessão | RF05 | RN01, RN04, RN05, RN06 |
| Registrar Público | RF07 | RN02, RN03 |
| Gerar Relatório | RF11 | RN08 |

---

## 🏗️ Arquitetura

O sistema segue a arquitetura em camadas **MVC + Service + Repository** com persistência em **SQLite**.

```
View → Controller → Service → Repository → SQLite
```

---

## 🛠️ Como gerar os diagramas

Com o [PlantUML JAR](https://plantuml.com/download):

```bash
java -jar plantuml.jar diagramas/*.puml
```

Ou acesse o [editor online](https://www.plantuml.com/plantuml/uml/) e cole o conteúdo de cada `.puml`.
