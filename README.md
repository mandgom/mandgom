# 🕵️‍♂️ Perfil Profesional de Mario
## ¡Bienvenido! Soy Mario 👋
### Estudiante de Desarrollo de Aplicaciones Web (DAW) y apasionado del Red Teaming
---

## Sobre mi 🤔
Actualmente sigo estudiando el segundo año de *DAW* y me gustaría avanzar mucho más que eso, seguir estudiando y aprendiendo. Tambien lo hago por mi cuenta, ya que mi pasion siempre y por siempre sera la **ciberseguridad**. Lo estudio y practico en mi unidad de almacenamiento portable con un doble cifrado de acceso a unidad y *S.O* Debian 12 Personalizado.

Con mucha ~~paciencia~~ disciplina he construido una mentalidad muy centrada en lo que quiero de verdad: entender cómo se construyen las aplicaciones para aprender a protegerlas (o romperlas).
> Mi pasión quiero que sea mi futuro. 

---

## 🎯 Mis Objetivos y Foco
El desarrollo web es mi base, pero la seguridad ofensiva es mi vocacion.

**Arsenal de Intereses:**
* Analisis de Vulnerabilidades Web
* Red Teaming y Escalada de Privilegios
* Criptografia Aplicada y SecDevOps

**Roadmap Profesional:**
1. Dominar el desarrollo backend seguro en mi ciclo superior
2. Prepararme para certificaciones ofensivas prácticas
3. Encontrar vulnerabilidades y participar en programas de Bug Bounty

**Checklist del Ciclo DAW:**
- [x] Sobrevivir y dominar DAW
- [ ] Desplegar mi portafolio integrando buenas prácticas de seguridad
- [ ] Destacar en mis prácticas de empresa auditando codigo

---

## 🧰 Mi Caja de Herramientas
La terminal es mi habitat natural. Ya dejamos atras los escaneos basicos, ahora prefiero investigar tecnicas de evasion, testear inyecciones avanzadas lanzando comandos como `sqlmap --level=5 --risk=3 --tamper=space2comment` como pequeño ejemplo o generando payloads especificos como este: `msfvenom -p linux/x64/meterpreter/reverse_tcp`.

![Metasploit](https://img.shields.io/badge/Metasploit-2C5199?style=for-the-badge&logo=metasploit&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white)
![Burp Suite](https://img.shields.io/badge/Burp_Suite-FF6633?style=for-the-badge&logo=BurpSuite&logoColor=white)

## 💻 Un poco de código
Me encanta automatizar la recolección de información (OSINT/Recon). Aqui dejo un *snippet* simple de un script en el que trabajo para extraer cabeceras HTTP de forma sigilosa:

```python
import requests

def sgrabber(url):
    headers = {'User-Agent': 'Mozilla/5.0 (Windows NT 10.0; Win64; x64)'}
    try:
        print(f"lanzando peticion...")
        respuesta = requests.get(url, headers=headers, timeout=5)
        server = respuesta.headers.get('Server', 'Oculto')
        print(f"servidor detectado: {server}")
        return server
    except Exception as e:
        print(f"objetivo inalcanzable, motivo: {e}")

sgrabber("http://localhost:8080")
