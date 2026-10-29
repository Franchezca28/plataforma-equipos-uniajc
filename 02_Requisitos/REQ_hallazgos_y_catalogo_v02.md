# Hallazgos y catálogo de requisitos (v02)

Extraído del documento TG1 v04, numerales 3.3.2 y 3.3.3. Incluye regla del negocio y datos involucrados en cada requisito funcional.

3.3.2 Registro de Hallazgos y Necesidades

H01

**Fuente: **Anteproyecto + entrevista simulada

**Actor: **Integrante

**Necesidad: **Consultar tareas, responsables y fechas en un solo lugar.

**Problema observado: **La información puede quedar distribuida en varios medios.

**Supuesto: **Acceso desde navegador.

H02

**Fuente: **Anteproyecto + Kim et al. (2015)

**Actor: **Coordinador

**Necesidad: **Crear un proyecto y organizar integrantes.

**Problema observado: **No existe una vista única del equipo y proyecto.

**Supuesto: **Un proyecto tiene coordinador.

H03

**Fuente: **Anteproyecto + entrevista simulada

**Actor: **Coordinador

**Necesidad: **Asignar tareas con responsable, fecha y estado.

**Problema observado: **Responsabilidades poco claras.

**Supuesto: **Una tarea tiene responsable principal.

H04

**Fuente: **Albarracín et al. (2019) + entrevista simulada

**Actor: **Integrante

**Necesidad: **Actualizar tarea y registrar avance.

**Problema observado: **La gestión manual reduce trazabilidad.

**Supuesto: **El avance queda asociado a la tarea.

H05

**Fuente: **Rodríguez Vásquez & Rodríguez Hernández (2023)

**Actor: **Integrante / coordinador

**Necesidad: **Consultar progreso general.

**Problema observado: **La fragmentación dificulta conocer el estado global.

**Supuesto: **Progreso calculado con tareas y avances.

H06

**Fuente: **ISO/IEC 25010

**Actor: **Todos

**Necesidad: **Usabilidad, seguridad y rendimiento adecuados.

**Problema observado: **Un sistema difícil o inseguro reduce utilidad.

**Supuesto: **Se comprobará con pruebas posteriores.

H07

**Fuente: **Anteproyecto + Hall & Buzwell (2013)

**Actor: **Integrante / coordinador / docente

**Necesidad: **Ver cómo se reparte la carga y la contribución entre los integrantes.

**Problema observado: **El aporte desigual (free-riding) es difícil de detectar a tiempo.

**Supuesto: **La participación se mide con las tareas y avances registrados; es un apoyo y no una calificación.

H08

**Fuente: **Anteproyecto + entrevista simulada

**Actor: **Integrante / coordinador / docente

**Necesidad: **Recibir avisos cuando una tarea o el proyecto estén en riesgo de retraso.

**Problema observado: **Los retrasos se descubren cuando la fecha ya venció.

**Supuesto: **Las tareas tienen fecha límite y estado actualizado.

H09

**Fuente: **Kim et al. (2015) + Dillenbourg et al. (2009)

**Actor: **Docente

**Necesidad: **Ver el estado de cada equipo durante el proceso y exportar un reporte.

**Problema observado: **El docente suele ver el producto final y no el proceso del equipo.

**Supuesto: **El docente está vinculado a los proyectos que acompaña.

H10

**Fuente: **Benning (2022) + entrevista simulada

**Actor: **Integrante / docente

**Necesidad: **Registrar una evaluación breve entre pares.

**Problema observado: **No hay evidencia del proceso interno del equipo.

**Supuesto: **El docente activa la evaluación (es opcional).

H11

**Fuente: **Análisis comparativo de herramientas existentes

**Actor: **Docente / integrante

**Necesidad: **Contar con rol docente e indicadores académicos de participación.

**Problema observado: **Las herramientas de propósito general no están pensadas para el aula.

**Supuesto: **El comparativo usa información pública y se confirma con la documentación oficial.

3.3.3 Catálogo Priorizado de Requisitos

Los hallazgos se transforman en requisitos funcionales y no funcionales numerados. La prioridad se define como alta o media según su relación con el alcance mínimo del producto y se establecen criterios de aceptación verificables para fases posteriores.

RF01 - Funcional

**Actor: **Coordinador

**Especificación: **Crear proyecto con nombre, descripción, estado y fechas de inicio y fin. Datos: Proyecto, Usuario.

