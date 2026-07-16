# 🤖 Cómo automatizo mi laburo con agentes IA

Comentaste **"todo"** 🙌

Acá te muestro cómo tengo armado el sistema para que la IA haga el trabajo pesado: orquestar agentes de código y generar contenido casi solo.

---

## 1. La base: contexto compartido con APC + orquestación con APX

Todos mis repos usan **APC (Agent Project Context)**, una convención abierta para guardar el contexto del proyecto para IA en una carpeta compartida `.apc/`. La idea es simple: *un proyecto, una sola capa de contexto* — en vez de duplicarlo entre `.claude/`, `.cursor/`, `.codex/`, etc.

- 🌐 Web: https://agentprojectcontext.com/
- 📦 Repo: https://github.com/agentprojectcontext/agentprojectcontext

Arriba de ese contexto uso **APX**: la capa práctica para operar **agentes, rutinas, MCPs, bridges de Telegram, tareas y automatizaciones**. Le delego un objetivo y coordina todo con un daemon local.

- 📦 Repo: https://github.com/agentprojectcontext/apx

La idea: yo defino el *qué*, y el sistema reparte el *cómo* entre los agentes.

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
