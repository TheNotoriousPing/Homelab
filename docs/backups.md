# 💾 Estrategia de Backups y Recuperación

---

## 🎯 Objetivo

Implementar un sistema fiable para realizar copias de seguridad periódicas de configuraciones y datos críticos, asegurando la recuperación rápida en caso de fallo o pérdida de información.

---

## 🛠️ Herramientas recomendadas

### 1. Rsync

- 🔄 Herramienta eficiente para sincronización y copias incrementales.  
- 🔐 Permite backups locales y remotos vía SSH.  
- ⚙️ Fácil de automatizar con scripts y cron.

**Ejemplo básico para backup local:**

```bash
rsync -av --delete /ruta/origen/ /ruta/destino/
```

**Ejemplo para backup remoto:**

```bash
rsync -av --delete /ruta/origen/ usuario@remoto:/ruta/destino/
```

---

### 2. BorgBackup (Borg)
- 📦 Software de backup deduplicado, comprimido y cifrado.

- ⚡ Ideal para backups seguros y eficientes.

- ⏳ Permite restauraciones puntuales y backups incrementales.

---
 
**Instalación:**

```bash
sudo apt install borgbackup
```

**Inicialización de repositorio con cifrado:**

```bash
borg init --encryption=repokey /ruta/al/repositorio
```

**Crear backup:**

```bash
borg create /ruta/al/repositorio::nombre_backup /ruta/origen
```

---

## 📝 Buenas prácticas
- 📅 Realizar backups periódicos (diarios, semanales) según criticidad.

- 🌍 Mantener al menos una copia remota para protección ante desastres locales.

- ✅ Probar la restauración regularmente para asegurar integridad.

- 🔐 Evitar almacenar contraseñas en texto plano; usar mecanismos seguros para gestión de secretos.

- 📚 Documentar las rutas, horarios y procedimientos de backup.

---

## 🤖 Automatización
- Usa cron para programar backups automáticos.

- Ejemplo de entrada en crontab para backup diario a las 2 AM:

```bash
0 2 * * * /usr/bin/rsync -av --delete /ruta/origen/ /ruta/destino/
```

---

## 📚 Recursos útiles
- [Rsync Documentation](https://rsync.samba.org/documentation.html)

- [BorgBackup Documentation](https://borgbackup.readthedocs.io/en/stable/)