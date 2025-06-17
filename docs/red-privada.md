# Red Privada entre Viviendas

## 🎯 Objetivo

Interconectar dos viviendas a través de una red virtual privada, permitiendo que todos los dispositivos se comuniquen como si estuvieran en la misma red local, incluso estando detrás de CG-NAT.

---

## 🔐 Opciones de implementación

### ✅ Opción 1: Tailscale (Recomendada)

Tailscale utiliza el protocolo WireGuard y es ideal para entornos con CG-NAT por su facilidad de configuración y mantenimiento.

**Ventajas:**

- Funciona automáticamente tras CG-NAT
- Instalación sencilla
- MagicDNS y Subnet Routing
- ACLs centralizadas desde la web

**Instalación en Orange Pi (Armbian):**

```bash
curl -fsSL https://tailscale.com/install.sh | sh
sudo tailscale up
```
## 🛠️ Recomendaciones con Tailscale

- Activa **MagicDNS** para evitar usar IPs manualmente.
- Gestiona las reglas de acceso (ACLs) desde [admin.tailscale.com](https://admin.tailscale.com).
- Utiliza `--advertise-routes` si necesitas hacer **Subnet Routing** y exponer una red local completa.

---

## 🧠 Opción 2: ZeroTier (Avanzada)

ZeroTier permite crear redes virtuales más flexibles y complejas, similar a una VPN con funciones tipo SD-WAN.

### ✅ Ventajas

- Control completo sobre la **topología de red**
- Ideal para redes mixtas o VLANs virtuales
- Compatible con **bridge de red** y acceso entre subredes

### 🧪 Instalación

```bash
curl -s https://install.zerotier.com | sudo bash
sudo zerotier-cli join <NETWORK_ID>
```

🔗 **Requiere configuración adicional en:** [my.zerotier.com](https://my.zerotier.com)

---

## 📝 Notas

- Debes autorizar manualmente cada nuevo dispositivo desde el panel web.
- Es necesario configurar reglas de red para definir los flujos de tráfico y accesos.

---

## ⚖️ Comparativa rápida

| Característica        | Tailscale         | ZeroTier        |
|-----------------------|-------------------|-----------------|
| Soporte CG-NAT        | ✅ Sí             | ✅ Sí           |
| Facilidad de uso      | 🟢 Muy fácil      | 🟡 Media        |
| Control avanzado      | 🟡 Limitado       | 🟢 Avanzado     |
| Subnet Routing        | ✅ Sí             | ✅ Sí           |
| Interfaz de gestión   | Web sencilla      | Web avanzada    |
| Consumo de recursos   | Bajo              | Bajo            |

---

## 🔚 Consideraciones finales

- Si buscas algo simple y funcional rápidamente, **Tailscale** es la mejor opción.
- Si necesitas crear redes virtuales complejas entre múltiples ubicaciones o VLANs, considera usar **ZeroTier**.
- Ambas soluciones pueden coexistir para pruebas, pero **usa solo una en producción** para evitar conflictos de red.

