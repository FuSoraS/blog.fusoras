---
layout: ../../layouts/MarkdownLayout.astro
title: Mi configuracion de Visual Studio Code
Description:
author: FuSoraS
---
1. Precionar `Ctrl + Shift + p`
2. Escribir: `Open User Settings (JSON)`
3. Abrirlo y pegar estas línea de codigo
```json
{
	"editor.minimap.enabled": false,
	"editor.cursorBlinking":"expand",
	"editor.renderLineHighlight": "all",
	"editor.smoothScrolling": true,
	"files.autoSave": "afterDelay",
	"files.autoSaveDelay": 3000
}
```