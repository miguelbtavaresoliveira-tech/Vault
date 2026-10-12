---
tipo: diario
data: <% tp.date.now("YYYY-MM-DD") %>
---

# <% tp.date.now("dddd, DD/MM/YYYY") %>

## Foco do dia (máx. 3)

- [ ] 
- [ ] 
- [ ] 

## Vencendo hoje ou atrasado

```tasks
not done
due before tomorrow
sort by due
```

## ADRs aguardando decisão

```dataview
TABLE projeto, data
FROM "20-projetos"
WHERE tipo = "adr" AND status = "proposta"
SORT data ASC
```

## Notas do dia

## Fechamento (2 min)

- O que avançou:
- O que travou:
- Primeira tarefa de amanhã:
