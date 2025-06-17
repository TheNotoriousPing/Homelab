# 🎯 Objetivos del Homelab

## 📋 Índice
1. [🚶‍♂️ Pasos previos para comenzar](#1-primeros-pasos)  
2. [🌐 Red Privada entre dos viviendas](#2-red-privada-entre-dos-viviendas) 
3. [🚫 Bloqueo de Publicidad y DNS Local](#3-bloqueo-de-publicidad-y-dns-local)  
4. [📹 Cámaras IP y CCTV](#4-cámaras-ip-y-cctv)   
5. [📊 Monitorización del Sistema](#5-monitorización-del-sistema)
6. [🛡️ Seguridad Proactiva](#6-seguridad-proactiva)  
7. [📈 SIEM Básico](#7-siem-básico)  

---
## 1. 🚶‍♂️ Pasos previos para comenzar

**Objetivo:** Preparar la Orange Pi 3B con Armbian, IP fija y acceso remoto seguro por SSH.

- **Sistema base:** Armbian (Debian Bookworm)  
- **Acceso remoto:** SSH con clave pública  
- **Requisitos:**  
  - 💾 Tarjeta microSD ≥ 16GB  
  - 🌐 IP estática configurada  
  - 🔐 SSH por clave y puerto personalizado

> 📎 Para la guía completa, consulta [primeros-pasos](primeros-pasos.md)


## 2. 🌐 Red Privada entre dos viviendas

**Objetivo:** Establecer una red privada segura que conecte dos ubicaciones físicas como si compartieran el mismo router, incluso cuando están detrás de CG-NAT.

- **Solución preferida:** Tailscale  
- **Alternativa avanzada:** ZeroTier  
- **Requisitos:**  
  - 🔒 Conexión segura y estable  
  - ⚙️ Facilidad de configuración y mantenimiento  
  - 📱 Soporte para dispositivos múltiples

> 📎 Para la guía completa, consulta [red-privada](red-privada.md)
---

## 3. 🚫 Bloqueo de Publicidad y DNS Local

**Objetivo:** Controlar y filtrar consultas DNS para bloquear publicidad, rastreadores y mejorar la privacidad de la red local.

- **Herramienta principal:** Pi-hole  
- **Complemento recomendado:** Unbound (DNS recursivo seguro)  
- **Funcionalidades clave:**  
  - 📡 Filtrado de anuncios a nivel de red  
  - 🔐 Resolución DNS local y segura  
  - 🛠️ Gestión centralizada de listas negras y blancas

> 📎 Para la guía completa, consulta [DNS Pi-hole](dns-pihole.md)

---

## 4. 📹 Cámaras IP y CCTV

**Objetivo:** Centralizar el acceso y gestión de cámaras IP (RTSP) y cámaras analógicas mediante DVR.

- **Software recomendado:** Frigate (detección de movimiento y análisis de video)  
- **Alternativas:** MotionEye, Shinobi  
- **Características necesarias:**  
  - 🎥 Soporte para múltiples cámaras y protocolos  
  - 💾 Grabación y almacenamiento local o en red  
  - 🔒 Acceso remoto seguro

> 📎 Para la guía completa, consulta [CCTV](cctv.md)

---

## 5. 📊 Monitorización del Sistema

**Objetivo:** Supervisar el estado y métricas del sistema para detectar anomalías y asegurar el correcto funcionamiento.

- **Herramientas:**  
  - Netdata (monitorización en tiempo real)  
  - Uptime Kuma (disponibilidad y latencia de servicios)  
- **Requisitos:**  
  - 👀 Visualización intuitiva de métricas  
  - 🔔 Alertas configurables  
  - 📈 Histórico de datos

> 📎 Para la guía completa, consulta [Monitorización](monitorizacion.md)

---

## 6. 🛡️ Seguridad Proactiva

**Objetivo:** Detectar y prevenir ataques o actividades sospechosas en la red y sistemas.

- **Herramientas:**  
  - CrowdSec (detección colaborativa de amenazas)  
  - Fail2Ban (protección contra accesos no autorizados) [opcional]  
- **Funcionalidades:**  
  - 📜 Análisis de logs en tiempo real  
  - 🚫 Bloqueo automático de IPs maliciosas  
  - 🔗 Integración con otras herramientas de seguridad

> 📎 Para la guía completa, consulta [Seguridad](seguridad.md)

---

## 7. 📈 SIEM Básico

**Objetivo:** Implementar un sistema básico de gestión de eventos e información de seguridad para recopilar, analizar logs y generar alertas.

- **Solución recomendada:** Wazuh (plataforma open source)  
- **Alternativa:** Elasticsearch + Kibana + Filebeat (stack ELK)  
- **Características:**  
  - 🗄️ Centralización y normalización de logs  
  - 🤖 Análisis automatizado y alertas  
  - 📊 Paneles de control personalizables

> 📎 Para la guía completa, consulta [SIEM](siem.md)

---
