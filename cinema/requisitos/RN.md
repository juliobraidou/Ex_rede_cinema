# Regras de Negócio – Rede de Cinemas

## RN01 – Intervalo mínimo entre sessões
Deve haver um intervalo mínimo configurável entre o término de uma sessão e o início da próxima na mesma sala. O valor padrão é **30 minutos** e é armazenado na entidade `ConfiguracaoSistema`. Esse intervalo é somado à duração do filme na validação de conflito de horário.

## RN02 – Capacidade da sala
O total de espectadores registrado em uma sessão não pode ser superior à capacidade máxima da sala onde a sessão ocorre.

## RN03 – Registro de público não negativo
O total de espectadores informado deve ser um valor inteiro maior ou igual a zero.

## RN04 – Sessão vinculada a filme ativo
Só é possível cadastrar uma sessão para filmes que estejam com `status = ativo` no sistema. Filmes inativos não podem receber novas sessões.

## RN05 – Duração obrigatória do filme
Todo filme deve ter o campo `duracao_min` preenchido. Esse valor é obrigatório para o cálculo do término da sessão e para a validação de conflitos de horário.

## RN06 – Unicidade de sala por horário
Uma sala não pode ter duas sessões com horários sobrepostos. O período ocupado por uma sessão é calculado como:

```
inicio_sessao  até  inicio_sessao + duracao_filme + intervalo_minimos
```

## RN07 – Tipo de participação obrigatório
Toda associação entre `Pessoa` e `Filme` (entidade `RoleFilme`) deve ter o campo `tipo_role` preenchido (ex: ator, diretora, produtor). O campo `personagem` é obrigatório apenas quando `tipo_role = ator`.

## RN08 – Relatório exige período
Todo relatório de público deve exigir data de início e data de fim. Não é permitida a geração de relatório sem filtro de período definido.
