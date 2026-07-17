<div align="center">

# 🧬 ParanoidCrypto

**DNA-based text encryption web application**

[![License: MIT](https://img.shields.io/badge/License-MIT-ff2a2a?style=flat-square)](LICENSE)
[![Firebase](https://img.shields.io/badge/Firebase-Realtime_Database-FFCA28?style=flat-square&logo=firebase)](https://firebase.google.com)
[![ORCID](https://img.shields.io/badge/ORCID-0000--0002--8893--526X-A6CE39?style=flat-square&logo=orcid)](https://orcid.org/0000-0002-8893-526X)
[![GitHub](https://img.shields.io/badge/GitHub-paranoidcrypto-181717?style=flat-square&logo=github)](https://github.com/paranoidcrypto)
[![Version](https://img.shields.io/badge/Version-2.0-ff2a2a?style=flat-square)](https://github.com/paranoidcrypto/paranoidcrypto/releases)

![ParanoidCrypto Logo](paranoid.gif)

</div>

---

## 🌐 Languages / Idiomas / Idiomas

| Language | Link |
|----------|------|
| 🇪🇸 **Español** | [Ir a la sección en español](#español) |
| 🇬 **English** | [Go to English section](#english) |
| 🇧🇷 **Português** | [Ir para a seção em português](#portugues) |

---

<a id="español"></a>
## 🇪🇸 Español

**ParanoidCrypto v2.0** es una aplicación web que transforma texto plano en secuencias de ADN (A, T, G, C) utilizando técnicas de codificación genética, compresión BWT+MTF y cifrado XOR con SHA-256. Todo el procesamiento ocurre en el navegador del usuario — tus datos nunca tocan un servidor.

### 🌟 Características

- 🔐 **Encriptación 100% client-side**: Tus datos nunca salen de tu navegador
- 🧬 **Codificación DNA**: Convierte texto en secuencias de nucleótidos (A, T, G, C)
- 🗜️ **Compresión BWT+MTF**: Transformación Burrows-Wheeler + Move-to-Front para ocultar patrones y reducir tamaño
- 🔑 **Cifrado XOR + SHA-256**: Protección adicional con clave secreta
-  **24 diccionarios de mapeo**: Selección de permutaciones de nucleótidos para mayor seguridad
- 🌍 **Multilingüe**: Español, Inglés y Portugués
- 📱 **Responsive**: Funciona en móvil, tablet y desktop
- ️ **Contador de visitas**: Estadísticas en tiempo real con Firebase
- 🎨 **Diseño cyberpunk rojo**: Interfaz oscura con acentos en rojo neón

### 🚀 Cómo usar

1. Abre `index.html` en tu navegador
2. Escribe tu mensaje secreto en el campo **INPUT**
3. Selecciona el diccionario de nucleótidos (1-24)
4. (Opcional) Ingresa una clave secreta para mayor seguridad
5. Haz clic en **ENCRYPT** (o **EJECUTAR**) para encriptar
6. Copia la secuencia de ADN resultante
7. Para desencriptar, cambia a modo **DECRYPT**, pega la secuencia, selecciona el mismo diccionario y usa la misma clave

### 🔒 Seguridad

- **BWT+MTF**: Compresión que oculta patrones del texto original
- **SHA-256**: Implementación en JavaScript puro (sin dependencias externas)
- **XOR Cipher**: Cifrado simétrico con stream generado por SHA-256
- **24 diccionarios**: Múltiples esquemas de mapeo de bits a nucleótidos
- **Zero-knowledge**: El servidor nunca ve tus datos ni claves
- **Sin backend**: Todo ocurre en el navegador del usuario

> ️ **Advertencia**: No usar para datos críticos sin capas adicionales de seguridad.

### 🛠️ Tecnologías

- HTML5, CSS3, JavaScript (ES6+)
- **Firebase Realtime Database** (contador de visitas)
- **Web Crypto API** (SHA-256)
- **Google Fonts**: JetBrains Mono, Fira Code, Source Code Pro, Noto Sans SC

### 📦 Instalación local

```bash
# Clonar el repositorio
git clone https://github.com/paranoidcrypto/paranoidcrypto.git

# Entrar al directorio
cd paranoidcrypto

# Abrir en tu navegador
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
### 🔒 Seguridad

- **SHA-256**: Implementación en JavaScript puro (sin dependencias externas)
- **XOR Cipher**: Cifrado simétrico con stream generado por SHA-256
- **Zero-knowledge**: El servidor nunca ve tus datos ni claves
- **Sin backend**: Todo ocurre en el navegador del usuario

> ⚠️ **Advertencia**: No usar para datos críticos sin capas adicionales de seguridad.

### 🛠️ Tecnologías

- HTML5, CSS3, JavaScript (ES6+)
- **Firebase Realtime Database** (contador de visitas)
- **Web Crypto API** (SHA-256)
- **Google Fonts**: JetBrains Mono, Fira Code, Source Code Pro

### 📦 Instalación local

```bash
# Clonar el repositorio
git clone https://github.com/paranoidcrypto/paranoidcrypto.git

# Entrar al directorio
cd paranoidcrypto

# Abrir en tu navegador
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

### 🌐 Despliegue

Puedes desplegar esta página en:
- **GitHub Pages** (gratis) — recomendado
- **Netlify** (gratis)
- **Vercel** (gratis)
- Cualquier hosting estático

### 📊 Contador de visitas

El proyecto usa **Firebase Realtime Database** para contar visitas. Para configurarlo:

1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/)
2. Crea una **Realtime Database**
3. Configura las reglas de seguridad (ver `SECURITY.md`)
4. Reemplaza la configuración en `index.html` con tus credenciales

### 🤝 Contribuciones

Las contribuciones son bienvenidas. Por favor:

1. Abre un **issue** primero para discutir cambios mayores
2. Haz **fork** del repositorio
3. Crea una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
4. Haz **commit** de tus cambios
5. Haz **push** a la rama
6. Abre un **Pull Request**

---

<a id="english"></a>
## 🇬🇧 English

**ParanoidCrypto** is a web application that transforms plain text into DNA sequences (A, T, G, C) using genetic encoding techniques and XOR encryption with SHA-256. All processing occurs in the user's browser — your data never touches a server.

### 🌟 Features

- 🔐 **100% client-side encryption**: Your data never leaves your browser
- 🧬 **DNA encoding**: Converts text into nucleotide sequences (A, T, G, C)
- 🔑 **XOR + SHA-256 cipher**: Additional protection with a secret key
- 🌍 **Multilingual**: Spanish, English, and Portuguese
- 📱 **Responsive**: Works on mobile, tablet, and desktop
- 👁️ **Visitor counter**: Real-time statistics with Firebase
- 🎨 **Cyberpunk design**: Dark interface with cyan accents

### 🚀 How to use

1. Open `index.html` in your browser
2. Type your secret message in the **INPUT** field
3. (Optional) Enter a secret key for additional security
4. Click **ENCRYPT** (or **EXECUTE**) to encrypt
5. Copy the resulting DNA sequence
6. To decrypt, switch to **DECRYPT** mode, paste the sequence, and use the same key

### 🔒 Security

- **SHA-256**: Pure JavaScript implementation (no external dependencies)
- **XOR Cipher**: Symmetric cipher with SHA-256-derived keystream
- **Zero-knowledge**: The server never sees your data or keys
- **No backend**: Everything happens in the user's browser

> ⚠️ **Warning**: Do not use for critical data without additional security layers.

### 🛠️ Technologies

- HTML5, CSS3, JavaScript (ES6+)
- **Firebase Realtime Database** (visitor counter)
- **Web Crypto API** (SHA-256)
- **Google Fonts**: JetBrains Mono, Fira Code, Source Code Pro

### 📦 Local installation

```bash
# Clone the repository
git clone https://github.com/paranoidcrypto/paranoidcrypto.git

# Enter the directory
cd paranoidcrypto

# Open in your browser
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

### 🌐 Deployment

You can deploy this page on:
- **GitHub Pages** (free) — recommended
- **Netlify** (free)
- **Vercel** (free)
- Any static hosting

### 📊 Visitor counter

The project uses **Firebase Realtime Database** to count visits. To configure it:

1. Create a project at [Firebase Console](https://console.firebase.google.com/)
2. Create a **Realtime Database**
3. Configure security rules (see `SECURITY.md`)
4. Replace the configuration in `index.html` with your credentials

### 🤝 Contributions

Contributions are welcome. Please:

1. Open an **issue** first to discuss major changes
2. **Fork** the repository
3. Create a branch for your feature (`git checkout -b feature/new-feature`)
4. **Commit** your changes
5. **Push** to the branch
6. Open a **Pull Request**

---

<a id="portugues"></a>
## 🇧🇷 Português

**ParanoidCrypto** é um aplicativo web que transforma texto plano em sequências de DNA (A, T, G, C) usando técnicas de codificação genética e criptografia XOR com SHA-256. Todo o processamento ocorre no navegador do usuário — seus dados nunca tocam um servidor.

### 🌟 Características

- 🔐 **Criptografia 100% client-side**: Seus dados nunca saem do seu navegador
- 🧬 **Codificação DNA**: Converte texto em sequências de nucleotídeos (A, T, G, C)
- 🔑 **Cifra XOR + SHA-256**: Proteção adicional com chave secreta
- 🌍 **Multilíngue**: Espanhol, Inglês e Português
- 📱 **Responsivo**: Funciona em celular, tablet e desktop
- 👁️ **Contador de visitas**: Estatísticas em tempo real com Firebase
- 🎨 **Design cyberpunk**: Interface escura com acentos em azul ciano

### 🚀 Como usar

1. Abra `index.html` no seu navegador
2. Digite sua mensagem secreta no campo **INPUT**
3. (Opcional) Insira uma chave secreta para segurança adicional
4. Clique em **ENCRYPT** (ou **EXECUTAR**) para criptografar
5. Copie a sequência de DNA resultante
6. Para descriptografar, mude para o modo **DECRYPT**, cole a sequência e use a mesma chave

### 🔒 Segurança

- **SHA-256**: Implementação em JavaScript puro (sem dependências externas)
- **Cifra XOR**: Cifra simétrica com fluxo derivado de SHA-256
- **Zero-knowledge**: O servidor nunca vê seus dados ou chaves
- **Sem backend**: Tudo acontece no navegador do usuário

> ⚠️ **Aviso**: Não use para dados críticos sem camadas adicionais de segurança.

### 🛠️ Tecnologias

- HTML5, CSS3, JavaScript (ES6+)
- **Firebase Realtime Database** (contador de visitas)
- **Web Crypto API** (SHA-256)
- **Google Fonts**: JetBrains Mono, Fira Code, Source Code Pro

### 📦 Instalação local

```bash
# Clonar o repositório
git clone https://github.com/paranoidcrypto/paranoidcrypto.git

# Entrar no diretório
cd paranoidcrypto

# Abrir no seu navegador
open index.html       # macOS
start index.html      # Windows
xdg-open index.html   # Linux
```

### 🌐 Implantação

Você pode implantar esta página em:
- **GitHub Pages** (grátis) — recomendado
- **Netlify** (grátis)
- **Vercel** (grátis)
- Qualquer hospedagem estática

### 📊 Contador de visitas

O projeto usa **Firebase Realtime Database** para contar visitas. Para configurá-lo:

1. Crie um projeto no [Firebase Console](https://console.firebase.google.com/)
2. Crie um **Realtime Database**
3. Configure as regras de segurança (veja `SECURITY.md`)
4. Substitua a configuração no `index.html` com suas credenciais

### 🤝 Contribuições

Contribuições são bem-vindas. Por favor:

1. Abra uma **issue** primeiro para discutir mudanças maiores
2. Faça **fork** do repositório
3. Crie uma branch para sua feature (`git checkout -b feature/nova-funcionalidade`)
4. Faça **commit** das suas mudanças
5. Faça **push** para a branch
6. Abra um **Pull Request**

---

## 👨‍💻 Autor / Author / Autor

**Paris Lavin**  
🔗 ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)  
🌐 GitHub: [paranoidcrypto](https://github.com/paranoidcrypto)

Investigador y desarrollador interesado en la intersección entre biología computacional, criptografía y bioinformática.

*Researcher and developer interested in the intersection of computational biology, cryptography, and bioinformatics.*

*Pesquisador e desenvolvedor interessado na interseção entre biologia computacional, criptografia e bioinformática.*

---

## 📄 Licencia / License / Licença

Este proyecto está bajo la licencia **MIT**. Ver [LICENSE](LICENSE) para más detalles.

*This project is licensed under the **MIT License**. See [LICENSE](LICENSE) for details.*

*Este projeto está sob a licença **MIT**. Veja [LICENSE](LICENSE) para mais detalhes.*

---

## 🙏 Créditos / Credits / Créditos

| Componente / Component / Componente | Autor / Author / Autor | Licencia / License / Licença |
|-------------------------------------|------------------------|------------------------------|
| Firebase SDK | Google Inc. | Apache 2.0 |
| JetBrains Mono | JetBrains | OFL |
| Fira Code | Nikita Prokopov | OFL |
| Source Code Pro | Adobe | OFL |
| SHA-256 | Based on FIPS 180-4 | Public domain |
| ORCID iD icon | ORCID, Inc. | CC BY 4.0 |

---

## 📬 Contacto / Contact / Contato

¿Preguntas o sugerencias? Abre un **issue** en este repositorio o contacta al autor vía ORCID.

*Questions or suggestions? Open an **issue** in this repository or contact the author via ORCID.*

*Dúvidas ou sugestões? Abra uma **issue** neste repositório ou entre em contato com o autor via ORCID.*

---

<div align="center">

**ParanoidCrypto** · Built with DNA, paranoia & caffeine · 2026

[![ORCID](https://img.shields.io/badge/ORCID-0000--0002--8893--526X-A6CE39?style=flat-square&logo=orcid)](https://orcid.org/0000-0002-8893-526X)
[![License: MIT](https://img.shields.io/badge/License-MIT-00e5ff?style=flat-square)](LICENSE)
[![GitHub](https://img.shields.io/badge/GitHub-paranoidcrypto-181717?style=flat-square&logo=github)](https://github.com/paranoidcrypto)

</div>
