# ✅ PENDIENTES DEL PROYECTO ALMA IA - FRONTEND

Este documento lista las tareas pendientes en el frontend de React, organizadas por módulos y prioridades, con referencias directas a los archivos involucrados y las acciones a realizar.

---

## 🔺 PRIORIDAD ALTA

### 1.4 Alumnos
- [ ] **Ir a opción Alertas: al pinchar la alerta para ir al detalle se cae**
  - Archivos: `app/alumnos/[id]/page.tsx`, `components/student/student-alerts.tsx`
  - Acción: Asegurar que el `alumno_alerta_id` del backend se mapee correctamente a la propiedad `id` de la interfaz `Alert` en `alertsData` antes de pasarlo a `StudentAlerts`.

### 1.5 Comparativo
- [ ] **Falta gráfico de líneas al final**
  - Archivos: `app/comparativo/page.tsx`, servicios de datos comparativos
  - Acción: Conectar los componentes de gráfico (`BarChartComparison`, `LineChartComparison`) a endpoints reales y agregar el gráfico de líneas si falta.

### 1.3 Home

- [ ] **Gráfico central debe ser de patologías, no emociones**
  - Archivo: `app/page.tsx`
  - Acción: Renombrar título y ajustar datos (`apiEmotions`) → Requiere nuevo endpoint.
    
### 1.8 Alertas (Grilla y Creación)
- [ ] **Grilla debe estar ordenada por fecha y hora descendente**
  - Archivos: `app/alertas/page.tsx`, `components/data-table.tsx`
  - Acción: Implementar lógica de ordenamiento.
- [ ] **Falta tipo de alerta Roja**
  - Archivo: `components/student/add-alert-modal.tsx`
  - Acción: Asegurar que esté habilitado el tipo de alerta “Roja”.
- [ ] **Falta opción para ingresar hora manual**
  - Archivo: `components/student/add-alert-modal.tsx`
  - Acción: Añadir campo de hora editable, con valor por defecto solo si no se especifica.

---

## ⚠️ PRIORIDAD MEDIA

### 1.1 Login
- [ ] **“Olvidaste contraseña”**
  - Archivo: `app/(auth)/login/page.tsx`
  - Acción: Implementar funcionalidad completa y su ruta `/forgot-password`.

### 1.2 Selector de Colegios
- [ ] **Validar funcionamiento con múltiples usuarios**
  - Archivos: `app/select-school/page.tsx`, `services/school-service.ts`

### 1.6 Informes
- [ ] **Descarga falla**
  - Archivo: `app/informes/page.tsx`
  - Acción: Depurar función de descarga.
- [ ] **Cambiar título botón a "Informe"**
- [ ] **Estilizar botón de descarga**

### 1.7 Perfil
- [ ] **Validar correo electrónico**
- [ ] **Cambiar imagen**
- [ ] **Evitar fechas de nacimiento futuras**
- [ ] **Si URL refiere a archivo, usar input tipo `file`**
- [ ] **Cambio de contraseña con checkbox para mostrar inputs**
- [ ] **Refrescar pantalla anterior al guardar (incluye cabecera)**
  - Archivos: `app/perfil/page.tsx`, `components/header.tsx`, servicios de perfil

---

## 🔻 PRIORIDAD BAJA

### 1.3 Home
- [ ] **Campanita de alertas muestra todas, no solo pendientes**
  - Archivos: `components/recent-alerts.tsx`, `services/home-service.ts`
  - Acción: Ajustar `fetchRecentAlerts` para que acepte filtro de estado o sea filtrado en backend.
- [ ] **"Alertas recientes" no se actualiza con el colegio**
  - Archivos: `components/recent-alerts.tsx`, `services/home-service.ts`, `lib/api-config.ts`
  - Acción: Asegurar que `fetchRecentAlerts` reciba `colegio_id`.
- [ ] **Fechas importantes desde la fecha actual**
  - Archivos: `components/important-dates.tsx`, `services/home-service.ts`
- [ ] **Gráfico de anillos con filtro: semana, mes, año**
  - Archivo: `app/page.tsx`
  - Acción: Implementar dropdown para elegir periodo.
- [ ] **Campanita animada si hay alertas pendientes**
  - Archivo: `components/recent-alerts.tsx`
  - Acción: Agregar animación CSS condicional.
- [ ] **Mejorar fondo y logo**
  - Archivos: CSS, `app/(auth)/login/page.tsx`, layouts

---

## 🔧 MOTORES (BACKEND)

Estos puntos son responsabilidad del backend, pero son críticos para el correcto funcionamiento del frontend.

- [ ] **Motor de Preguntas**
  - Auditoria (Pendiente Inicio Proceso, termino de proceso, cantidad de registrados procesados, control de error, correo envio a casilla de equipo tècnico)
- [ ] **Motor de Alertas**
  - Amarillas (Pendiente revisar dias consecutivos y feriados)
  - Naranjas
  - Rojas
  - Inactividad (Pendiente implementar)
  - Auditoria (Pendiente Inicio Proceso, termino de proceso, cantidad de registrados procesados, control de error, correo envio a casilla de equipo tècnico)
- [ ] **Motor de Informes**
  - Gustos
  - Alumnos por mes
  - Colegio
  - Cursos
  - Nivel

---

> ✳️ Notas:
> - Se recomienda priorizar tareas de la sección "Alta" para garantizar la funcionalidad base.
> - Las tareas de prioridad baja pueden implementarse progresivamente una vez se estabilicen las funcionalidades clave.
