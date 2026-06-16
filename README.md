# QuoteBox Automation

Sistema de automatización completo para QuoteBox, construido con n8n y Google Sheets.

## ¿Qué hace el sistema?

- **Scraping con login** — accede a la plataforma con credenciales, recorre todas las páginas y extrae frases por tags configurables
- **Storage idempotente** — guarda las frases en Google Sheets sin duplicados, verificado con múltiples corridas
- **Detección de novedades** — compara contra el storage existente y manda un email de resumen agrupado por tag solo cuando hay frases nuevas
- **Bot de WhatsApp** — responde consultas por autor en lenguaje natural ("¿Cuántas frases hay de Einstein?", "¿Cuáles son?")
- **Registro de autores desconocidos** — cuando el autor no existe, responde amigablemente y registra la consulta con contador acumulado

## Stack

- **Workflow engine:** n8n (self-hosted)
- **Storage:** Google Sheets
- **Notificaciones:** Gmail
- **WhatsApp:** Twilio Sandbox
- **Lenguaje:** JavaScript (nodos Code de n8n)

## Estructura del repo
quotebox-automation/

├── workflows/

│   ├── quotebox_scraping.json       # Scraping + storage + email

│   └── quotebox_whatsapp_bot.json   # Bot de WhatsApp

└── DECISIONES.md                    # Documento de decisiones técnicas


## Demo

🎥 [Ver Loom](https://www.loom.com/share/10f84fc52f394198bf1ed820acb10348)

