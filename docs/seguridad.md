# 🔐 Seguridad Proactiva

---

## 🎯 Objetivo

Implementar mecanismos que detecten comportamientos anómalos o intentos de ataque en la Orange Pi y servicios asociados, mejorando la protección de la red y sistemas.

---

## 🛠️ Herramientas recomendadas

### 1. CrowdSec

- 🔥 Firewall colaborativo con detección basada en comportamiento.  
- 🚫 Bloqueo automático de IPs maliciosas.  
- 🔗 Integración con servicios comunes (SSH, HTTP, etc.).  
- 🌐 Comunidad activa que comparte inteligencia de amenazas.

**Instalación básica:**

```bash
curl -s https://packagecloud.io/install/repositories/crowdsec/crowdsec/script.deb.sh | sudo bash
sudo apt install crowdsec
```

Configura parsers y escenarios según los servicios que tengas activos.

---

### 2. Fail2Ban (complementario)

- 🛡️ Monitoriza logs y bloquea IPs tras varios intentos fallidos.  
- 🔐 Útil para proteger servicios específicos como SSH.

**Instalación:**

```bash
sudo apt install fail2ban
```

Configura reglas en `/etc/fail2ban/jail.local` según tus necesidades.

---

## 📝 Buenas prácticas de seguridad

- 🔄 Cambiar puertos por defecto (ej. SSH) para evitar ataques automatizados.  
- 🔑 Usar claves SSH en lugar de contraseñas.  
- 🛠️ Mantener el sistema y software actualizados.  
- 🚪 Revisar y limitar puertos abiertos con firewall (UFW o iptables).  
- 💾 Realizar backups de configuraciones y registros críticos.

---

## 📚 Recursos útiles

- [Documentación CrowdSec](https://doc.crowdsec.net/)  
- [Fail2Ban GitHub](https://github.com/fail2ban/fail2ban)  
- [Guía básica de seguridad Linux](https://linuxsecurity.expert/tutorials/)