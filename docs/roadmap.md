# 🛣️ Roadmap del Proyecto Homelab

## 🎯 Objetivo  
Definir una hoja de ruta clara, estructurada y práctica para la implementación progresiva del homelab, facilitando planificación, ejecución y seguimiento.

---

## 🚀 Fase 1: Preparación del Hardware y Sistema Base

- [ ] Recepción y montaje de la **Orange Pi 3B**  
- [ ] Instalación de **Armbian** y actualización completa del sistema  
- [ ] Configuración de usuario seguro y acceso **SSH**  
- [ ] Configuración básica de firewall (**UFW** o **iptables**)  
- [ ] Documentación detallada de la configuración inicial  

---

## 🌐 Fase 2: Configuración de Red Privada

- [ ] Evaluar opciones: **Tailscale** vs **ZeroTier**  
- [ ] Instalación y configuración de **Tailscale** (recomendado para empezar)  
- [ ] Pruebas de conectividad entre viviendas  
- [ ] Documentar configuración y resultados  

---

## 🛡️ Fase 3: DNS Local y Bloqueo de Publicidad

- [ ] Instalación de **Pi-hole**  
- [ ] (Opcional) Configuración de **Unbound** como DNS recursivo privado  
- [ ] Configurar dispositivos para usar Pi-hole como DNS principal  
- [ ] Documentar configuración y personalizaciones  

---

## 🎥 Fase 4: Vigilancia CCTV

- [ ] Evaluar cámaras disponibles y compatibilidad **RTSP**  
- [ ] Instalar y configurar **Frigate** o alternativas (**MotionEye**, **Shinobi**)  
- [ ] Configurar almacenamiento para grabaciones  
- [ ] Configurar acceso remoto seguro vía VPN (ej. Tailscale)  
- [ ] Documentar instalación y uso  

---

## 📊 Fase 5: Monitorización del Sistema y Servicios

- [ ] Instalar **Netdata** para monitorización en tiempo real  
- [ ] Instalar **Uptime Kuma** para supervisión de servicios  
- [ ] Configurar alertas y notificaciones personalizadas  
- [ ] Documentar configuración y mejores prácticas  

---

## 🔐 Fase 6: Seguridad Proactiva

- [ ] Instalar **CrowdSec** para detección y mitigación de amenazas  
- [ ] (Opcional) Instalar **Fail2Ban** para protección específica (ej. SSH)  
- [ ] Configurar firewall avanzado y políticas de acceso estrictas  
- [ ] Documentar políticas y procedimientos de seguridad  

---

## 🗃️ Fase 7: SIEM Básico

- [ ] Instalar **Wazuh** o stack **Elasticsearch + Kibana + Filebeat**  
- [ ] Configurar centralización y análisis de logs  
- [ ] Definir alertas críticas y paneles de control  
- [ ] Documentar procesos y uso de la plataforma  

---

## 💾 Fase 8: Backups y Mantenimiento

- [ ] Definir estrategia integral de backups (local y remoto)  
- [ ] Implementar automatizaciones con **rsync** o **BorgBackup**  
- [ ] Programar y ejecutar pruebas regulares de restauración  
- [ ] Documentar cronogramas y procedimientos  

---

## 📚 Fase 9: Documentación y Publicación

- [ ] Organizar toda la documentación con **MkDocs**  
- [ ] Configurar y desplegar documentación pública con **GitHub Pages**  
- [ ] Actualizar roadmap y seguimiento de avances  

---

## 📝 Notas adicionales

- Cada fase debe estar acompañada de documentación clara y respaldos.  
- Priorizar siempre la seguridad y estabilidad en cada implementación.  
- Revisar y ajustar el roadmap periódicamente según el progreso y aprendizajes.

