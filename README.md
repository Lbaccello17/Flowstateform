# FlowState — Creator Research Form

Form de entrevistas de usuario para el producto FlowState.  
Deploy en Netlify con persistencia nativa de respuestas vía **Netlify Forms**.

---

## Deploy en 3 pasos

### 1. Subir a GitHub

```bash
git init
git add .
git commit -m "feat: creator research form"
git remote add origin https://github.com/TU_USUARIO/flowstate-research.git
git push -u origin main
```

### 2. Conectar en Netlify

1. Ir a [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**
2. Elegir GitHub → seleccionar el repo `flowstate-research`
3. Configuración de build:
   - **Base directory**: *(dejar vacío)*
   - **Publish directory**: `.`
   - **Build command**: *(dejar vacío)*
4. Click **Deploy site**

Netlify detecta automáticamente `data-netlify="true"` en el HTML y activa Forms.

### 3. Compartir el link

Una vez deployado, Netlify te da una URL del tipo:  
`https://flowstate-research.netlify.app`

Esa URL es la que mandás.

---

## Ver las respuestas

**Netlify Dashboard → Forms → creator-research**

Desde ahí podés:
- Ver cada submission individual
- **Exportar todo como CSV** (botón arriba a la derecha)
- Activar notificaciones por email por cada nuevo submit
- Conectar a Zapier / Make para enviar a Google Sheets automáticamente

---

## Límites plan gratuito Netlify

| | Free |
|---|---|
| Submissions / mes | 100 |
| Storage | 10MB |
| Export CSV | ✓ |
| Email notifications | ✓ |

Para escalar: plan Pro de Netlify ($19/mes) = submissions ilimitadas.

---

## Estructura del repo

```
flowstate-research/
├── index.html      ← el form completo
├── netlify.toml    ← config de build y headers
└── README.md       ← este archivo
```

---

## Stack

- HTML / CSS / JS puro — sin dependencias, sin frameworks
- Netlify Forms — backend serverless nativo
- Google Fonts: Geist (tipografía FlowState)
