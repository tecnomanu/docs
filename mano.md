# 🖐️ Controlá el cursor con la mano

Comentaste **"mano"** 🙌

Acá va el repo del proyectito: **controlar el cursor de tu Mac con gestos de la mano**, usando la webcam y sin ningún hardware extra.

> ⚠️ Es un **proyecto experimental** — más para jugar y aprender que para producción. Pero está bueno para meter mano (nunca mejor dicho) en visión por computadora.

👉 **Repo:** https://github.com/tecnomanu/control-cursor-with-hand

---

## Qué hace
Movés la mano y el cursor sigue el punto entre el índice y el pulgar. Los gestos disparan clicks:

| Gesto | Acción |
|---|---|
| Mover la mano | Mover el cursor |
| Pinza índice + pulgar | Click izquierdo / arrastrar |
| Doble pinza índice + pulgar | Doble click |
| Dedo medio + pulgar | Click del medio / scroll |
| Anular + pulgar (sostenido) | Click derecho |
| Meñique + pulgar (tap) | Click derecho rápido |

Además tiene un **glow** translúcido que sigue la mano (cambia de color según el gesto), preview de la cámara con el esqueleto de la mano, e ícono en la barra de menú.

## Cómo está hecho
- **[MediaPipe](https://mediapipe.dev/)** para el tracking de la mano
- **PyQt5** para el overlay del glow
- **Quartz** (nativo de macOS) para el input del mouse pixel-perfect

## Requisitos
- **macOS** (Apple Silicon o Intel, Sonoma 14+)
- **Python 3.9 – 3.11** (MediaPipe todavía no soporta 3.12+)
- Webcam

## Instalación
```bash
git clone https://github.com/tecnomanu/control-cursor-with-hand.git
cd control-cursor-with-hand
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
```

Si te copa el proyecto, una ⭐ me ayuda un montón 🙌
Y si lo mejorás o le agregás gestos, mandá un PR 😉
