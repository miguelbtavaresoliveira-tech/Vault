---
tipo: painel
---

# Painel geral

## PRDs (os mais desatualizados primeiro)

```dataview
TABLE projeto, status, versao, atualizado
FROM "20-projetos"
WHERE tipo = "prd"
SORT atualizado ASC
```

## ADRs aguardando decisão

```dataview
TABLE projeto, data
FROM "20-projetos"
WHERE tipo = "adr" AND status = "proposta"
SORT data ASC
```

## ADRs aceitas nos últimos 30 dias

```dataview
TABLE projeto, data
FROM "20-projetos"
WHERE tipo = "adr" AND status = "aceita" AND data >= date(today) - dur(30 days)
SORT data DESC
```

## Tarefas abertas por projeto

```dataview
TASK
FROM "20-projetos"
WHERE !completed
GROUP BY file.link
```

## Conhecimento reutilizável (últimas notas)

```dataview
TABLE criado
FROM "30-conhecimento"
SORT criado DESC
LIMIT 10
```