**Regla del negocio: **Solo un usuario con rol de coordinador crea proyectos, y la fecha de fin no puede ser anterior a la de inicio.

**Restricción: **Nombre obligatorio.

**Prioridad: **Alta** | Fuente: **H02

**Criterio de aceptación: **Con datos válidos, el proyecto se crea y aparece en el listado.

RF02 - Funcional

**Actor: **Coordinador

**Especificación: **Gestionar integrantes del equipo. Datos: Equipo, Usuario, Proyecto.

**Regla del negocio: **Cada equipo trabaja en un único proyecto, y un usuario puede integrar más de un equipo.

**Restricción: **Solo el coordinador modifica el equipo.

**Prioridad: **Alta** | Fuente: **H02

**Criterio de aceptación: **Los integrantes activos aparecen asociados al proyecto.

RF03 – Funcional

**Actor: **Coordinador

**Especificación: **Crear y asignar tareas con responsable, fecha, estado y complejidad (1 a 5 puntos). Datos: Tarea, Usuario, Proyecto.

**Regla del negocio: **Toda tarea nueva inicia en estado «Pendiente» y tiene un único responsable.

**Restricción: **El responsable pertenece al equipo.

**Prioridad: **Alta** | Fuente: **H03

**Criterio de aceptación: **La tarea queda visible con responsable, fecha, estado y complejidad.

RF04 - Funcional

**Actor: **Integrante

**Especificación: **Actualizar el estado de una tarea asignada. Datos: Tarea, Usuario.

**Regla del negocio: **Solo el responsable de la tarea cambia su estado.

**Restricción: **El estado debe pertenecer al conjunto definido.

**Prioridad: **Alta** | Fuente: **H01-H04

**Criterio de aceptación: **La vista refleja el nuevo estado.

RF05 - Funcional

**Actor: **Integrante

**Especificación: **Registrar avance con fecha, porcentaje y observación. Datos: Avance, Tarea.

**Regla del negocio: **Cada avance queda asociado a una tarea y conserva su fecha; los avances anteriores no se sobrescriben.

**Restricción: **El porcentaje debe estar entre 0 y 100.

**Prioridad: **Alta** | Fuente: **H04

**Criterio de aceptación: **El avance queda guardado y consultable.

RF06 - Funcional

**Actor: **Todos

**Especificación: **Consultar tareas indicando estado, responsable y fecha. Datos: Tarea, Usuario, Proyecto.

**Regla del negocio: **El estado, el responsable y la fecha límite de cada tarea se muestran siempre juntos en la consulta.

**Restricción: **Solo se muestran proyectos asociados al usuario.

**Prioridad: **Alta** | Fuente: **H01

**Criterio de aceptación: **La consulta muestra los datos mínimos definidos.

RF07 - Funcional

**Actor: **Todos

**Especificación: **Consultar progreso general usando tareas y avances. Datos: Proyecto, Tarea, Avance.

**Regla del negocio: **El progreso general se calcula con el mismo criterio para todos los proyectos y se actualiza cuando cambia el estado o el avance de una tarea.

**Restricción: **Debe utilizarse un criterio de cálculo único.

**Prioridad: **Alta** | Fuente: **H05

**Criterio de aceptación: **Se muestra un indicador coherente con los datos registrados.

RF08 - Funcional

**Actor: **Coordinador

**Especificación: **Editar datos y cerrar el proyecto al finalizar. Datos: Proyecto, Tarea, Avance.

**Regla del negocio: **Un proyecto cerrado deja de aceptar nuevas tareas, pero conserva las existentes y sus avances.

**Restricción: **Debe conservar tareas y avances.

**Prioridad: **Media** | Fuente: **Anteproyecto

**Criterio de aceptación: **Los cambios válidos se guardan sin perder trazabilidad.

RF09 - Funcional

**Actor: **Todos

**Especificación: **Calcular y mostrar el índice de participación de cada integrante (carga relativa y contribución relativa). Datos: Tarea, Avance, Usuario, Indicador de participación.

**Regla del negocio: **El índice se calcula por integrante ponderando las tareas por su complejidad (1 a 5).

**Restricción: **Debe aplicarse la regla de cálculo documentada en este numeral y ser visible para todos los integrantes.

**Prioridad: **Alta** | Fuente: **H07

**Criterio de aceptación: **Con un caso de prueba calculado manualmente, los valores mostrados coinciden con una tolerancia de 0,01.

RF10 - Funcional

**Actor: **Todos

