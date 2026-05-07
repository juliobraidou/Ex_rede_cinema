# Requisitos Funcionais – Rede de Cinemas

## RF01 – Cadastro de Cinema
O sistema deve permitir cadastrar cinemas informando nome, logradouro, cidade, estado e endereço completo.

## RF02 – Cadastro de Sala
O sistema deve permitir cadastrar salas vinculadas a um cinema, com número identificador e capacidade máxima de público.

## RF03 – Cadastro de Filme
O sistema deve permitir cadastrar filmes com título, sinopse, duração em minutos, ano de lançamento, classificação indicativa, status (ativo/inativo) e gênero(s).

## RF04 – Cadastro de Elenco e Direção
O sistema deve permitir associar pessoas (atores e diretores) a filmes, registrando o tipo de participação (`tipo_role`) e o nome do personagem quando aplicável.

## RF05 – Cadastro de Sessão
O sistema deve permitir cadastrar sessões vinculadas a uma sala e a um filme ativo, informando data, horário, idioma, formato (2D, 3D, IMAX) e preço do ingresso.

## RF06 – Controle de Conflito de Horário
O sistema deve impedir o cadastro de sessões que conflitem com sessões já existentes na mesma sala, respeitando a duração do filme somada ao intervalo obrigatório entre sessões definido em `ConfiguracaoSistema`.

## RF07 – Registro de Público
O sistema deve permitir registrar o total de espectadores por sessão, validando que o valor não ultrapasse a capacidade da sala e não seja negativo.

## RF08 – Totalização de Público
O sistema deve totalizar o público agrupado por sessão, por filme e por cinema, dentro de um período informado.

## RF09 – Consulta de Filmes em Cartaz
O sistema deve permitir consultar os filmes com status ativo por cinema, exibindo as sessões disponíveis com horários e detalhes.

## RF10 – Consulta de Elenco e Detalhes
O sistema deve permitir consultar informações detalhadas de um filme, incluindo elenco, diretor(es) e gênero(s).

## RF11 – Geração de Relatórios de Público
O sistema deve gerar relatórios de público agrupados por sessão, por filme ou por cinema, exigindo obrigatoriamente um filtro de período (data início e data fim).
