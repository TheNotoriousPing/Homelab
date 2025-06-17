# 📊 Monitorización del Sistema y Servicios

---

## 🎯 Objetivo

Contar con herramientas que permitan supervisar el estado y rendimiento de la Orange Pi y de los servicios que se ejecutan en ella, para detectar problemas antes de que afecten la operatividad.

---

## 🛠️ Herramientas recomendadas

### 1. Netdata

- 📈 Monitorización en tiempo real de recursos del sistema (CPU, memoria, disco, red).  
- 🌐 Visualizaciones gráficas y detalladas vía web.  
- 🚨 Alertas configurables para detectar anomalías.

**Instalación básica:**

```bash
bash <(curl -Ss https://my-netdata.io/kickstart.sh)
```

Accede a la interfaz web en:  
`http://<IP_ORANGE_PI>:19999`

---

### 2. Uptime Kuma

- 🖥️ Monitorización de disponibilidad de servicios y hosts (HTTP, TCP, ICMP...).  
- ⚙️ Fácil configuración y panel moderno.  
- 🔔 Alertas mediante correo, Telegram, Discord y más.

**Instalación con Docker (recomendado):**

```bash
docker run -d --restart=always -p 3001:3001 --name uptime-kuma louislam/uptime-kuma
```

Accede a la interfaz en:  
`http://<IP_ORANGE_PI>:3001`

> Si prefieres instalar sin Docker, revisa la [documentación oficial](https://github.com/louislam/uptime-kuma).

---

## ⚙️ Configuración recomendada

- Monitoriza los servicios clave: Pi-hole, Tailscale, Frigate, CrowdSec, entre otros.  
- Define alertas para caídas o sobrecargas.  
- Integra notificaciones en tus canales preferidos para recibir avisos.

---

## 💡 Consejos para un buen monitoreo

- ⚠️ No sobrecargar el sistema con demasiados checks muy frecuentes.  
- 📊 Revisar regularmente las gráficas y logs para detectar tendencias.  
- 🔄 Mantener actualizadas las herramientas para beneficiarte de mejoras y seguridad.

---

## 📚 Recursos útiles

- [Netdata Documentation](https://learn.netdata.cloud/docs/)  
- [Uptime Kuma GitHub](https://github.com/louislam/uptime-kuma)  