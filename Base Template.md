---
"start date:": <% tp.date.now("YYYY-MM-DD") %>
"time:": <% tp.date.now("YYYY-MM-DD HH:mm") %>
tags:
  - "#Base"
content: <% tp.file.content %>
Template Tags: 
---
<%*
const prompt = await tp.system.prompt("Title:")
const title = await prompt
await tp.file.rename(title)
%> 

