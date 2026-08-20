
# Venn diagrams 
* https://mermaid.ai/open-source/syntax/venn.html

## Syntax

    Start with venn-beta.
    Use set for a single set name.
    Use union for an overlap of two or more set names.
    Identifiers in union must be defined by earlier set lines.
    Set identifiers can be bare words (A, Set_1) or quoted strings ("Foo Bar").

```mermaid
venn-beta
  set A["Alpha"]:20
    text A1["React"]
    text A2["Design Systems"]
  set B["Beta"]:12
  union A,B["AB"]:3
  style A fill:#ff6b6b
  style A,B color:#333
  style A1 color:red
```

    
```mermaid
venn-beta
  set A["Alpha"]:20
    text A1["React"]
    text A2["Design Systems"]
  set B["Beta"]:12
  union A,B["AB"]:3
  style A fill:#ff6b6b
  style A,B color:#333
  style A stroke: green
  style A1 color:red
  style AB fill-opacity:white
```


```mermaid
venn-beta
  set A["Alpha"]:20
    text A1["React"]
    text A2["Design Systems"]
  set B["Beta"]:5
  union A,B["AB"]:3
  style union A,B color:black
  style A fill:#ff6b6b
  style A,B color:#333
  style A stroke: green
  style A1 color:red
  style AB fill-opacity:white
```



```mermaid
venn-beta
  title "Team overlap"
  set Frontend
  set Backend
  union Frontend,Backend["APIs"]
```

```mermaid
---
config:
  htmlLabels: false
---
flowchart LR
    markdown["`This **is** _Markdown_`"]
    newLines["`Line1
    Line 2
    Line 3`"]
    markdown --> newLines

```
```mermaid
venn-beta
  title "Operaciones con conjuntos"
  set A
  set B
  set C
  union A,B
  union A,C
  union B,C
  union A,B,C
```