**Especificación: **Mostrar la distribución de la carga del equipo y señalar un desequilibrio cuando la diferencia respecto de la participación equitativa (1/n) supere el umbral configurado. Datos: Indicador de participación, Umbral, Usuario.

**Regla del negocio: **Hay desequilibrio cuando la diferencia entre la participación de un integrante y 1/n supera el umbral configurado (0,20 por defecto).

**Restricción: **El umbral por defecto es 0,20 y debe ser configurable.

**Prioridad: **Alta** | Fuente: **H07

**Criterio de aceptación: **Con un equipo de 3 integrantes y umbral 0,20, un integrante con más del 53,3 % de la carga se marca como desequilibrio.

RF11 - Funcional

**Actor: **Sistema (notifica a integrante, coordinador y docente)

**Especificación: **Generar alertas tempranas de riesgo de retraso según las reglas A1, A2 y A3 y notificarlas. Datos: Alerta, Tarea, Proyecto, Usuario.

**Regla del negocio: **Las alertas se generan con las reglas A1 (vencimiento próximo), A2 (avance del proyecto inferior al 70 % del esperado) y A3 (carga relativa por encima del umbral).

**Restricción: **Las reglas se evalúan de forma periódica y la alerta se conserva en la plataforma aunque falle otro medio de envío.

**Prioridad: **Alta** | Fuente: **H08

**Criterio de aceptación: **Una tarea con vencimiento en 48 horas o menos y estado distinto de «Hecha» genera la alerta A1 y se notifica al responsable; un proyecto con avance menor al 70 % del esperado genera la alerta A2; y un integrante cuya carga relativa supera el umbral configurado genera la alerta A3. En los tres casos la alerta queda registrada en la plataforma.

RF12 - Funcional

**Actor: **Coordinador / Docente

**Especificación: **Configurar los umbrales de las reglas de alerta y de desequilibrio. Datos: Umbral, Proyecto.

**Regla del negocio: **Solo el coordinador y el docente vinculado modifican los umbrales, y el cambio aplica a las evaluaciones posteriores.

**Restricción: **Los valores deben estar dentro de rangos permitidos.

**Prioridad: **Media** | Fuente: **H07, H08

**Criterio de aceptación: **Un valor fuera de rango se rechaza; un valor válido se aplica a los cálculos siguientes.

RF13 - Funcional

**Actor: **Docente

**Especificación: **Presentar un panel con el estado de cada equipo: avance, tareas vencidas y alertas activas. Datos: Proyecto, Equipo, Tarea, Alerta.

**Regla del negocio: **Una tarea se considera vencida cuando su fecha límite pasó y no está terminada.

**Restricción: **El docente ve únicamente los proyectos a los que está vinculado.

**Prioridad: **Alta** | Fuente: **H09

**Criterio de aceptación: **Un docente vinculado a dos proyectos ve solo esos dos, con avance, tareas vencidas y alertas.

RF14 - Funcional

**Actor: **Docente

**Especificación: **Exportar un reporte de avance y participación por equipo en PDF o CSV. Datos: Proyecto, Tarea, Avance, Indicador de participación.

**Regla del negocio: **El reporte se genera por equipo y se descarga en el formato elegido por el docente.

**Restricción: **El reporte refleja los datos vigentes al momento de exportar.

**Prioridad: **Media** | Fuente: **H09, H11

**Criterio de aceptación: **El archivo exportado contiene los mismos datos que muestra el panel en ese momento.

RF15 - Funcional

**Actor: **Integrante

**Especificación: **Registrar una evaluación breve entre pares (puntaje de 1 a 5 y comentario opcional) cuando el docente la active. Datos: Evaluación entre pares, Usuario, Proyecto.

**Regla del negocio: **Cada integrante evalúa una sola vez a cada compañero por periodo de evaluación.

**Restricción: **Las valoraciones individuales solo las ve el docente.

**Prioridad: **Media** | Fuente: **H10

**Criterio de aceptación: **Tras enviarla, solo el docente puede consultarla y el integrante no puede editarla.

RF16 - Funcional

**Actor: **Coordinador

**Especificación: **Vincular un docente al proyecto. Datos: Proyecto, Usuario.

**Regla del negocio: **Un proyecto puede tener más de un docente vinculado, y un docente puede estar vinculado a varios proyectos.

**Restricción: **Solo pueden vincularse usuarios con rol de docente.

**Prioridad: **Media** | Fuente: **H09

**Criterio de aceptación: **Al vincular un docente, el proyecto aparece en su panel.

