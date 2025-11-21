
---

# 📱 miAppLoginMultiUsuario

Aplicación móvil desarrollada con **React Native + Expo** y **TypeScript**, que integra:

* Pantalla de **Login** (Evaluación 1 revisada e integrada).
* Sistema de **navegación avanzada** con Expo Router.
* Sección principal con **Tabs** (Home / Perfil).
* Módulo completo de **TODOList**, incluyendo:

* creación de tareas,
* foto desde cámara/galería,
* obtención de localización,
* marcado de completadas/no completadas,
* eliminación,
* y persistencia local con AsyncStorage + FileSystem.

Proyecto correspondiente a la **Evaluación 2**, demostrando estructura profesional, manejo de estado, navegación, buenas prácticas, componentes reutilizables e integración de módulos nativos.

---

## Objetivo académico

Demostrar dominio en:

* Desarrollo móvil con **React Native + Expo**.
* Uso de **TypeScript** en toda la lógica de la app.
* Manejo de estado con **React Hooks**.
* Persistencia local con **AsyncStorage**.
* Navegación declarativa con **Expo Router**.
* Implementación de un flujo completo: *login → tabs → tareas*.
* Trabajo colaborativo con commits de múltiples integrantes.

---

## Tecnologías utilizadas

* **Expo**
* **React Native**
* **Expo Router**
* **TypeScript**
* **AsyncStorage**
* **Expo Location**
* **Expo ImagePicker**
* **Expo FileSystem**
* **@expo/vector-icons**

---

## Estructura principal del proyecto

```bash
miAppLoginMultiUsuario/
├─ app/
│  ├─ _layout.tsx
│  ├─ index.tsx
│  ├─ auth/
│  │  └─ index.tsx
│  └─ home/
│     ├─ _layout.tsx
│     ├─ index.tsx
│     └─ tareas/
│        ├─ index.tsx
│        └─ create.tsx
├─ src/
│  ├─ storage/
│  │  ├─ userStorage.js
│  │  └─ todolist.js
│  └─ types/
│     └─ todolist.ts
├─ app.json
├─ package.json
├─ tsconfig.json
└─ README.md
```

---

# Funcionalidad de Login (Evaluación 1 integrada)

La app incluye:

* Campo **email**
* Campo **password** (seguro)
* Botón **Iniciar sesión**
* Validación:

  * Si la contraseña **≠ "1234"** → “Contraseña incorrecta”
  * Si es correcta → pasa a la vista con Tabs
* El usuario queda guardado en **AsyncStorage**

Luego se redirige automáticamente a:

* **Home** (bienvenida)
* **Perfil** (muestra email del usuario)

---

# Navegación con Expo Router

* `app/_layout.tsx` controla el stack raíz
* `app/index.tsx` decide si mostrar **login** o **home**
* `app/home/_layout.tsx` organiza todas las pantallas internas
* `app/home/index.tsx` contiene los **Tabs**

---

# Módulo TODO List (Requerimiento principal)

Incluye:

### Crear tareas con

* Título (*obligatorio*)
* Foto mediante **ImagePicker**
* Ubicación usando **expo-location**
* Guardado de foto en **FileSystem**
* Guardado en persistencia local con AsyncStorage
* Asociación automática al usuario **admin**

### Funcionalidades

* Listar tareas asociadas al usuario admin
* Marcar como completada/no completada
* Eliminar tareas
* Persistencia entre sesiones

---

# Video demostrativo (Requisito de la evaluación)

**YouTube:**
[https://youtu.be/1KYEbf2-Mac](https://youtu.be/1KYEbf2-Mac)

El video muestra:

1. Pantalla de Login
2. Validación correcta / incorrecta
3. Tabs Home y Perfil
4. Todo List:

   * Crear una tarea con foto y ubicación
   * Completar tareas
   * Eliminar tareas
5. Flujo completo funcionando

---

# Integrantes del Grupo

### **Efren Tovar**

**Técnico dev**

* Configuración inicial del proyecto con Expo + TypeScript
* Implementación completa de la lógica de login (Evaluación 1)
* Integración del login al flujo de navegación con Expo Router
* Desarrollo del TODO List:
* formulario de creación
* manejo de fotos con ImagePicker
* localización con Expo Location
* almacenamiento en FileSystem
* persistencia en AsyncStorage
* listados, completado y eliminado
* Integración general, testing y refactor

### **Eduardo Ahumada**

**Técnico dev Documentación y mejoras visuales**

* Creación y edición del **README.md**
* Ajustes de diseño de pantallas y estilo visual
* Revisión de componentes, estructura y orden del código
* Commit de documentación y mejoras

### **Daniel Castro**

**Técnico dev Soporte y revisión**

* Revisión del flujo de navegación entre pantallas y estructura del proyecto
* Apoyo en pruebas de funcionamiento general y Evaluación del flujo entre pantallas
* Observaciones sobre uso de buenas prácticas y estructura
* Comentarios y observaciones del codigo

### **Jeremy Sanhueza**

**Técnico dev Soporte y revision**

* Revisión general de navegación
* Revisión visual de pantallas
* Ajustes de interfaz
* Apoyo en validación de rutas y flujos
* Comentarios y observaciones del codigo
* Desarrollo de El documento txt en pdf

---

# Instalación y ejecución

### Clonar

```bash
[![miAppLoginMultiUsuario](https://img.shields.io/badge/miAppLoginMultiUsuario-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/ejts29/miAppLoginMultiUsuario)


cd miAppLoginMultiUsuario
```

### Instalar dependencias

```bash
npm install
```

### Ejecutar (Expo Go o Dev Client)

```bash
npx expo start
```

o en Android:

```bash
npx expo run:android
```

---

# Uso de IA en el proyecto

El grupo utilizó una IA generativa (ChatGPT) como apoyo para:

* Resolver errores de dependencias y configuración con Expo
* Depurar comandos de consola
* Reorganizar el proyecto y mejorar la arquitectura
* Orientación técnica en el uso de FileSystem, AsyncStorage, Expo Router y TypeScript

Todas las decisiones de implementación, pruebas finales y funcionamiento fueron realizadas por los integrantes del grupo.

---

# Entrega EVA

Archivo `.txt o pdf` incluirá:

* Enlace al repositorio GitHub
* Enlace al video YouTube
* Integrantes completos
* Descripción general de la aplicación

---
