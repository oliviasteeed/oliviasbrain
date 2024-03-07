---
links: "[[My Second Brain <3]]"
---
```button
name QuickAdd: New Project Note
type command
action QuickAdd: New Project Note
```

## By Status
### No Status
```dataview
table created
from #project AND !"Templates"
where (status !="🔴") and (status !="🟠") and (status !="🟡") and (status !="🟢") and (status !="🔵")
sort created desc
```
### Ongoing 🔵
```dataview
table created
from #project AND !"Templates"
where status= "🔵"
sort created desc
```
### Conceptual 🔴
```dataview
table created
from #project AND !"Templates"
where status= "🔴"
sort created desc
```
### In Progress 🟡
```dataview
table created
from #project AND !"Templates" 
where status= "🟡"
sort created desc
```
### Finished 🟢
```dataview
table created
from #project AND !"Templates" 
where status= "🟢"
sort created desc
```
