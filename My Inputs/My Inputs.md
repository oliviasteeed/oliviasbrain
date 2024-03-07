---
links: "[[My Second Brain <3]]"
---
```button
name QuickAdd: New Input Note
type command
action QuickAdd: New Input Note
```

## By Status
### No Status
```dataview
table created
from #input AND !"Templates"
where (status !="🔴") and (status !="🟠") and (status !="🟡") and (status !="🟢")
sort created desc
```
### Backlog 🔴
Needs processing
```dataview
table created
from #input AND !"Templates"
where status= "🔴"
sort created desc
```
### Reading 🟠
```dataview
table created
from #input AND !"Templates"
where status = "🟠"
sort created desc
```
### Note Making 🟡
Currently processing into atomic notes
```dataview
table created
from #concept AND !"Templates"
where status = "🟡"
sort created desc
```
### Finished 🟢
```dataview
table created
from #input AND !"Templates"
where status = "🟢"
sort created desc
```


## By Type
### Books
```dataview
table created
from #input/book and !"Templates"
sort created desc
```
### Articles
```dataview
table created, status
from #input/article AND !"Templates"
sort Created desc
```
### Podcasts
```dataview
table created, status
from #input/podcast AND !"Templates"
sort Created desc
```
### Videos
```dataview
table created, status
from #input/video AND !"Templates"
sort Created desc
```
### GetAbstract
```dataview
table created, status
from #input/getabstract  AND !"Templates"
sort Created desc
```