RNF01 - No funcional

**Actor: **Todos

**Especificación: **Usabilidad: navegación comprensible y etiquetas claras.

**Restricción: **La aplicación debe ser web responsiva.

**Prioridad: **Alta** | Fuente: **ISO/IEC 25010

**Criterio de aceptación: **En la prueba de usabilidad se obtiene una puntuación SUS igual o superior a 68 y una tasa de éxito del 80 % o más en las tareas principales (Brooke, 1996).

RNF02 - No funcional

**Actor: **Todos

**Especificación: **Seguridad: restringir acciones según rol y proteger proyectos.

**Restricción: **No se deben exponer proyectos ajenos.

**Prioridad: **Alta** | Fuente: **ISO/IEC 25010 + Ley 1581

**Criterio de aceptación: **El 100 % de los casos de prueba de permisos definidos bloquea las acciones no autorizadas.

RNF03 - No funcional

**Actor: **Todos

**Especificación: **Rendimiento adecuado en operaciones habituales.

**Restricción: **Se medirá en ambiente de prueba.

**Prioridad: **Media** | Fuente: **ISO/IEC 25010

**Criterio de aceptación: **El 95 % de las consultas habituales (tablero principal, detalle de proyecto y detalle de tarea) responde en 3 segundos o menos en el ambiente de prueba, con los datos de prueba definidos.

RNF04 - No funcional

**Actor: **Todos

**Especificación: **Accesibilidad: legibilidad, contraste y navegación consistente.

**Restricción: **Uso en navegador.

**Prioridad: **Media** | Fuente: **Anteproyecto + ISO/IEC 25010

**Criterio de aceptación: **El texto principal tiene una relación de contraste mínima de 4,5:1 y las pantallas principales pueden recorrerse con el teclado, verificado con una lista de comprobación sin barreras críticas.

RNF05 - No funcional

**Actor: **Equipo técnico

**Especificación: **Mantenibilidad: componentes separados y código versionado.

**Restricción: **Debe existir historial real en Git.

**Prioridad: **Media** | Fuente: **Pressman & Maxim (2020)

**Criterio de aceptación: **La estructura del repositorio separa interfaz, lógica y datos, y el historial permite revisar los cambios de ambos integrantes mediante mensajes descriptivos.

RNF06 - No funcional

**Actor: **Equipo técnico / Todos

**Especificación: **Adecuación funcional: el cálculo del índice y de las alertas debe producir los resultados esperados.

**Restricción: **Se verificará con casos de prueba calculados manualmente.

**Prioridad: **Alta** | Fuente: **ISO/IEC 25010 + H07

**Criterio de aceptación: **Al menos el 95 % de los casos de prueba definidos coinciden con el resultado esperado.

RNF07 - No funcional

**Actor: **Todos

**Especificación: **Seguridad y privacidad: el detalle individual de las evaluaciones entre pares y de los indicadores solo se muestra a quienes corresponde según su rol.

**Restricción: **El tratamiento de datos debe ser conforme a la Ley 1581 de 2012.

**Prioridad: **Alta** | Fuente: **H10 + Ley 1581

**Criterio de aceptación: **Las pruebas de permisos confirman que un integrante no accede a las valoraciones individuales de otros.

Reglas preliminares del índice y de las alertas

Las siguientes reglas son una definición preliminar que se refinará en la segunda fase, durante el diseño. Sea n el número de integrantes del equipo.

• Puntos asignados (PA) y puntos completados (PC). PA de un integrante es la suma de los puntos de complejidad de las tareas que tiene asignadas. PC es la suma de los puntos de las tareas que completó: una tarea terminada a tiempo aporta el 100 % de sus puntos y una terminada con retraso aporta el 50 %.

• Carga relativa (CR) y contribución relativa (CT). CR = PA del integrante dividido por la suma de PA del equipo. CT = PC del integrante dividido por la suma de PC del equipo. La participación equitativa de referencia es 1/n.

• Desequilibrio. Se señala cuando |CR − 1/n| o |CT − 1/n| superan el umbral u, que por defecto es 0,20 y es configurable.

• Alerta A1. Tarea con vencimiento en 48 horas o menos y estado distinto de «Hecha».

• Alerta A2. Proyecto cuyo avance (puntos completados sobre puntos totales) es menor al 70 % del avance esperado de forma lineal según sus fechas de inicio y fin.

• Alerta A3. Desequilibrio de carga de un integrante según el umbral u.

