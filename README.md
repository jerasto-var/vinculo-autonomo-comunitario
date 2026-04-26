# vinculo-autonomo-comunitario

Ecosistema digital ligero y soberano diseñado para la gestion de comunidades y asociaciones civiles. Este proyecto permite centralizar la comunicacion, la administracion de roles y el resguardo documental utilizando hardware de bajo consumo (Raspberry Pi).

## 🚀 Vision General
El proyecto busca eliminar la dependencia de servicios de nube externos, proporcionando una infraestructura "todo en uno" que garantiza la privacidad de los datos y la autonomia tecnologica de la organizacion.

## 🛠️ Arquitectura Tecnica
La solucion se basa en una orquestacion de microservicios mediante Docker:

* **Base de Datos y Usuarios:** PocketBase (Backend ligero y reactivo).
* **Gestion Documental:** Gitea (Control de versiones y archivo historico).
* **Mensajeria en Tiempo Real:** Gotify (Notificaciones push privadas).
* **Orquestador de Logica:** Worker dedicado en Python para automatizacion de flujos.

## 📋 Requisitos del Sistema
* **Hardware:** Raspberry Pi 4 (minimo 2GB RAM) o equivalente ARM64.
* **SO Recomendado:** Debian / Raspberry Pi OS (64-bit).
* **Entorno de Desarrollo:** Compatible con Termux + QEMU para pruebas moviles.

## 🔧 Instalacion Rapida (Desarrollo)
1. Clonar el repositorio:
   ```bash
   git clone [https://github.com/tu-usuario/vinculo-autonomo-comunitario.git](https://github.com/tu-usuario/vinculo-autonomo-comunitario.git)
   ```
2. Configurar variables de entorno:
   ```bash
   cp .env.example .env
   ```
3. Levantar servicios:
   ```bash
   docker-compose up -d
   ```

## 📖 Documentacion
Para detalles sobre el progreso del desarrollo, hitos tecnicos y proximos pasos, consulta el archivo [JOURNAL.md](./JOURNAL.md).

---
*Desarrollado bajo principios de soberania digital y software libre.*
