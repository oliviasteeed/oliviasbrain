---
links: "[[My Areas]]"
tags:
  - area
---
```button
name QuickAdd: New Fleeting Note
type command
action QuickAdd: New Fleeting Note
```

## By Status
### No Status
```dataview
table created
from #thought AND !"Templates"
where (status !="🔴") and (status !="🟠") and (status !="🟡") and (status !="🟢")
sort created desc
```
### Backlog 🔴
Baby notes
```dataview
table created
from #thought AND !"Templates"
where status ="🔴"
sort created desc
```
### In Progress 🟡
Teenage notes
```dataview
table created
from #thought AND !"Templates"
where status ="🟡"
sort created desc
```
### Finished 🟢
Adult notes
```dataview
table created
from #thought AND !"Templates"
where status ="🟢"
sort created desc
```
