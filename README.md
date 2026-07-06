# 🧬 ParanoidCrypto

**Encriptación de texto basada en secuencias de ADN**

ParanoidCrypto es una aplicación web que transforma texto plano en secuencias de ADN (A, T, G, C) utilizando técnicas de codificación genética y cifrado XOR con SHA-256. Todo el procesamiento ocurre en el navegador del usuario — tus datos nunca tocan un servidor.

![ParanoidCrypt Logo](paranoid.gif)

---

## 🌟 Características

- 🔐 **Encriptación 100% client-side**: Tus datos nunca salen de tu navegador
- 🧬 **Codificación DNA**: Convierte texto en secuencias de nucleótidos (A, T, G, C)
- 🔑 **Cifrado XOR + SHA-256**: Protección adicional con clave secreta
- 🌍 **Multilingüe**: Español, Inglés y Portugués
- 📱 **Responsive**: Funciona en móvil, tablet y desktop
- 👁️ **Contador de visitas**: Estadísticas en tiempo real con Firebase
- 🎨 **Diseño cyberpunk**: Interfaz oscura con acentos en azul cian

---

## 🚀 Cómo usar

1. Abre `index.html` en tu navegador
2. Escribe tu mensaje secreto en el campo **INPUT**
3. (Opcional) Ingresa una clave secreta para mayor seguridad
4. Haz clic en **ENCRYPT** (o **EJECUTAR**) para encriptar
5. Copia la secuencia de ADN resultante
6. Para desencriptar, cambia a modo **DECRYPT**, pega la secuencia y usa la misma clave

---

## 🔒 Seguridad

- **SHA-256**: Implementación en JavaScript puro (sin dependencias externas)
- **XOR Cipher**: Cifrado simétrico con stream generado por SHA-256
- **Zero-knowledge**: El servidor nunca ve tus datos ni claves
- **Sin backend**: Todo ocurre en el navegador del usuario

> ⚠️ **Advertencia**: No usar para datos críticos sin capas adicionales de seguridad.

---

## 🛠️ Tecnologías

- HTML5, CSS3, JavaScript (ES6+)
- **Firebase Realtime Database** (contador de visitas)
- **Web Crypto API** (SHA-256)
- **Google Fonts**: JetBrains Mono, Fira Code, Source Code Pro

---

## 📦 Instalación local

```bash
# Clonar el repositorio
git clone https://github.com/paranoidcrypto/paranoidcrypto.git

# Entrar al directorio
cd paranoidcrypto

# Abrir en tu navegador
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux

## 🧬 Mis Proyectos

### ParanoidCrypt
Encriptación de texto basada en secuencias de ADN.

[![ParanoidCrypto](https://img.shields.io/badge/ParanoidCrypto-DNA_Encryption-00e5ff?style=for-the-badge)](https://github.com/paranoidcrypto/paranoidcrypto)
