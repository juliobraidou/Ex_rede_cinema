# Requisitos Não Funcionais – Rede de Cinemas

## RNF01 – Persistência
O sistema deve utilizar **SQLite** como banco de dados local, sem dependência de servidor externo.

## RNF02 – Arquitetura
O sistema deve seguir a arquitetura em camadas **MVC + Service + Repository**, com separação clara de responsabilidades entre View, Controller, Service e Repository.

## RNF03 – Desempenho
As operações de consulta e listagem devem responder em menos de **2 segundos** em condições normais de uso.

## RNF04 – Portabilidade
O sistema deve funcionar sem necessidade de instalação de servidor externo ou serviços de terceiros.

## RNF05 – Manutenibilidade
O código deve estar organizado em módulos correspondentes às camadas da arquitetura, facilitando a evolução e correção do sistema.
