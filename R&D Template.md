---
"start date:": <% tp.date.now("YYYY-MM-DD") %>
"time:": <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
  - Research_and_development
content: <% tp.file.content %>
Template Tags: <% await tp.file.title %>
---

<%*
const prompt = await tp.system.prompt("Title:")
const title = await prompt
await tp.file.rename(title)
await tp.file.move("R&D/"+ title)
%>
# Goal


## Project Goals

```dataview
Task
FROM <%* tp.file.path(true) %> and #Project 
WHERE !fullyCompleted
SORT created DESC
Group by file.link
Sort rows.file.ctime DESC
```
