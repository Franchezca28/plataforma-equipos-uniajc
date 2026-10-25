# Descripción detallada de los casos de uso (v01)

Extraído del documento TG1, numeral 3.3.5. Diagrama en MOD_casos_de_uso_v01.png.

CU01 - Crear y gestionar proyecto

**Actor(es): **Coordinador

**Propósito: **Registrar y mantener datos generales de un proyecto.

**Precondiciones: **Usuario identificado.

**Flujo normal: **Seleccionar crear proyecto; ingresar datos; confirmar; validar; registrar.

**Alternativas: **Solicitar datos faltantes.

**Excepciones: **Ante fallo de persistencia no se crea.

**Resultado esperado: **Proyecto registrado y asociado al coordinador.

**Requisitos: **RF01, RF08

CU02 - Gestionar equipo

**Actor(es): **Coordinador

**Propósito: **Definir integrantes del proyecto.

**Precondiciones: **Proyecto existente y permisos de coordinador.

**Flujo normal: **Abrir proyecto; acceder a equipo; seleccionar integrantes; confirmar.

**Alternativas: **Retirar integrante cuando corresponda.

**Excepciones: **Bloquear modificación sin permisos.

**Resultado esperado: **Equipo actualizado.

**Requisitos: **RF02, RF16

CU03 - Asignar tarea

**Actor(es): **Coordinador

**Propósito: **Registrar una tarea y asignarla a un integrante.

**Precondiciones: **Proyecto y equipo existentes.

**Flujo normal: **Nueva tarea; ingresar datos; seleccionar responsable; confirmar.

**Alternativas: **Ajustar datos antes de confirmar.

**Excepciones: **Rechazar responsable ajeno al equipo.

**Resultado esperado: **Tarea creada y asignada.

**Requisitos: **RF03

CU04 - Actualizar tarea y registrar avance

**Actor(es): **Integrante

**Propósito: **Mantener estado y avance de tareas.

**Precondiciones: **Tarea existente y permiso de actualización.

**Flujo normal: **Abrir tarea; modificar estado o avance; confirmar; validar; guardar.

**Alternativas: **Actualizar solo estado cuando corresponda.

**Excepciones: **Rechazar porcentaje fuera de 0-100.

**Resultado esperado: **Tarea y avance actualizados.

**Requisitos: **RF04, RF05

CU05 - Consultar progreso

**Actor(es): **Integrante / coordinador

**Propósito: **Visualizar tareas, responsables, estados y progreso.

**Precondiciones: **Usuario pertenece al proyecto.

**Flujo normal: **Abrir proyecto; consultar tareas/avances; calcular indicador; presentar resumen.

**Alternativas: **Filtrar por estado o responsable.

**Excepciones: **Si no hay tareas, informar que no hay datos suficientes.

**Resultado esperado: **Vista actualizada del proyecto.

**Requisitos: **RF06, RF07

CU06 - Consultar participación y carga

**Actor(es): **Integrante / coordinador / docente

**Propósito: **Hacer visible el reparto del trabajo y la contribución de cada integrante.

**Precondiciones: **Al menos una tarea asignada en el proyecto.

**Flujo normal: **Abrir el proyecto; acceder a participación; consultar carga y contribución relativas por integrante y la referencia 1/n; revisar la señal de desequilibrio.

**Alternativas: **Si no hay tareas completadas, mostrar solo la carga.

**Excepciones: **Equipo de un solo integrante: no se muestra comparación.

**Resultado esperado: **Reparto del trabajo visible para todos.

**Requisitos: **RF09, RF10

CU07 - Recibir alertas de riesgo

**Actor(es): **Integrante / coordinador / docente (activado por el sistema)

**Propósito: **Anticipar retrasos y desequilibrios de carga.

**Precondiciones: **Reglas de alerta activas y tareas con fecha límite.

**Flujo normal: **El sistema evalúa A1, A2 y A3 periódicamente; si una regla se cumple, genera la alerta; notifica; el usuario la consulta y la marca como atendida.

**Alternativas: **Una regla desactivada no genera alertas.

**Excepciones: **Si falla el envío por correo, la alerta se conserva en la plataforma y se reintenta.

**Resultado esperado: **Alerta registrada y notificada.

**Requisitos: **RF11

CU08 - Configurar umbrales

**Actor(es): **Coordinador / docente

**Propósito: **Ajustar la sensibilidad de las reglas de alerta y de desequilibrio.

**Precondiciones: **Proyecto existente y permisos de coordinador o docente.

**Flujo normal: **Abrir configuración; editar umbral de desequilibrio, horas de anticipación y avance esperado; confirmar.

**Alternativas: **Restaurar los valores por defecto.

**Excepciones: **Rechazar valores fuera de rango.

**Resultado esperado: **Reglas actualizadas.

**Requisitos: **RF12

CU09 - Consultar panel docente y exportar reporte

**Actor(es): **Docente

**Propósito: **Dar seguimiento a varios equipos y documentar el avance.

**Precondiciones: **Docente vinculado a uno o más proyectos.

**Flujo normal: **Abrir el panel; ver avance, tareas vencidas y alertas por equipo; entrar al detalle de un equipo; elegir PDF o CSV; descargar el reporte.

**Alternativas: **Filtrar por proyecto o equipo.

**Excepciones: **Sin proyectos vinculados: mensaje informativo. Si falla la generación del reporte, informar y permitir reintento.

**Resultado esperado: **Estado de los equipos visible y reporte descargado.

**Requisitos: **RF13, RF14

CU10 - Evaluar a pares

**Actor(es): **Integrante

**Propósito: **Aportar una valoración del proceso del equipo.

**Precondiciones: **El docente activó la evaluación.

**Flujo normal: **Abrir la evaluación; calificar a cada compañero de 1 a 5; comentar (opcional); enviar.

**Alternativas: **Guardar como borrador.

**Excepciones: **Una evaluación ya enviada no se puede editar.

**Resultado esperado: **Valoraciones visibles solo para el docente.

**Requisitos: **RF15

