# EDO Core

**Enterprise Development & Operations (EDO) Core** es un framework de gobernanza, operación y automatización diseñado para construir ecosistemas de trabajo escalables, auditables y asistidos por Inteligencia Artificial.

---

## 🎯 Manifiesto

EDO no existe para producir contenido.

EDO existe para diseñar y operar los sistemas que producen contenido, conocimiento, documentación, activos y procesos de forma consistente, reproducible y verificable.

```text
Sistema → Proceso → Automatización → Producción
```

Nunca en el orden inverso.

---

## 💡 Problema que Resuelve

La mayoría de los proyectos complejos fallan por:

* Información duplicada.
* Automatizaciones inconsistentes.
* Prompts imposibles de mantener.
* Ausencia de trazabilidad.
* Dependencia excesiva del conocimiento tácito.

EDO Core proporciona una arquitectura común para evitar estos problemas mediante gobernanza, inventarios, workflows y automatización estructurada.

---

## 🧠 Principios Fundamentales

### Single Source of Truth (SSOT)

Cada entidad posee un único identificador y una única fuente de verdad.

---

### State-Driven Workflow

Todo activo existe dentro de una máquina de estados definida.

Las acciones dependen del estado actual.

---

### Idempotencia

Ejecutar el mismo proceso múltiples veces sobre el mismo input no debe producir efectos inconsistentes.

---

### Modularidad

Skills, Prompts y Automatizaciones son independientes del contenido específico del proyecto.

---

### Auditabilidad

Toda modificación relevante debe ser rastreable.

---

### Evolución Controlada

Las decisiones arquitectónicas deben documentarse mediante ADRs.

---

## 🏗️ Anatomía del Framework

```text
edo-core/
│
├── 00_GOVERNANCE/
│   ├── VISION_Y_ALCANCE.md
│   ├── SISTEMA_EDITORIAL.md
│   └── ADR/
│
├── 01_FUENTES/
│
├── 02_INVENTARIO/
│
├── 03_ESQUEMAS/
│
├── 04_ACTIVOS/
│
├── 05_SKILLS/
│
├── 06_PROMPTS/
│
├── 07_AUTOMATIZACIONES/
│
├── 08_REPORTES/
│
├── 09_TESTING/
│
├── 10_SOPS/
│
└── 99_DOCUMENTACION/
```

Cada directorio representa una responsabilidad única dentro del ecosistema.

---

## 🧩 Entidades Fundamentales

### Fuente

Origen de información que ingresa al sistema.

Ejemplos:

* Documentos
* Imágenes
* Bases de datos
* APIs
* Entradas manuales

---

### Activo

Unidad de trabajo gestionada por EDO.

Todo activo posee:

* UUID
* Estado
* Metadatos
* Dependencias
* Historial

---

### Skill

Capacidad reutilizable que ejecuta una función específica.

Ejemplos:

* Clasificación
* Transformación
* Curación
* Auditoría

---

### Prompt

Interfaz estructurada utilizada para interactuar con un modelo de lenguaje.

---

### SOP

Procedimiento operativo estandarizado.

Define cómo debe ejecutarse una actividad dentro del sistema.

---

## 🔄 Flujo Operativo

Todo activo sigue un ciclo de vida controlado.

```text
INGESTADO
    ↓
CLASIFICADO
    ↓
EN_PRODUCCION
    ↓
EN_REVISION
    ↓
APROBADO
    ↓
PUBLICADO
    ↓
ARCHIVADO
```

Las Skills y Automatizaciones actúan únicamente cuando un activo se encuentra en estados compatibles.

---

## ⚙️ Modelo de Interacción

```text
Fuente
   │
   ▼
Inventario Maestro
   │
   ▼
Skill
   │
   ▼
Prompt
   │
   ▼
Resultado
   │
   ▼
Auditoría
   │
   ▼
Cambio de Estado
```

Toda salida válida debe volver al Inventario Maestro.

---

## 📦 Contrato Mínimo de un Activo

```json
{
  "uuid": "AST-000001",
  "tipo": "activo",
  "estado": "INGESTADO",
  "dependencias": [],
  "metadata": {},
  "hash": "sha256-xxxxx"
}
```

---

## 🚀 Quick Start

### 1. Crear una implementación

Crear una nueva instancia basada en EDO Core.

---

### 2. Definir Gobernanza

Completar:

* VISION_Y_ALCANCE
* SISTEMA_EDITORIAL
* ADR iniciales

---

### 3. Inicializar Inventario

Crear el Inventario Maestro.

Definir:

* UUIDs
* Estados
* Tipos
* Dependencias

---

### 4. Incorporar SOPs

Establecer procedimientos operativos mínimos.

---

### 5. Construir Skills

Implementar capacidades reutilizables.

---

### 6. Conectar Automatizaciones

Integrar workflows y herramientas externas.

---

## 🚫 Fuera de Alcance

EDO Core no es:

* Un gestor documental.
* Una aplicación final para usuarios.
* Una base de datos de negocio.
* Un repositorio de contenido específico.

EDO Core es el motor operativo que permite construir esos sistemas.

---

## 📈 Estado del Framework

Versión: 0.1.0-alpha

Estado actual:

Arquitectura → Gobernanza → SOPs → Automatización → Producción

El framework se encuentra en fase fundacional y evoluciona mediante decisiones arquitectónicas controladas.
