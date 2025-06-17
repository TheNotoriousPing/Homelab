# 🛡️ DNS Local y Bloqueo de Publicidad con Pi-hole

---

## 🎯 Objetivo

Configurar un servidor DNS local que filtre publicidad, rastreadores y dominios maliciosos para toda la red, mejorando la privacidad y experiencia de navegación.

---

## 🛠️ Herramientas principales

- **Pi-hole**: Servidor DNS que bloquea anuncios y rastreadores a nivel de red.  
- **Unbound** (opcional): Resolver DNS recursivo privado para mayor privacidad y evitar el uso de DNS externos.

---

## ⚙️ Instalación de Pi-hole

### 📋 Requisitos previos

- Orange Pi con Armbian instalado y actualizado.  
- Acceso SSH o consola local.  
- Puerto 53 UDP/TCP disponible en la red.

### 🚀 Pasos básicos

```bash
curl -sSL https://install.pi-hole.net | bash
```

Sigue el asistente para configurar:

- Selecciona la interfaz de red que usarás para la red local.  
- Define el DNS upstream (puedes usar Unbound si lo configuras).  
- Gestiona listas negra y blanca (más adelante puedes personalizar).

---

## 🔒 Configuración recomendada con Unbound

Para mejorar la privacidad y hacer que Pi-hole resuelva directamente sin depender de terceros:

### Instalación de Unbound

```bash
sudo apt install unbound
```

### Configuración básica

Edita el archivo de configuración:

```bash
sudo nano /etc/unbound/unbound.conf.d/pi-hole.conf
```

Añade el siguiente contenido:

```conf
server:
    verbosity: 1
    interface: 127.0.0.1
    port: 5335
    do-ip4: yes
    do-udp: yes
    do-tcp: yes
    root-hints: "/var/lib/unbound/root.hints"
    hide-identity: yes
    hide-version: yes
    harden-glue: yes
    harden-dnssec-stripped: yes
    use-caps-for-id: yes
    edns-buffer-size: 1232
    prefetch: yes
    num-threads: 2
```

### Descarga del archivo root hints

```bash
sudo wget -O /var/lib/unbound/root.hints https://www.internic.net/domain/named.cache
```

### Reinicia Unbound

```bash
sudo systemctl restart unbound
```

### Configura Pi-hole

En Pi-hole, establece el DNS upstream a:

```
127.0.0.1#5335
```

---

## 🔧 Uso y administración

- Accede a la interfaz web de Pi-hole en:  
  `http://<IP_DE_TU_ORANGE_PI>/admin`  
- Revisa estadísticas, añade listas negras o blancas, y bloquea dominios.  
- Actualiza regularmente las listas para mantener la efectividad.

---

## 💡 Consejos adicionales

- Configura tus dispositivos o router para usar la Orange Pi como servidor DNS principal.  
- Habilita el registro de consultas para auditoría (si tu espacio y rendimiento lo permiten).  
- Realiza backups periódicos de la configuración (`/etc/pihole`).

---

## 📚 Recursos útiles

- [Documentación oficial Pi-hole](https://pi-hole.net/documentation/)  
- [Guía para Unbound con Pi-hole](https://docs.pi-hole.net/guides/unbound/)  