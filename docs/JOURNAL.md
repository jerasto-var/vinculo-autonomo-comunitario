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

---

## 4. Estatus Actual del Proyecto
* **Estado:** 🟢 Entorno de desarrollo operativo.
* **Plataforma:** Termux (Host) / QEMU (Testing) / GitHub (Sincronizacion).
* **Dependencias instaladas:** `httpx`, `python-dotenv`.

---

## 5. Pendientes y Observaciones
### Pendientes Inmediatos (Backlog):
- [ ] Configurar el script de lanzamiento de QEMU (`qemu-run.sh`) con montaje de carpetas.
- [ ] Crear el `docker-compose.yml` base para los servicios de PocketBase y Gitea.
- [ ] Desarrollar script de prueba para validacion de flujo de datos inicial.

### Observaciones Tecnicas:
* Se opto por peticiones directas via `httpx` para optimizar el consumo de recursos y compatibilidad en el entorno movil.
* El repositorio local se renombro satisfactoriamente eliminando acentos para asegurar la integridad de las rutas en Git.

---

## 6. Futuros Pasos
* Definicion de variables de entorno finales en `.env`.
* Pruebas de carga inicial en QEMU para validar consumo de RAM.