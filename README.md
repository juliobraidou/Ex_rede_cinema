# Sistema de Gerenciamento – Rede de Cinemas

Documentação de Engenharia de Software para o sistema de gerenciamento de uma rede de cinemas.

## Estrutura do repositório

```
cinema/
├── requisitos/
│   ├── requisitos-funcionais.md
│   ├── requisitos-nao-funcionais.md
│   └── regras-de-negocio.md
└── diagramas/
    ├── casos-de-uso.puml
    ├── diagrama-classes.puml
    ├── atividade-cadastrar-sessao.puml
    ├── atividade-registrar-publico.puml
    ├── atividade-gerar-relatorio.puml
    ├── sequencia-cadastrar-sessao.puml
    ├── sequencia-registrar-publico.puml
    └── sequencia-gerar-relatorio.puml
```

## Como gerar os diagramas

### Opção 1 – Editor online
Acesse [https://www.plantuml.com/plantuml/uml/](https://www.plantuml.com/plantuml/uml/) e cole o conteúdo de cada arquivo `.puml`.

### Opção 2 – JAR local
```bash
java -jar plantuml.jar diagramas/*.puml
```

### Opção 3 – VS Code
Instale a extensão **PlantUML** (jebbs.plantuml) e use `Alt+D` para preview.

## Rastreabilidade

| Requisito | Regra de Negócio | Diagrama de Atividade | Diagrama de Sequência |
|---|---|---|---|
| RF05 – Cadastrar Sessão | RN01, RN04, RN05, RN06 | atividade-cadastrar-sessao | sequencia-cadastrar-sessao |
| RF07 – Registrar Público | RN02, RN03 | atividade-registrar-publico | sequencia-registrar-publico |
| RF11 – Gerar Relatório | RN08 | atividade-gerar-relatorio | sequencia-gerar-relatorio |
