---
"start date:": <% tp.date.now("YYYY-MM-DD") %>
"time:": <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
  - Service
content: <% tp.file.content %>
---

<%*
const prompt = await tp.system.prompt("Title:")
const title = await prompt
await tp.file.rename(title)
await tp.file.move("Service/"+ title)
%>


```meta-bind-button
label: Bronze Client
hidden: false
class: ""
tooltip: ""
id: Bronze Client
style: default
actions:
  - type: command
    command: workspace:new-tab
  - type: templaterCreateNote
    templateFile: Merk hilfe/Template/Bronze Client Template.md
    folderPath: Service/Clients/Bronze Package
    fileName: ""
    openNote: true

```


```meta-bind-button
label: Silver Client
hidden: false
class: ""
tooltip: ""
id: Silver Client
style: default
actions:
  - type: command
    command: workspace:new-tab
  - type: templaterCreateNote
    templateFile: Merk hilfe/Template/Silver Client Template.md
    folderPath: Service/Clients/Silver Package
    fileName: ""
    openNote: true

```

# Goal

- [ ] 

## To do

```dataview
Task
FROM "Service/Clients" and #Service  
WHERE !fullyCompleted
SORT modified DESC
Group by file.link
Sort rows.file.modified DESC
```