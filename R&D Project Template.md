---
"start date:": <% tp.date.now("YYYY-MM-DD") %>
"time:": <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
  - Research_and_development
  - Project
content: <% tp.file.content %>
Template Tags:
---
<%*
const prompt = await tp.system.prompt("Title:")
const title = await prompt
await tp.file.rename(title)
%>

# Goal

```meta-bind-button
label: New Project File
hidden: false
class: ""
tooltip: ""
id: Project File
style: default
actions:
  - type: command
    command: workspace:new-tab
  - type: templaterCreateNote
    templateFile: Merk hilfe/Template/R&D Project File Template.md
    folderPath: "<%* tp.file.path(true)+title %>"
    fileName: ""
    openNote: true

```

## To do


```dataview
Task
FROM <%* tp.file.path(false) %>
WHERE !fullyCompleted
SORT created DESC
Group by file.link
Sort rows.file.ctime DESC
```
