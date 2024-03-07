---
created: <% tp.date.now("YYYY-MM-DD") %>
tags:
  - reviews/weekly
links: '[[<% tp.date.now("YYYY-[M]M") %>]]'
---
[[Calendar/WeeklyNotes/<% moment(tp.file.title, "YYYY-[W]WW").add(-1, 'weeks').format("YYYY-[W]WW") %>|<% moment(tp.file.title, "YYYY-[W]WW").add(-1, 'weeks').format("YYYY-[W]WW") %>]] ⬅️ [[Calendar/MonthlyNotes/<% moment(tp.file.title,'YYYY-[W]WW').format('YYYY-[M]MM') %>|<% moment(tp.file.title,'YYYY-[W]WW').format('YYYY-[M]MM') %>]] ➡️ [[Calendar/WeeklyNotes/<% moment(tp.file.title, "YYYY-[W]WW").add(1, 'weeks').format("YYYY-[W]WW") %>|<% moment(tp.file.title, "YYYY-[W]WW").add(1, 'weeks').format("YYYY-[W]WW") %>]]

mantra
### Focus/Priorities
- 
### Goals/Opportunities
- 
### Tasks
- [ ] 
### Avoid
- 
## Weekly Notes Recap
### Days
```dataview
table Summary
from [[]] AND "My Agenda/Daily Notes"
sort file.name asc
```
### New Notes Created
```dataview
TABLE Tags as Note_Type, created
from "" and !"Templates"
WHERE contains(created, "YYYY-MM-DD") OR   
contains(created, "YYYY-MM-DD") OR 
contains(created, "YYYY-MM-DD") OR 
contains(created, "YYYY-MM-DD8") OR 
contains(created, "YYYY-MM-DD") OR 
contains(created, "YYYY-MM-DD") OR
contains(created, "YYYY-MM-DD")

SORT created asc
```
## Reflection

### Review
Summary::

Focus (compared to intentions)
- 
Worries and Obstacles
- 
Opportunities
- 
Realizations/Learning
- 
Appreciation
- 
Next Time
- 
