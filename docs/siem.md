# 🛡️ SIEM Básico para Centralización de Logs

---

## 🎯 Objetivo

Centralizar los registros (logs) de los distintos servicios y sistemas del homelab para facilitar la monitorización, análisis de eventos y generación de alertas de seguridad.

---

## 🛠️ Herramientas recomendadas

### 1. Wazuh

- 📦 Plataforma ligera y todo en uno para gestión de logs, detección de intrusiones y cumplimiento.  
- 🔍 Integra recolección de logs, análisis y respuesta automática.  
- 🤝 Compatible con agentes para múltiples sistemas y con integraciones para Kubernetes, Docker, entre otros.

**Instalación básica en Armbian:**

```bash
curl -s https://packages.wazuh.com/install.sh | sudo bash
Configura agentes para los servicios que quieras monitorizar.
```

### 2. Stack básico: Elasticsearch + Kibana + Filebeat
- 🔎 Elasticsearch: Motor de búsqueda y almacenamiento escalable de logs.

- 📊 Kibana: Interfaz web para visualizar y analizar logs de forma gráfica.

- 🐝 Filebeat: Agente ligero para enviar logs desde la Orange Pi a Elasticsearch.

---

## Instalación y configuración:

- Instala Elasticsearch y Kibana siguiendo la documentación oficial para ARM (puede requerir ajustes).

- Configura Filebeat en la Orange Pi para enviar logs locales a Elasticsearch.

---

## ⚙️ Recomendaciones
- ✅ Empieza con Wazuh para una solución integrada y sencilla.

- 📈 Planifica el almacenamiento para logs, ya que pueden crecer rápidamente.

- 🚨 Define reglas y alertas para eventos críticos (intentos de acceso, fallos, anomalías).

- 🔐 Protege el acceso a la interfaz web con autenticación y HTTPS para mayor seguridad.

---

## 📚 Recursos útiles
- [Documentación oficial Wazuh](https://documentation.wazuh.com/)

- [Elasticsearch para ARM](https://www.elastic.co/blog/elasticsearch-on-arm)

- [Kibana](https://www.elastic.co/kibana)

- [Filebeat](https://www.elastic.co/beats/filebeat)