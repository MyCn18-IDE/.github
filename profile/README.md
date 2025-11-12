# MyCn18 Flows: Define tu flujo, sin ataduras, a cualquier nivel.

**MyCn18** es la plataforma de orquestación **Code-First** de código abierto. Nuestro motor traduce tus flujos visuales en **TypeScript auditable y ejecutable**, ofreciendo control, transparencia y la libertad de crear *software* sin límites.

Si exiges **transparencia, control de datos y escalabilidad empresarial**, este es tu motor.

-----

## Características principales

| Capacidad Clave | Descripción |
| :--- | :--- |
| **Cuatro Niveles de Abstracción** | **De la IA al Código Fuente:** Empieza con **Prompt-to-Flow (Nivel 4)**, usa **Componentes Completos (Nivel 3)**, personaliza con **Flujos Algorítmicos (Nivel 2)** o modifica el **Código Fuente directo (Nivel 1)**. |
| **AI-Native Platform** | **Estrategia AI-First:** Chatbot integrado para la creación de flujos (Prompt-to-Flow). Listo para construir flujos con Agentes de IA. |
| **Componentes Completos mediante Nodos de Alto Nivel (High-level Block Node)** | El verdadero poder: flujos simples mediante la creación de **componentes completos** (HBNs) que encapsulan la lógica compleja. |
| **Cada componente es personalizable mediante UI con Nodos de Bajo Nivel (Low-level Block Node)** | El límite es tu imaginación: puedes personalizar cada HBN mediante un canvas para manipular variables, ciclos, etc. Ideal para iniciantes en el mundo de la programación o q simplemente quieren explorar |
| **Estrategia Code-First** | Para desarrolladores experimentados (como yo mismo q odio este tipo de sistemas pq t obligan a usar la UI) siempre está la opción de implementar desde cero nodos personalizados o incluso personalizar el codigo fuente de cada nodo pre-hecho |
| **Full Control & Self-Host** | **Auto-Hosteable por Diseño.** Nuestro *Worker* es **MIT**. Despliega donde quieras con Docker o K8s. |
| **Herramientas CLI** | La **`mycn18-cli`** actúa como una herramienta abstracta para el ***self-hosting* simplificado** y para **acceder y probar cualquier SDK** (privado o comunitario) desde tu entorno de trabajo. |
| **Independencia del Ecosistema** | **Exporta tu Lógica:** Exporta tus flujos a código fuente estándar (**Node.js, Python (próximamente), etc.**) para que puedas ejecutarlo en tu propia infraestructura sin depender de MyCn18. |
| **Enterprise-Ready** | Orquestación robusta con **BullMQ** y Auditoría completa con *logging* a **PostgreSQL**. |

-----

## 🏗️ La Arquitectura del Motor: El Secreto del Código

MyCn18 garantiza la calidad del código mediante su **Jerarquía de Nodos**, la base de nuestra transparencia:

  * **Nodos de Alto Nivel (HBN) — Componentes Completos:** Son las plantillas que arrastras (`Enviar correo`, `Analizar con LLM`, `Insertar en una BD`, etc.`). **La UI maneja su complejidad.**
  * **Nodos de Bajo Nivel (LBN) — Átomos de Programación:** Son los bloques fundamentales (`if-else`, `ciclos`, `sdk-call`). **El código generado siempre es limpio** porque se construye a partir de esta sintaxis atómica.

-----

## 📦 Organización y Open Core (¡Transparencia Total\!)

| Repositorio | Rol Principal | Licencia | Estado |
| :--- | :--- | :--- | :--- |
| **`mycn18-worker`** | **Motor de Ejecución y Orquestación.** Sandbox de VM2. | **MIT** | Público |
| **`mycn18-community-sdks`** | **SDKs Comunitarios.** Plataforma para recibir contribuciones de integraciones. | **MIT** | Público |
| **`mycn18-cli`** | **Herramientas Abstractas.** Self-Hosting y uso de SDKs desde la terminal. | **MIT** | Privado |
| **`mycn18-ui-editor`** | Interfaz de Usuario. | **MIT** | Privado |
| **`mycn18-ui-utilities`** | **Catálogo de Nodos y Generador de Código (PI).** | Proprietary | Privado |
| **`mycn18-private-sdks`** | **Integraciones Premium/Oficiales (PI).** | Proprietary | Privado |

-----

## 🤝 Estrategia de Colaboración: ¡Crea tu Propio SDK\!

Mantenemos la PI de nuestros SDKs y el Generador (Catálogo) privados para asegurar la financiación, pero abrimos la puerta para que la comunidad se encargue de las integraciones.

### 1\. Colaboración en el Motor (MIT)

El repositorio `mycn18-worker` está abierto a Pull Requests para:

  * Mejoras en la seguridad del **Sandbox (VM2)** y el sistema de inyección de módulos (`resolver.ts`).
  * Optimización de la orquestación (BullMQ) y el *logging* de BDD.
  * Integración de frameworks de testing de flujos (Git-Ops).

### 2\. Creación de SDKs de Comunidad (`mycn18-community-sdks`)

Este es el mecanismo para que **nos ayudes a construir las integraciones** sin comprometer tu código ni el nuestro:

1.  **Contrato Público:** El repositorio **`mycn18-community-sdks`** contendrá el **contrato (interface)** que todo SDK externo debe seguir.
2.  **Tu Repositorio MIT:** Implementa la lógica de la API de un tercero (ej: para Trello o Discord) en tu propio repositorio MIT.
3.  **Inyección Segura:** Nuestro **`mycn18-worker` (MIT)** tiene la lógica para **descargar, validar e inyectar de forma segura** tu SDK en el *sandbox* durante la ejecución.

De esta manera, la comunidad impulsa el ecosistema de integraciones, y nosotros garantizamos la seguridad y el control.

-----

## 🎬 Quick Start

### Self-Hosting con la CLI (Próximamente):

```bash
# Usa la CLI para gestionar el despliegue del Worker
mycn18-cli setup --host local
```

### Ver el Motor en Acción:

Consulta la guía de *Self-Hosting* en el repositorio [mycn18-worker](https://github.com/MyCn18-flows/mycn18-worker).

### Recursos

📚 [Documentación Oficial (Próximamente)]()
🔧 [Repositorio del Worker](https://github.com/MyCn18-flows/mycn18-worker)
👥 [Comunidad SDKs](https://github.com/MyCn18-flows/mycn18-community-sdks)

### Nota: 
Si queda alguna duda o desea contactarme de alguna forma, visite mi [portafolio](https://luke1606.github.io/mycn18-consulting/).

### Estado actual
MyCn18 es un proyecto que apenas está comenzando y avanza a un ritmo constante, impulsado por la dedicación de un solo desarrollador, si desean apoyar de cualquier forma, en todos los repositorios públicos están las formas de apoyarme, aunque sea simplemente visitar mi [portafolio](https://luke1606.github.io/mycn18-consulting) y mandarme un correo, me motiva a seguir.
