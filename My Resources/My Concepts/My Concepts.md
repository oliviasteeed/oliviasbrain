---
links: "[[My Second Brain <3]]"
---
```button
name QuickAdd: New Concept Note
type command
action QuickAdd: New Concept Note
```

## By Status
### No Status
```dataview
table created
from #concept AND !"Templates"
where (status !="🔴") and (status !="🟠") and (status !="🟡") and (status !="🟢")
sort created desc
```
### Backlog 🔴
Baby notes
```dataview
table created
from #concept AND !"Templates"
where status = "🔴"
sort created desc
```
### In Progress 🟡
Teenage notes
```dataview
table created
from #concept AND !"Templates"
where status = "🟡"
sort created desc
```
### Finished 🟢
Adult notes
```dataview
table created
from #concept AND !"Templates"
where status = "🟢"
sort created desc
```
