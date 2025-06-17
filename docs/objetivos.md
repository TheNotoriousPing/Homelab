# 🎯 Objetivos del Homelab

## 📋 Índice
1. [🌐 Red Privada entre dos viviendas](#1-red-privada-entre-dos-viviendas)  
2. [🚫 Bloqueo de Publicidad y DNS Local](#2-bloqueo-de-publicidad-y-dns-local)  
3. [📹 Cámaras IP y CCTV](#3-cámaras-ip-y-cctv)  
4. [📊 Monitorización del Sistema](#4-monitorización-del-sistema)  
5. [🛡️ Seguridad Proactiva](#5-seguridad-proactiva)  
6. [📈 SIEM Básico](#6-siem-básico)  

---

## 1. 🌐 Red Privada entre dos viviendas

**Objetivo:** Establecer una red privada segura que conecte dos ubicaciones físicas como si compartieran el mismo router, incluso cuando están detrás de CG-NAT.

- **Solución preferida:** Tailscale  
- **Alternativa avanzada:** ZeroTier  
- **Requisitos:**  
  - 🔒 Conexión segura y estable  
  - ⚙️ Facilidad de configuración y mantenimiento  
  - 📱 Soporte para dispositivos múltiples

---

## 2. 🚫 Bloqueo de Publicidad y DNS Local

**Objetivo:** Controlar y filtrar consultas DNS para bloquear publicidad, rastreadores y mejorar la privacidad de la red local.

- **Herramienta principal:** Pi-hole  
- **Complemento recomendado:** Unbound (DNS recursivo seguro)  
- **Funcionalidades clave:**  
  - 📡 Filtrado de anuncios a nivel de red  
  - 🔐 Resolución DNS local y segura  
  - 🛠️ Gestión centralizada de listas negras y blancas

---

## 3. 📹 Cámaras IP y CCTV

**Objetivo:** Centralizar el acceso y gestión de cámaras IP (RTSP) y cámaras analógicas mediante DVR.

- **Software recomendado:** Frigate (detección de movimiento y análisis de video)  
- **Alternativas:** MotionEye, Shinobi  
- **Características necesarias:**  
  - 🎥 Soporte para múltiples cámaras y protocolos  
  - 💾 Grabación y almacenamiento local o en red  
  - 🔒 Acceso remoto seguro

---

## 4. 📊 Monitorización del Sistema

**Objetivo:** Supervisar el estado y métricas del sistema para detectar anomalías y asegurar el correcto funcionamiento.

- **Herramientas:**  
  - Netdata (monitorización en tiempo real)  
  - Uptime Kuma (disponibilidad y latencia de servicios)  
- **Requisitos:**  
  - 👀 Visualización intuitiva de métricas  
  - 🔔 Alertas configurables  
  - 📈 Histórico de datos

---

## 5. 🛡️ Seguridad Proactiva

**Objetivo:** Detectar y prevenir ataques o actividades sospechosas en la red y sistemas.

- **Herramientas:**  
  - CrowdSec (detección colaborativa de amenazas)  
  - Fail2Ban (protección contra accesos no autorizados) [opcional]  
- **Funcionalidades:**  
  - 📜 Análisis de logs en tiempo real  
  - 🚫 Bloqueo automático de IPs maliciosas  
  - 🔗 Integración con otras herramientas de seguridad

---

## 6. 📈 SIEM Básico

**Objetivo:** Implementar un sistema básico de gestión de eventos e información de seguridad para recopilar, analizar logs y generar alertas.

- **Solución recomendada:** Wazuh (plataforma open source)  
- **Alternativa:** Elasticsearch + Kibana + Filebeat (stack ELK)  
- **Características:**  
  - 🗄️ Centralización y normalización de logs  
  - 🤖 Análisis automatizado y alertas  
  - 📊 Paneles de control personalizables

---
