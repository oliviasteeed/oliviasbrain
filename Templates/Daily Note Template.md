---
tags:
  - dailynote
week: '[[ <% tp.date.now("YYYY-[W]WW") %> ]]'
created: <% tp.date.now("YYYY-MM-DD") %>
---
## Tasks
- [ ] 
## Journal
- 
### New Notes
```dataview
list
from ""
where contains(created, "<%tp.file.title%>")
sort file.mtime desc
```
## Reflection
- 