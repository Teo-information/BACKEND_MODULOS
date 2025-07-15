# Módulo 05 - Citas y Estados 📅

## **Responsabilidades**
Modelo Appointment completo, modelo AppointmentStatus, CRUD de citas, filtros por fecha, estados de citas, calendario de citas, sistema de tickets y gestión de habitaciones.

## **Meta: Lograr MVC con APIs para React**

### **Model (Modelo)**
- [ ] **Appointment Model**: Modelo completo de cita con relaciones
- [ ] **AppointmentStatus Model**: Estados de citas (pendiente, confirmada, cancelada, etc.)
- [ ] **Ticket Model**: Sistema de tickets para citas
- [ ] **Room Model**: Gestión de habitaciones/consultorios

### **View (Vista/API)**
- [ ] **Appointment Controllers**: CRUD completo de citas
- [ ] **Status Controllers**: Gestión de estados de citas
- [ ] **Ticket Controllers**: Sistema de tickets
- [ ] **Calendar Controllers**: Calendario de citas
- [ ] **API Resources**: Transformación de datos para React

### **Controller (Lógica de Negocio)**
- [ ] **Appointment Services**: Lógica de gestión de citas
- [ ] **Status Services**: Lógica de estados
- [ ] **Ticket Services**: Lógica de tickets
- [ ] **Calendar Services**: Lógica de calendario
- [ ] **Validation Services**: Validación de horarios y disponibilidad

## **Archivos Incluidos**
```
05_appointments_status/
├── appointments/
│   ├── AppointmentController.php
│   ├── AppointmentService.php
│   ├── Appointment.php (Model)
│   ├── AppointmentStatusController.php
│   ├── AppointmentStatusService.php
│   ├── AppointmentStatus.php (Model)
│   └── Requests/ (StoreAppointmentRequest, UpdateAppointmentRequest, etc.)
├── tickets/
│   ├── TicketController.php
│   ├── TicketService.php
│   └── Requests/ (TicketRequest)
└── rooms/
    ├── RoomController.php
    ├── RoomService.php
    └── Room.php (Model)
```

## **APIs a Desarrollar para React**
- `GET /api/appointments` - Listar citas con paginación
- `POST /api/appointments` - Crear nueva cita
- `GET /api/appointments/{id}` - Obtener cita específica
- `PUT /api/appointments/{id}` - Actualizar cita
- `DELETE /api/appointments/{id}` - Eliminar cita
- `GET /api/appointments/calendar` - Calendario de citas
- `GET /api/appointments/by-date/{date}` - Citas por fecha
- `GET /api/appointments/by-therapist/{id}` - Citas por terapeuta
- `GET /api/appointments/by-patient/{id}` - Citas por paciente
- `PUT /api/appointments/{id}/status` - Cambiar estado de cita
- `GET /api/appointment-statuses` - Listar estados disponibles
- `POST /api/appointment-statuses` - Crear nuevo estado
- `GET /api/tickets` - Listar tickets
- `POST /api/tickets` - Crear ticket
- `GET /api/rooms` - Listar habitaciones
- `POST /api/rooms` - Crear habitación
- `GET /api/appointments/statistics` - Estadísticas de citas

## **Tareas Específicas**
1. **CRUD de Citas**: Gestión completa de citas médicas
2. **Sistema de Estados**: Estados de citas con transiciones
3. **Calendario de Citas**: Vista de calendario con filtros
4. **Sistema de Tickets**: Tickets para seguimiento de citas
5. **Gestión de Habitaciones**: Consultorios y disponibilidad
6. **Validación de Horarios**: Verificación de disponibilidad
7. **Filtros Avanzados**: Por fecha, terapeuta, paciente, estado
8. **Notificaciones**: Recordatorios de citas
9. **Estadísticas**: Estadísticas de citas y ocupación

## **Campos del Modelo Appointment**
- Paciente (relación)
- Terapeuta (relación)
- Fecha y hora
- Duración
- Estado (pendiente, confirmada, cancelada, completada)
- Tipo de consulta
- Habitación/consultorio
- Observaciones
- Precio
- Ticket asociado

## **Campos del Modelo AppointmentStatus**
- Nombre del estado
- Color (para UI)
- Descripción
- Es final (boolean)
- Permite cancelación (boolean)

## **Estados de Citas**
- Pendiente (amarillo)
- Confirmada (verde)
- En progreso (azul)
- Completada (gris)
- Cancelada (rojo)
- No asistió (naranja)

## **Dependencias**
- Laravel Eloquent para relaciones
- Laravel Validation para requests
- Laravel Resources para APIs
- Carbon para manejo de fechas
- Laravel Notifications para recordatorios

## **Entregables**
- [ ] CRUD completo de citas
- [ ] Sistema de estados funcional
- [ ] Calendario de citas implementado
- [ ] Sistema de tickets operativo
- [ ] Gestión de habitaciones establecida
- [ ] Validación de horarios robusta
- [ ] APIs documentadas y testeadas
- [ ] Integración con React lista
- [ ] Tests unitarios y de integración 