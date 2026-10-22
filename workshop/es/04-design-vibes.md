<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización orientada al diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Es un enfoque de desarrollo orientado al diseño: empieza con una visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia al modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Usa `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo de planificación.
<!-- track:cli:end -->

Escribe este prompt:

> Quiero transformar esta página en una experiencia de arcade retro completa. Planifica una renovación visual integral que incluya: efectos de líneas de escaneo CRT en el fondo, un brillo de neón en el título que pulse como un letrero, una insignia VS animada con cambios de color en el degradado, una superposición brillante/iridiscente en las tarjetas de resultados de usuario, animaciones de entrada flotante para los campos, texto de carga que cambie de verde a morado y efectos de brillo al pasar el cursor sobre los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) y los colores de acento verde (`#5fed83`) y morado (`#8a2be2`). Usa un tema oscuro con la fuente de juegos retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado de implementación que cubre todos los efectos visuales. **No lo aceptes de inmediato**: revisa el plan e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo: «Haz que el pulso de neón sea más lento, de unos 3 segundos»).
- Pregunta por efectos concretos (por ejemplo: «¿Cómo funcionará la superposición iridiscente de las tarjetas?»).
- Pide cambios en el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés satisfecho con el plan, pide a Copilot que lo implemente.

> Implementa el plan del tema de arcade retro que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a la hoja de estilos. Esto puede incluir:

- `@keyframes` para líneas de escaneo, pulso de neón, brillo iridiscente y efectos de entrada flotante.
- Pseudoelementos (`::before`, `::after`) para efectos de superposición.
- Propiedades personalizadas de CSS para los colores del tema.
- Transiciones y estados al pasar el cursor para los elementos interactivos.

<!-- track:cli:start -->
Cuando terminen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta los detalles visuales

> **⚠️ ¿No ves los cambios?** Si el tema o las animaciones no aparecen, detén el servidor de desarrollo (`Ctrl+C`), reinícialo con `npm run dev` y fuerza la actualización del navegador (`Ctrl+Shift+R`).

Mantén abierta la vista previa del navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de escaneo es demasiado intenso; reduce la opacidad a 0.03.

> Añade un sutil parpadeo eléctrico al texto del título.

> La insignia VS debería pulsar con más intensidad.

Este es un enfoque de **desarrollo orientado al diseño**: iteras sobre el resultado visual en tiempo real. Cada prompt refina la experiencia hasta que encaje. No te conformes con «suficientemente bueno»: perfecciona el diseño hasta que la página parezca propia de una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deberían reflejar las decisiones de diseño importantes para mantenerlas presentes en los prompts posteriores.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Añade a copilot-instructions.md una sección de guía de diseño que describa nuestro tema de arcade retro: colores, fuentes y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Actualiza las instrucciones del repositorio con una breve guía de diseño para el tema de arcade retro: colores, fuentes, estilo de animación y la regla de que las nuevas interfaces mantengan la estética de neón.
<!-- track:cli:end -->

Cuando la página se vea bien, haz commit de las instrucciones actualizadas y los cambios de diseño.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para esbozar un **sistema de diseño antes de implementarlo**.
- **Iterar sobre el resultado visual** con prompts de seguimiento rápidos.
- **Actualizar las instrucciones tras tomar decisiones importantes** para mantener la identidad visual.
