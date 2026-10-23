<!-- l10n-sync: source-file="workshop/04-design-vibes.md" -->
# Parte 4: Tematización orientada al diseño

---

En esta parte, usarás los ciclos de planificación e implementación de Copilot para diseñar una transformación completa del tema. Este enfoque empieza por el diseño: define una visión, itera sobre los elementos visuales y deja que Copilot se encargue del trabajo pesado de CSS.

## Tarea 1: Planifica el tema retro

<!-- track:vscode:start -->
Cambia a modo **Plan** en GitHub Copilot Chat.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Ejecuta `/plan` en GitHub Copilot CLI o pulsa **Shift+Tab** hasta activar el modo plan.
<!-- track:cli:end -->

Escribe este prompt:

> Quiero transformar esta página en una experiencia completa de arcade retro. Planifica una renovación visual que incluya: efectos de líneas de barrido CRT en el fondo, un resplandor de neón pulsante en el título, una insignia VS animada con cambios de color en el degradado, una capa brillante y reluciente sobre las tarjetas de resultados de usuario, animaciones de entrada flotante para los campos, texto de carga que alterne entre verde y morado, y efectos de resplandor al pasar el cursor por los cuadrados de contribuciones. Mantén el fondo oscuro (`#0a0a1a`) y los colores de acento verde (`#5fed83`) y morado (`#8a2be2`). Usa un tema oscuro con la fuente retro Press Start 2P de Google Fonts.

Copilot generará un plan detallado que abarcará todos los efectos visuales. **No lo aceptes de inmediato**: revísalo e itera:

- Sugiere ajustes en la duración de las animaciones (por ejemplo: *«Haz que el pulso de neón sea más lento, de unos 3 segundos»*).
- Pregunta por efectos concretos (por ejemplo: *«¿Cómo funcionará el efecto brillante de las tarjetas?»*).
- Pide que cambie el enfoque si algo no te convence.

## Tarea 2: Implementa el tema

Cuando estés conforme con el plan, pide a Copilot que lo implemente:

> Implementa el plan del tema de arcade retro que acabamos de diseñar.

Copilot añadirá varias animaciones CSS, pseudoelementos y transiciones a la hoja de estilos. Podría incluir:

- `@keyframes` para líneas de barrido, pulso de neón, brillo y animaciones de entrada flotante
- Pseudoelementos (`::before`, `::after`) para efectos de superposición
- Propiedades personalizadas de CSS para los colores del tema
- Transiciones y estados al pasar el cursor por elementos interactivos

<!-- track:cli:start -->
Cuando se apliquen los cambios, usa `/diff` para revisar los estilos antes de aprobarlos.
<!-- track:cli:end -->

## Tarea 3: Ajusta los detalles visuales

> **⚠️ ¿No ves los cambios?** Si no aparecen el nuevo tema o las animaciones, detén el servidor (`Ctrl+C`), reinícialo con `npm run dev` y fuerza la recarga del navegador (`Ctrl+Shift+R`).

Mantén abierta la vista previa en el navegador e itera sobre el diseño. Prueba prompts como:

> El efecto de líneas de barrido es demasiado intenso; reduce la opacidad a 0.03.

> Añade un parpadeo eléctrico sutil al título.

> La insignia VS debería pulsar de forma más llamativa.

Este es un enfoque de **desarrollo orientado al diseño**: iteras sobre el resultado visual en tiempo real. Cada prompt refina la experiencia hasta que tenga el aspecto adecuado. No te conformes con algo simplemente aceptable: lleva el diseño hasta que parezca propio de una máquina recreativa.

## Tarea 4: Actualiza las instrucciones

Tus instrucciones deben reflejar las decisiones importantes de diseño para mantener la coherencia en los prompts posteriores.

<!-- track:vscode:start -->
Pide a Copilot Chat:

> Añade a `copilot-instructions.md` una sección de guía de diseño que describa el tema de arcade retro: colores, fuentes y estilo de animación.
<!-- track:vscode:end -->

<!-- track:cli:start -->
Pide a Copilot CLI:

> Actualiza las instrucciones del repositorio con una breve guía de diseño para el tema de arcade retro: colores, fuentes, estilo de animación y la regla de que la nueva interfaz debe mantener la estética de neón.
<!-- track:cli:end -->

Cuando la página tenga el aspecto deseado, haz commit de las instrucciones actualizadas y de los cambios de diseño.

## ✅ Parte 4 completada

**Lo que has aprendido:**

- Usar flujos de planificación para esbozar un **sistema de diseño antes de implementarlo**
- **Iterar sobre el resultado visual** con prompts de seguimiento
- **Actualizar las instrucciones después de tomar decisiones importantes** para mantener una identidad visual coherente
