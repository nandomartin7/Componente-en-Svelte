# 📌 Filtro de Usos del Seguro - Svelte 🚗🛡️

Este es un componente de **Svelte** que permite a los clientes filtrar y visualizar sus **usos de seguro** asociados a sus contratos.  
El sistema obtiene los datos desde una API REST desarrollada en **Spring Boot** y forma parte de un proyecto más grande cuyo frontend principal está en **Vue.js**.

---

## 🚀 Funcionalidad  

✅ Obtener **todos los usos** de seguro del cliente autenticado.  
✅ **Filtrar usos** por fecha para obtener registros específicos.  
✅ Mostrar los **usos en una tabla** con detalles relevantes.  
✅ **Redirección a Vue** para mantener la integración del sistema.  

---

## 📦 Instalación y Configuración

### 🔹 1. Clonar el repositorio  
```bash
git clone https://github.com/tu-usuario/tu-repositorio-svelte.git
cd tu-repositorio-svelte
```

### 🔹 2. Instalar dependencias
```bash
npm install
```

### 🔹 3. Ejecutar el proyecto en modo desarrollo
```bash
npm run dev
```
Por defecto, el proyecto se ejecutará en:
```bash
http://localhost:50577
```

### 🔹 4. Configurar la API Backend
Este proyecto consume datos desde un backend en Spring Boot. Asegúrate de que el servidor de la API está corriendo en:
```bash
http://localhost:8080
```
Si la URL de la API es diferente, puedes modificarla en el código fuente.

---

## 🛠️ Uso
Este componente obtiene el idCliente desde la URL y lo utiliza para obtener los contratos y usos de seguro asociados.

🔹 Datos obtenidos de la API
El sistema obtiene los siguientes datos:

Contratos del Cliente:
```bash
GET /contrato/filtrar/cliente?idcliente={idCliente}
```
Usos de Seguro:
```bash
GET /uso/filtrar/contrato?idContrato={idContrato}
```
🔹 Filtro de Fechas
Los usuarios pueden filtrar los usos del seguro por un rango de fechas, y los resultados se mostrarán en una tabla.

---
## 📂 Estructura del Proyecto
```bash
📦 src
 ┣ 📂 components    # Componentes de Svelte
 ┣ 📂 assets        # Estilos y recursos
 ┣ 📜 App.svelte    # Componente principal
 ┣ 📜 main.js       # Punto de entrada
 ┗ 📜 package.json  # Dependencias del proyecto
```

---
## 🏗️ Implementación Técnica

🔹 Integración con Vue.js
El componente Svelte se integra con el frontend de Vue.js mediante la redirección con window.location.href y la transferencia del idCliente como parámetro de la URL.

🔹 Principios SOLID aplicados
✅ SRP (Single Responsibility Principle): Cada módulo tiene una única responsabilidad (obtención de datos, filtrado, renderizado).
✅ OCP (Open/Closed Principle): El código está abierto a extensiones sin modificar la lógica existente. 

🔹 Patrones de Diseño
✅ Factory Pattern: Se usa en el backend para la creación de planes de seguro. 
✅ ingleton Pattern: Se usa en el backend para  instanciar el método de creación del Factory.

---
## 🚀 Despliegue
Este módulo está deployado en Vercel y se integra con el frontend de Vue.

Puedes acceder al despliegue en:

Frontend Pirncipal en Vue.Js: https://buenas-practicas-core-frontend.vercel.app/login-cliente

Componete en Svelte.Js: https://componente-en-svelte.vercel.app/

---
## 💬 Contacto
### Carlos Larco: carlos.larco.escobar@udla.edu.ec
### Fernando Camacho: fernando.camacho@udla.edu.ec









