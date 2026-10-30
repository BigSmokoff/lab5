---
tags: [dataview, metadata, query]
---
# Dataview запросы для САПР

Заметки в обсидиан удобно фильтровать через плагин Dataview. 

### Активные проекты по решателю
```dataview
TABLE status
FROM "03 Проекты"
WHERE contains(tags, "solver") OR contains(tags, "cad")
```

### Математическая база
```dataview
LIST
FROM "01 Заметки"
WHERE contains(tags, "math") OR contains(tags, "algorithms")
SORT file.name ASC
```

Такие запросы позволяют быстро ориентироваться в концепциях, когда нужно связать теорию из [[Книга А.В. Столярова Введение в профессию]] с прикладными задачами вроде вычисления [[Матрица Якоби для системы ограничений]].