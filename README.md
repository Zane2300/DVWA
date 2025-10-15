
# 🧠 DVWA Exploitation Lab

[![OWASP Top10](https://img.shields.io/badge/OWASP-Top%2010-red.svg)](https://owasp.org)
[![DVWA](https://img.shields.io/badge/DVWA-Lab-orange.svg)](https://github.com/digininja/DVWA)
[![Tools](https://img.shields.io/badge/Tools-Burp%20Suite%20%7C%20ZAP%20%7C%20cURL-blue.svg)]()
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> Repositorio con la documentación práctica de explotación de vulnerabilidades en **Damn Vulnerable Web Application (DVWA)**. Contiene guías por vulnerabilidad, payloads y capturas. Trabajo realizado en entorno controlado para aprendizaje.

---

## 📁 Estructura del repositorio

```
DVWA/
│
├── assets/                   # Capturas de pantalla de cada ataque y resultado
│   ├── brute_force_low.png
│   ├── sql_injection_low.png
│   ├── xss_stored_high.png
│   └── ...
│
├── Brute_Force.md
├── Command_Injection.md
├── CSP_Bypass.md
├── CSRF.md
├── File_Inclusion.md
├── File_Upload.md
├── JavaScript.md
├── SQL_Injection.md
├── SQL_Injection_Blind.md
├── Weak_Session_ID.md
├── XSS_Dom.md
├── XSS_Reflected.md
├── XSS_Stored.md
└── README.md
```

---

## 🧭 Tabla de contenido

- [Sobre el proyecto](#-sobre-el-proyecto)
- [Entorno de laboratorio](#-entorno-de-laboratorio)
- [Vulnerabilidades analizadas](#-vulnerabilidades-analizadas)
- [Cómo replicar el laboratorio](#-cómo-replicar-el-laboratorio)
- [Ejemplos y capturas](#-ejemplos-y-capturas)
- [Licencia](#-licencia)
- [Autor](#-autor)

---

## ℹ️ Sobre el proyecto

Este repositorio reúne documentación práctica y reproducible sobre pruebas de seguridad realizadas en **DVWA**, incluyendo:
- Explicación de cada vulnerabilidad.
- Payloads y ejemplos por nivel de seguridad (Low / Medium / High).
- Capturas de pantalla que muestran la explotación y resultados.

> **Propósito:** educacional. No utilices estas técnicas fuera de entornos autorizados.

---

## ⚙️ Entorno de laboratorio

- **Aplicación:** DVWA (Damn Vulnerable Web Application).  
- **Plataforma:** Kali Linux / Windows + XAMPP / LAMP local.  
- **Navegador:** Firefox (DevTools) / Chrome.  
- **Herramientas:** Burp Suite, OWASP ZAP, cURL, Python (requests), sqlmap (opcional).  
- **Niveles probados:** Low, Medium, High (según disponibilidad en DVWA).

---

## 🔍 Vulnerabilidades analizadas

Cada `*.md` incluye:
- Descripción técnica de la vulnerabilidad.
- Paso a paso de explotación en DVWA.
- Payloads y código empleado.
- Capturas de pantalla (`assets/`).

Listado:
- Brute Force
- Command Injection
- CSP Bypass
- CSRF
- File Inclusion (LFI/RFI)
- File Upload
- JavaScript / Payloads
- SQL Injection (Clásica)
- SQL Injection (Blind)
- Weak Session ID
- XSS (DOM, Reflected, Stored)

---

## ▶️ Cómo replicar el laboratorio (breve)

1. Clona DVWA oficial:  
   ```bash
   git clone https://github.com/digininja/DVWA.git
   ```
2. Instala un entorno LAMP (XAMPP / LAMP) y configura DVWA según su README.  
3. Asegura que PHP, MySQL y Apache funcionan y que la configuración de DVWA está completada (`config/config.inc.php`).  
4. Accede a DVWA en el navegador y selecciona el nivel de seguridad deseado (Low/Medium/High).  
5. Abre las guías del repo (`*.md`) y sigue los pasos con las herramientas indicadas.

---

## 🖼️ Ejemplos y capturas

Las capturas de cada vulnerabilidad están en `assets/`. Ejemplos rápidos:

- `assets/sql_injection_low.png` — SQL Injection (Low).  
- `assets/XSS_STORED_high.png` — XSS almacenado (High).  
- `assets/brute_force_low.png` — Fuerza bruta (Low).

Puedes incrustarlas en la documentación o verlas directamente en la carpeta `assets/`.

---

## 📜 Licencia

Este proyecto se publica bajo **MIT License**. Consulta el fichero `LICENSE` para más detalles.

---

## 👤 Autor

**Alex Rosell** — Técnico en Ciberseguridad y Administración de Sistemas.  
Contacto: enlace a tu perfil (LinkedIn / GitHub).