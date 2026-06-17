# Exentia Panel

Panel privado del equipo de Exentia Spa & Beauty Salon. Inicio de sesión con cuenta de GHL.

## Flujo

1. Terapeuta abre el panel → si no tiene sesión activa, ve botón "Iniciar sesión"
2. Click → redirige a GHL OAuth (`marketplace.gohighlevel.com/oauth/chooselocation`)
3. Logueado en GHL, autoriza la app → GHL regresa con `?code=` a n8n
4. n8n intercambia code por access_token, valida que sea Exentia, obtiene info del usuario y firma un JWT
5. n8n redirige al panel con `?token=JWT`
6. Panel guarda el JWT en localStorage y muestra los datos del terapeuta

## Hosting

GitHub Pages — `https://0VictorRodriguez0.github.io/exentia-panel/`

## Stack

HTML + CSS + JS vanilla. Sin build, sin dependencias.
