# 🤖 Cómo automatizo mi laburo con agentes IA

Comentaste **"todo"** 🙌

Acá te muestro cómo tengo armado el sistema para que la IA haga el trabajo pesado: orquestar agentes de código y generar contenido casi solo.

---

## 1. El cerebro: orquestar agentes con APX

En vez de saltar entre mil herramientas, uso **APX** como capa que **orquesta varios agentes/CLIs de código** (Claude Code, Codex, Gemini, etc.) desde un solo lugar. Le delego un objetivo, corre **rutinas** y coordina todo con un **daemon local**.

La idea: yo defino el *qué*, y el sistema reparte el *cómo* entre los agentes.

> ⚙️ *Si querés que arme una guía/repo público de APX para que lo puedas probar, avisame y lo subo.*

---

## 2. Generar contenido en serie (para hacerme publicidad casi solo)

Con dos proyectos open source cierro el círculo de "crear una vez, mostrar muchas":

### 🎬 framevox — videos publicitarios
Videos promocionales con composiciones **HyperFrames** + **voz IA** (Gemini, Piper, ElevenLabs).
👉 https://github.com/tecnomanu/framevox

### 📹 video-docs-builder — tutoriales automáticos
Graba el navegador con Playwright, le pone **narración TTS** (Piper/ElevenLabs/OpenAI) y arma el MP4 con FFmpeg. Ideal para mostrar una app sin grabar a mano.
👉 https://github.com/tecnomanu/video-docs-builder

---

## 3. El combo completo
1. **APX** orquesta a los agentes que construyen y documentan el proyecto.
2. **video-docs-builder** genera el tutorial en video.
3. **framevox** arma la pieza publicitaria con voz IA.
4. Publico, y sigo con lo siguiente.

Menos tareas manuales, más foco en construir.

Si te copa alguno de los repos, una ⭐ me ayuda un montón 🙌
Y si querés que profundice en alguna parte, escribime y lo vemos.
