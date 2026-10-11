# Box-Drawing Input 

As an alternative to indentation, you can use box-drawing characters to define the tree structure. The parser auto-detects the format — no extra keyword or config is needed. This is how most file tree diagrams are drawn already, so you can turn those into Mermaid diagrams with very little effort.

Both standard (`├──`, `└──`, `│`) and heavy (`┣━━`, `┗━━`, `┃`) Unicode variants are supported.

##### Code:

```
treeView-beta
├── src/
│   ├── index.ts
│   └── utils.ts
├── package.json
└── README.md
```



```mermaid
treeView-beta
├── src/
│   ├── index.ts
│   └── utils.ts
├── package.json
└── README.md

```







Depth is inferred from the column position of the branch character, so deeper nesting works naturally:

##### Code:

```
treeView-beta
├── packages/
│   ├── mermaid/
│   │   ├── src/
│   │   │   ├── parser.ts
│   │   │   └── renderer.ts
│   │   └── package.json
│   └── parser/
│       └── src/
└── README.md
```



```mermaid
treeView-beta
├── packages/
│   ├── mermaid/
│   │   ├── src/
│   │   │   ├── parser.ts
│   │   │   └── renderer.ts
│   │   └── package.json
│   └── parser/
│       └── src/
└── README.md

```

**Note:** If a parse error occurs, line numbers in the error message refer to your original input. Tab characters are automatically expanded to spaces.