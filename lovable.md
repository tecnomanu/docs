# 🚀 Publicá GRATIS tu web de Lovable en tu dominio .com.ar

Comentaste **"PUBLICAR"** 🙌 Acá va el paso a paso para tomar una web hecha con **Lovable** (o cualquier app con IA) y dejarla online, con tu propio dominio `.com.ar` y HTTPS, sin pagar hosting.

La idea: Lovable te da el código → vos lo deployás en un servidor propio con **Dokploy** (open source, tipo "Vercel casero") → apuntás tu dominio → listo.

---

## Lo que vas a necesitar
- Tu proyecto en **Lovable** (o el repo que te genera).
- Un **servidor** (una VPS barata, o incluso una máquina en tu casa con Docker).
- **Dokploy** instalado en ese servidor (1 comando).
- Un dominio **.com.ar** (se registra gratis en NIC Argentina si tenés CUIT/CUIL).

---

## Paso 1 — Sacá el código de Lovable
En Lovable, conectá el proyecto a **GitHub** (botón *GitHub → Connect*). Eso te crea un repo con el código de tu web. Anotá la URL del repo.

## Paso 2 — Instalá Dokploy en tu servidor
Entrá por SSH a tu servidor y corré:

```bash
curl -sSL https://dokploy.com/install.sh | sh
```

Cuando termina, te da un panel web en `http://IP-DE-TU-SERVIDOR:3000`. Creá tu usuario admin ahí.

## Paso 3 — Creá la app en Dokploy
1. En el panel: **Create Application**.
2. Fuente: **GitHub** → elegí el repo que te creó Lovable.
3. Build: la mayoría de las webs de Lovable son **Nixpacks** o **Dockerfile** (Dokploy lo detecta solo). Si es una app Vite/React, el build suele ser `npm run build` y sirve la carpeta `dist`.
4. **Deploy**. En un par de minutos tenés la web corriendo en una URL interna.

## Paso 4 — Conectá tu dominio .com.ar
1. Registrá/entrá a tu dominio en **NIC.ar**.
2. Apuntá un registro **A** de tu dominio a la **IP de tu servidor**.
   *(Para `www`, un CNAME al dominio raíz.)*
3. En Dokploy → tu app → **Domains** → agregá `tudominio.com.ar` y activá **HTTPS (Let's Encrypt)**. Dokploy saca el certificado solo.

## Paso 5 — Probá
Esperá unos minutos a que propague el DNS y entrá a `https://tudominio.com.ar`. 🎉

---

## Tips
- ¿No tenés servidor? Una VPS de ~5 USD/mes alcanza y sobra para varias webs.
- Cada vez que hagas push al repo (desde Lovable o a mano), Dokploy puede **redeployar solo** (activá auto-deploy).
- Guardá este doc: el mismo flujo te sirve para **cualquier** app, no solo Lovable.

¿Te trabaste en algún paso? Respondeme el DM y lo destrabamos 🙌
