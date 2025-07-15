# Módulo 03 - Pacientes y Diagnósticos 🏥

## **Responsabilidades**
Modelo Patient completo, modelo Diagnosis, CRUD de pacientes, búsqueda de pacientes, gestión de diagnósticos y relación con historiales médicos.

## **Meta: Lograr MVC con APIs para React**

### **Model (Modelo)**
- [ ] **Patient Model**: Modelo completo de paciente con relaciones
- [ ] **Diagnosis Model**: Modelo de diagnósticos médicos
- [ ] **Patient-Diagnosis Relationship**: Relación muchos a muchos
- [ ] **Patient-History Relationship**: Relación con historiales

### **View (Vista/API)**
- [ ] **Patient Controllers**: CRUD completo de pacientes
- [ ] **Diagnosis Controllers**: Gestión de diagnósticos
- [ ] **Search Controllers**: Búsqueda avanzada de pacientes
- [ ] **API Resources**: Transformación de datos para React

### **Controller (Lógica de Negocio)**
- [ ] **Patient Services**: Lógica de gestión de pacientes
- [ ] **Diagnosis Services**: Lógica de diagnósticos
- [ ] **Search Services**: Búsqueda y filtros avanzados
- [ ] **Validation Services**: Validación de datos médicos

## **Archivos Incluidos**
```
03_patients_diagnoses/
├── patients/
│   ├── PatientController.php
│   ├── PatientService.php
│   ├── Patient.php (Model)
│   ├── PatientResource.php
│   ├── PatientCollection.php
│   └── Requests/ (StorePatientRequest, UpdatePatientRequest, SearchPatientsRequest)
└── diagnoses/
    ├── DiagnosisController.php
    ├── Diagnosis.php (Model)
    └── Requests/ (StoreDiagnosisRequest, UpdateDiagnosisRequest)
```

## **APIs a Desarrollar para React**
- `GET /api/patients` - Listar pacientes con paginación
- `POST /api/patients` - Crear nuevo paciente
- `GET /api/patients/{id}` - Obtener paciente específico
- `PUT /api/patients/{id}` - Actualizar paciente
- `DELETE /api/patients/{id}` - Eliminar paciente
- `GET /api/patients/search` - Búsqueda avanzada de pacientes
- `GET /api/patients/{id}/diagnoses` - Diagnósticos de un paciente
- `POST /api/patients/{id}/diagnoses` - Agregar diagnóstico a paciente
- `GET /api/diagnoses` - Listar diagnósticos
- `POST /api/diagnoses` - Crear diagnóstico
- `PUT /api/diagnoses/{id}` - Actualizar diagnóstico
- `DELETE /api/diagnoses/{id}` - Eliminar diagnóstico
- `GET /api/patients/statistics` - Estadísticas de pacientes

## **Tareas Específicas**
1. **CRUD de Pacientes**: Gestión completa de pacientes
2. **Sistema de Diagnósticos**: Diagnósticos médicos con categorías
3. **Búsqueda Avanzada**: Filtros por nombre, documento, edad, etc.
4. **Relaciones Médicas**: Paciente-Diagnóstico-Historial
5. **Validación Médica**: Validación de datos médicos
6. **Paginación**: Listado paginado con filtros
7. **Estadísticas**: Estadísticas de pacientes y diagnósticos
8. **Exportación**: Exportar datos a CSV/PDF

## **Campos del Modelo Patient**
- Documento de identidad
- Nombres y apellidos
- Fecha de nacimiento
- Género
- Dirección
- Teléfono
- Email
- Grupo sanguíneo
- Alergias
- Antecedentes médicos
- Contacto de emergencia

## **Campos del Modelo Diagnosis**
- Código de diagnóstico (CIE-10)
- Nombre del diagnóstico
- Descripción
- Categoría
- Severidad
- Tratamiento recomendado

## **Dependencias**
- Laravel Eloquent para relaciones
- Laravel Validation para requests médicos
- Laravel Resources para APIs
- Laravel Scout para búsqueda avanzada

## **Entregables**
- [ ] CRUD completo de pacientes
- [ ] Sistema de diagnósticos funcional
- [ ] Búsqueda avanzada implementada
- [ ] Relaciones médicas establecidas
- [ ] APIs documentadas y testeadas
- [ ] Validación médica robusta
- [ ] Integración con React lista
- [ ] Tests unitarios y de integración 