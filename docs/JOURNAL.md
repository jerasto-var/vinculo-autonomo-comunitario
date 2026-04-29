# Journal - Vinculo Autonomo Comunitario

## 1. Vision del Proyecto
**Objetivo:** Crear una infraestructura digital independiente y ligera para la gestion de asociaciones civiles y comunidades, facilitando la comunicacion interna y la organizacion de procesos administrativos en hardware de bajo costo.

**Alcance:**
* Gestion de usuarios y roles personalizados.
* Herramientas para facilitar la comunicacion y el flujo de informacion entre miembros.
* Repositorio documental y registro de acuerdos estructurados.
* Sistema de notificaciones push en tiempo real.

**Fuera de Alcance:**
* Streaming de video o almacenamiento masivo de archivos multimedia.
* Sustitucion de contabilidad fiscal oficial.
* Redes sociales abiertas.

---

## 2. Plan de Trabajo (Roadmap)
1.  **Fase de Cimentacion:** Configuracion de orquestacion Docker y limites de recursos para Raspberry Pi 4 (2GB).
2.  **Fase de Estructura y Datos:** Despliegue de PocketBase y diseño de arquitectura de datos base.
3.  **Fase de Interfaz:** Dashboard estatico ligero y sistema de alertas via Gotify.
4.  **Fase de Inteligencia:** Implementacion de un orquestador para el procesamiento avanzado de informacion y automatizacion de flujos.

---

## 3. Historial de Actividades

### [2026-04-25] - Inicializacion y Sincronizacion del Entorno
* **Definicion del Nombre:** Se eligio `vinculo-autonomo-comunitario` para reflejar autonomia tecnica y proposito social.
* **Configuracion en Termux:** * Creacion de entorno de desarrollo nativo.
    * Configuracion de Python `venv` (se corrigio error de rutas por caracteres especiales).
    * Instalacion de dependencias base (`httpx`, `python-dotenv`).
* **Hito de GitHub:** * Vinculacion mediante Token de Acceso Personal (PAT).
    * Resolucion de conflictos de historiales mediante `pull --allow-unrelated-histories`.
    * Primer `push` exitoso al repositorio remoto.

### [2026-04-28] - Fase de Cimentación: Reestructuración y Entorno

* **Reorganización del Repositorio:** Se implementó una estructura de directorios más limpia, moviendo la documentación a `docs/` y los scripts de prueba a `scripts/`.
* **Gestión de Dependencias:** Se inicializó formalmente el entorno virtual (`venv`) y se creó el archivo `requirements.txt` incluyendo `httpx` y `python-dotenv`.
* **Control de Versiones:** Se configuró `.gitignore` para proteger archivos sensibles (`.env`), archivos de sistema de QEMU (`*.qcow2`) y el entorno virtual.
* **Automatización de Terminal:** Optimización de funciones en `.bashrc` para soportar la sincronización de archivos entre Markor y la nueva estructura de carpetas mediante el uso de `basename` y bucles `for`.

---

## 4. Estado de la Infraestructura

* **Repositorio Local:** Configurado en Termux bajo `~/proyectos/vinculo-autonomo-comunitario`.
* **Estructura de Carpetas:** * `/docs`: Documentación y Journals.
    * `/scripts`: Utilidades y pruebas de conexión.
    * `/docker`: (Pendiente) Configuración de microservicios.
* **Entorno Python:** `venv` activo con `httpx` y `python-dotenv` instalados.
* **Conectividad:** Scripts de prueba validados para futuras integraciones con PocketBase/Gotify.

---

## 5. Próximos Pasos Inmediatos

1.  **Configuración de Docker:** Redactar el `docker-compose.yml` para desplegar la instancia local de PocketBase.
2.  **Variables de Entorno:** Crear el archivo `.env` local (protegido por gitignore) con las claves necesarias.
3.  **Orquestador Inicial:** Comenzar el desarrollo de `main.py` en `src/` para gestionar el flujo de datos.
4.  **Pruebas en QEMU:** Validar la portabilidad de los scripts dentro de la máquina virtual Alpine.

---

## 6. Glosario y Referencias Rápidas

* **v-pull / v-push:** Funciones personalizadas en Bash para sincronizar el cerebro (Markor) con el código (Termux).
* **lt:** Alias de `tree` configurado para ignorar carpetas pesadas y mostrar archivos ocultos.
* **Requerimientos:** `pip install -r requirements.txt` para replicar el entorno en cualquier dispositivo (ej. Raspberry Pi).
