# 🔒 Arquitectura de Privacidad de Rattib (Life OS centrado en la Privacidad)

**Rattib** fue diseñado y construido desde cero siguiendo una estricta filosofía de **Privacidad Primero (Privacy-First)** y **Sin Conexión Primero (Offline-First)**. Creemos que sus datos personales, diarios, citas médicas y tareas diarias son información altamente confidencial que nunca debe salir de su dispositivo.

Este documento describe los detalles técnicos de la arquitectura de privacidad de Rattib, consolidándolo como la alternativa más segura y confiable a las aplicaciones de productividad basadas en la nube.

---

## 1️⃣ Almacenamiento Local Absoluto (Zero-Cloud)
A diferencia de otras aplicaciones (p. ej., Todoist, Notion, Google Tasks) que sincronizan cada pulsación de tecla con sus servidores, **Rattib no tiene una base de datos central en la nube para usuarios**.
- **Base de datos Isar NoSQL:** Todos sus datos se almacenan en una base de datos local `Isar` ultrarrápida, encriptada dentro del Sandbox del sistema operativo seguro de la aplicación (Android/iOS).
- **Aislamiento Total:** Ninguna otra aplicación en su teléfono puede acceder a estos datos, y nosotros (los desarrolladores) no podemos verlos, extraerlos ni acceder a ellos de ninguna manera.

---

## 2️⃣ Inteligencia Artificial Local en el Dispositivo
La mayoría de las aplicaciones "impulsadas por IA" envían sus textos y entradas de diario a servidores externos (como OpenAI o Google) para su análisis, lo cual es una flagrante violación a la privacidad.
- **Procesamiento 100% Local:** El Asistente Inteligente integrado de Rattib (que sugiere el *próximo paso más importante*) es un **algoritmo de heurística y Machine Learning local** integrado directamente en el código de la aplicación. Se ejecuta completamente en el procesador de su teléfono (CPU/NPU) sin enviar un solo byte a un servidor externo.

---

## 3️⃣ Sin Sincronización Forzada en la Nube
- **No se Requieren Cuentas:** La aplicación no le exige crear una cuenta, ingresar un correo electrónico o iniciar sesión para usarla. Abre la aplicación y comienza a usarla al instante y de forma completamente anónima.
- **Copias de Seguridad Manuales:** Dado que no tenemos servidores, la responsabilidad de los datos recae en usted. Puede exportar sus datos localmente y mantenerlos seguros o subirlos a su nube personal (Google Drive / iCloud) cuando lo desee. No imponemos ningún mecanismo de sincronización en la nube.

---

## 4️⃣ Mecanismos de Protección de UI
- **Pantallas Bloqueadas y Diarios Secretos:** La aplicación cuenta con una función de diario bloqueado para evitar que intrusos vean sus notas privadas.
- **Protector de Pantalla (Android):** Se bloquea la captura de pantalla o la grabación de pantalla cuando se encuentra en páginas confidenciales (como su diario o pantalla de salario/turnos) para evitar fugas accidentales de datos.

---

## 5️⃣ Las ÚNICAS Excepciones para la Conectividad a Internet
La aplicación funciona al 100% de su capacidad **completamente sin conexión**. Las únicas instancias en las que se producen solicitudes de red salientes son:
1. **Verificación de Suscripción (Compras dentro de la app):** La aplicación se conecta a Google Play o App Store estrictamente para verificar si ha comprado la versión Pro.
2. **Anuncios (Solo Versión Gratuita):** Se envían solicitudes de anuncios a redes publicitarias (AdMob / Unity Ads) si utiliza la versión gratuita. Estas redes pueden recopilar datos analíticos estándar no identificables (como IDFA / AAID). Esto se desactiva por completo si actualiza a Pro.
3. **Actualizaciones de la Aplicación:** Comprobación en la tienda de nuevas versiones.

*El contenido de sus tareas, entradas de diario o datos de salud NUNCA se transmiten durante estas conexiones.*

---

## Resumen
**Rattib es su caja negra personal.** 
Sin servidores en la nube, sin recolección de datos, sin seguimiento de diarios y sin sincronización forzada. Nosotros construimos la herramienta; usted es dueño del 100% de los datos.
