# 🎥 Vigilancia y Control de Cámaras CCTV

---

## 🎯 Objetivo

Unificar el acceso y gestión de cámaras analógicas (vía DVR) e IP, eliminando la dependencia de apps propietarias o terceros, y facilitando el acceso seguro desde cualquier ubicación.

---

## 🛠️ Herramientas recomendadas

### 1. Frigate

- 🤖 Sistema de grabación NVR con detección de objetos basado en inteligencia artificial (TensorFlow).  
- 📹 Compatible con cámaras IP que soporten RTSP.  
- 🔗 Integración con Home Assistant y otros sistemas domóticos.

**Instalación recomendada:** mediante Docker para aislar el servicio.

Ejemplo básico:

```bash
docker run -d \\
  --name frigate \\
  --restart=unless-stopped \\
  --privileged \\
  -p 5000:5000 \\
  -v /path/to/config:/config \\
  -v /path/to/storage:/media/frigate \\
  -v /dev/bus/usb:/dev/bus/usb \\
  blakeblackshear/frigate:stable
```

### 2. MotionEye
- 🖥️ Alternativa ligera y sencilla para grabación y monitoreo de cámaras.

- 🎥 Soporta cámaras USB, IP y fuentes de video en red.

### 3. Shinobi
- ⚙️ Sistema de vigilancia flexible y escalable.

- 📡 Soporta múltiples tipos de cámaras y configuraciones personalizadas.

---

## 🔒 Acceso remoto seguro
- Configura acceso remoto a través de VPN (por ejemplo, Tailscale) para evitar exposición directa de cámaras a Internet.

- Usa autenticación fuerte y considera limitar acceso por IP.

---

## ⚠️ Consideraciones
- 💾 Asegura suficiente espacio de almacenamiento para grabaciones.

- 🗑️ Configura políticas de retención para no saturar el disco.

- 🎥 Prioriza cámaras compatibles con RTSP para facilidad de integración.

- 🛠️ Revisa la compatibilidad del hardware (por ejemplo, capacidad USB o CPU) para tareas intensivas como detección por IA.

---

## 📚 Recursos útiles
- [Frigate NVR](https://docs.frigate.video/)

- [MotionEye GitHub](https://github.com/motioneye-project/motioneye)

- [Shinobi CCTV](https://shinobi.video/)