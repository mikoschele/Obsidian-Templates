---
"start date:": <% tp.date.now("YYYY-MM-DD") %>
"time:": <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
  - Research_and_development
  - Project
  - File
content: <% tp.file.content %>
Template Tags:
---
<%*
const prompt = await tp.system.prompt("Title:")
const title = await prompt
await tp.file.rename(title)
%>

```meta-bind-button
label: New Note
hidden: false
class: ""
tooltip: ""
id: New Note
style: default
actions:
  - type: command
    command: workspace:new-tab
  - type: templaterCreateNote
    templateFile: Merk hilfe/Template/Base Template.md
    folderPath: "<%* await tp.file.path(true)%>/Notes"
    fileName: ""
    openNote: true

```

## To do

- [ ] 

