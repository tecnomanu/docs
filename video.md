# 🎬 Cómo hago videos publicitarios con IA

Si llegaste acá es porque comentaste **"video"** en Instagram. Bienvenido 🙌
Este es el detrás de escena de cómo armo los videos que ves en la cuenta, con dos caminos según lo que quieras lograr.

---

## 1. El video "imposible" → Veo 3

El reel donde un personaje 100% virtual habla a cámara está hecho con **Veo 3** (Google DeepMind). La clave: Veo 3 **genera el video y la voz en un mismo prompt**, así que no tenés que grabar audio aparte ni sincronizar nada.

### Cómo estructurar el prompt

Pensá el prompt en 4 capas y ponelas todas juntas:

1. **Personaje**: quién es, cómo se ve, qué acento tiene.
2. **Escena / cámara**: dónde está, plano, luz.
3. **Acción**: qué hace mientras habla.
4. **Diálogo**: el texto exacto que querés que diga (entre comillas).

### Plantilla que uso

```text
A [descripción física del personaje] with a [acento/tono] accent,
sitting in [locación], [tipo de plano y luz].
He/She looks at the camera and says, in a natural conversational tone:
"[Acá va el guion textual, cortito, 1-2 frases]".
Realistic lighting, subtle head movement, cinematic, 16:9.
```

### Ejemplo real (estilo del reel)

```text
A friendly Latino man in his 30s with a Colombian "paisa" accent,
sitting in a sunny modern living room, medium shot, soft daylight.
He looks straight at the camera and says, in a relaxed confident tone:
"¿En serio pensás que esto lo grabé de verdad? Todo esto lo hizo una IA".
Natural micro-expressions, realistic lighting, cinematic, vertical 9:16.
```

**Tips que me sirvieron:**
- Guiones **cortos** (5–8 segundos de habla). Si es largo, dividilo en varias tomas.
- El **acento** cambia todo: pedilo explícito ("paisa", "rioplatense", etc.).
- Generá **2–3 variantes** del mismo prompt y quedate con la mejor toma.
- Para vertical (reels) pedí `9:16`; para YouTube, `16:9`.

---

## 2. Para escalar y hacerlo repetible → 2 herramientas open source

Veo 3 es genial para la toma "wow", pero cuando querés **volumen** o **videos de producto/tutorial**, uso estos dos proyectos míos (son gratis, y si te sirven me ayudás un montón con una ⭐):

### 🅰️ framevox — videos publicitarios
Arma videos promocionales con composiciones **HyperFrames** + **voz IA** (Gemini, Piper o ElevenLabs). Ideal para reels de producto o marketing con narración.

👉 https://github.com/tecnomanu/framevox

### 🅱️ video-docs-builder — tutoriales automáticos
Genera videos-tutorial solos: **graba el navegador** con Playwright, le pone **narración TTS** (Piper/ElevenLabs/OpenAI) y arma el MP4 con FFmpeg. Perfecto para documentar una app sin grabar a mano.

👉 https://github.com/tecnomanu/video-docs-builder

---

### ¿Por dónde empezar?
- Querés una toma con "actor" IA → **Veo 3**.
- Querés reels de producto en serie → **framevox**.
- Querés documentar/mostrar una app → **video-docs-builder**.

Cualquier duda, respondeme el DM y lo vemos 🙌
