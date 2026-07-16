# ✅ Mi setup de la TODO List de Cursor (con prompts)

Comentaste **"todo"** 🙌 Acá te dejo cómo uso la **TODO List del agente de Cursor**: la función donde el agente **arma la lista de tareas de una feature y las va tildando solo** mientras programa. Menos alt-tab entre editor y gestor de tareas, más foco en la lógica.

---

## Qué es
Cuando le pedís al **Agent** de Cursor algo que tiene varios pasos, arma una **lista de to-dos** en el panel y la va marcando en tiempo real a medida que completa cada parte. Lo bueno: la lista queda **atada a tu código**, no en un post-it aparte.

Para que aparezca sí o sí, el truco es **pedírselo explícito** en el prompt.

---

## Setup en 3 pasos

### 1. Activá el modo Agent
Abrí el chat (`⌘/Ctrl + L`) y pasá el chat a modo **Agent** (arriba del input). Ese modo es el que planifica y ejecuta por pasos.

### 2. Pedile el plan como TODO (el prompt clave)
No arranques con "hacé X". Arrancá pidiendo el plan:

```text
Antes de tocar código, armá una TODO list con los pasos necesarios
para [describí la feature]. Mostrámela y esperá mi OK.
Después ejecutá los pasos uno por uno y andá tildando cada ítem
a medida que lo terminás.
```

Así te muestra la lista, la aprobás, y recién ahí ejecuta tildando en vivo.

### 3. Mantené la lista viva
Mientras trabaja, si algo cambia:

```text
Actualizá la TODO: marcá lo hecho, agregá los pasos nuevos que
descubriste y dejá pendientes los que faltan.
```

---

## Prompts que uso seguido

**Para features nuevas:**
```text
Actuá como tech lead. Descomponé "[feature]" en una TODO list de
tareas chicas y verificables (máximo ~7). Ordenalas por dependencia.
No escribas código hasta que apruebe la lista.
```

**Para bugs:**
```text
Armá una TODO para reproducir, aislar y arreglar este bug.
Primer ítem: reproducirlo con un test que falle. Último ítem:
que el test pase. Tildá a medida que avanzás.
```

**Para refactors grandes:**
```text
Hacé una TODO de refactor incremental: cada ítem tiene que dejar
el proyecto compilando y los tests en verde. Nada de cambios masivos
de una. Andá tildando y avisá si algún paso rompe algo.
```

---

## Por qué me cambió el flujo
- El plan queda **a la vista** y lo apruebo antes de que toque nada.
- Si me distraigo, **retomo** viendo qué quedó tildado.
- Es una forma barata de que el agente **no se mande cambios de más**: se ata a la lista.

Guardá el reel para tu próxima sesión de codeo, y si te sirvió pasáselo a alguien que todavía vive pegado a los post-its 😉

¿Dudas? Respondeme el DM 🙌
