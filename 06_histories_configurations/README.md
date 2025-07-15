# Módulo 06 - Historiales y Configuraciones 📋

## **Responsabilidades**
Modelo History, modelos de configuración (DocumentType, PaymentType, PredeterminedPrice), CRUD de historiales, gestión de configuraciones y relación con pacientes.

## **Meta: Lograr MVC con APIs para React**

### **Model (Modelo)**
- [ ] **History Model**: Modelo completo de historial médico
- [ ] **DocumentType Model**: Tipos de documentos
- [ ] **PaymentType Model**: Tipos de pago
- [ ] **PredeterminedPrice Model**: Precios predeterminados
- [ ] **History-Patient Relationship**: Relación con pacientes

### **View (Vista/API)**
- [ ] **History Controllers**: CRUD completo de historiales
- [ ] **DocumentType Controllers**: Gestión de tipos de documento
- [ ] **PaymentType Controllers**: Gestión de tipos de pago
- [ ] **PredeterminedPrice Controllers**: Gestión de precios
- [ ] **API Resources**: Transformación de datos para React

### **Controller (Lógica de Negocio)**
- [ ] **History Services**: Lógica de gestión de historiales
- [ ] **DocumentType Services**: Lógica de tipos de documento
- [ ] **PaymentType Services**: Lógica de tipos de pago
- [ ] **PredeterminedPrice Services**: Lógica de precios
- [ ] **Validation Services**: Validación de datos médicos

## **Archivos Incluidos**
```
06_histories_configurations/
├── histories/
│   ├── HistoryController.php
│   ├── HistoryService.php
│   ├── History.php (Model)
│   └── Requests/ (StoreHistoryRequest, UpdateHistoryRequest)
└── configurations/
    ├── DocumentTypeController.php
    ├── DocumentTypeService.php
    ├── DocumentType.php (Model)
    ├── PaymentTypeController.php
    ├── PaymentTypeService.php
    ├── PaymentType.php (Model)
    ├── PredeterminedPricesController.php
    ├── PredeterminedPriceService.php
    ├── PredeterminedPrice.php (Model)
    └── Requests/ (StoreDocumentTypeRequest, UpdatePaymentTypeRequest, etc.)
```

## **APIs a Desarrollar para React**
- `GET /api/histories` - Listar historiales con paginación
- `POST /api/histories` - Crear nuevo historial
- `GET /api/histories/{id}` - Obtener historial específico
- `PUT /api/histories/{id}` - Actualizar historial
- `DELETE /api/histories/{id}` - Eliminar historial
- `GET /api/histories/by-patient/{id}` - Historiales por paciente
- `GET /api/document-types` - Listar tipos de documento
- `POST /api/document-types` - Crear tipo de documento
- `PUT /api/document-types/{id}` - Actualizar tipo de documento
- `DELETE /api/document-types/{id}` - Eliminar tipo de documento
- `GET /api/payment-types` - Listar tipos de pago
- `POST /api/payment-types` - Crear tipo de pago
- `PUT /api/payment-types/{id}` - Actualizar tipo de pago
- `DELETE /api/payment-types/{id}` - Eliminar tipo de pago
- `GET /api/predetermined-prices` - Listar precios predeterminados
- `POST /api/predetermined-prices` - Crear precio predeterminado
- `PUT /api/predetermined-prices/{id}` - Actualizar precio
- `DELETE /api/predetermined-prices/{id}` - Eliminar precio

## **Tareas Específicas**
1. **CRUD de Historiales**: Gestión completa de historiales médicos
2. **Sistema de Configuraciones**: Tipos de documento, pago y precios
3. **Relaciones Médicas**: Historial-Paciente-Diagnóstico
4. **Validación Médica**: Validación de datos de historiales
5. **Paginación**: Listado paginado con filtros
6. **Exportación**: Exportar historiales a PDF
7. **Búsqueda**: Búsqueda en historiales médicos
8. **Estadísticas**: Estadísticas de historiales y configuraciones

## **Campos del Modelo History**
- Paciente (relación)
- Terapeuta (relación)
- Fecha de consulta
- Motivo de consulta
- Diagnóstico
- Tratamiento
- Observaciones
- Próxima cita
- Estado del historial
- Archivos adjuntos

## **Campos del Modelo DocumentType**
- Código de documento
- Nombre del documento
- Descripción
- Es obligatorio (boolean)
- Formato de validación

## **Campos del Modelo PaymentType**
- Código de pago
- Nombre del tipo de pago
- Descripción
- Es activo (boolean)
- Comisión (porcentaje)

## **Campos del Modelo PredeterminedPrice**
- Nombre del servicio
- Descripción
- Precio base
- Duración
- Categoría
- Es activo (boolean)

## **Dependencias**
- Laravel Eloquent para relaciones
- Laravel Validation para requests médicos
- Laravel Resources para APIs
- DomPDF para exportación de PDF
- Laravel Storage para archivos adjuntos

## **Entregables**
- [ ] CRUD completo de historiales
- [ ] Sistema de configuraciones funcional
- [ ] Relaciones médicas establecidas
- [ ] Exportación de PDF implementada
- [ ] APIs documentadas y testeadas
- [ ] Validación médica robusta
- [ ] Integración con React lista
- [ ] Tests unitarios y de integración 