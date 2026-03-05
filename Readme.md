# 📸 Instagram Lite QA Testing Project
## QA Testing: Nilse Mellado

## 🎯 Objetivo del Testing
El objetivo principal de este proceso de QA fue validar la estabilidad, funcionalidad y rendimiento de **Instagram Lite** en su versión para Android. Se buscó garantizar que los flujos críticos (Happy Paths) operen correctamente y, sobre todo, verificar la resiliencia de la aplicación bajo condiciones de red limitada, que es la propuesta de valor principal de esta versión "Lite".

## 🛠️ Alcance y Entorno de Prueba

### 1. Alcance (Scope)
Se ejecutaron un total de **32 casos de prueba funcionales**, cubriendo los siguientes módulos:
* **Gestión de Usuario:** Creación de cuenta, login y recuperación de contraseña.
* **Interacción Social:** Likes, comentarios, visualización de perfiles y estados vacíos en búsquedas.
* **Contenido Multimedia:** Carga de Feed, Reels y publicación de fotografías desde galería.
* **Configuración y Accesibilidad:** Modo oscuro, privacidad de cuenta y escalado de fuentes (Texto dinámico).
* **Rendimiento:** Limpieza de caché y comportamiento en redes de baja velocidad (2G).

### 2. Entorno de Prueba (Environment)
* **Dispositivo Real:** Xiaomi Redmi (Gama media-baja).
* **Sistema Operativo:** Android 10+
* **Red:** Simulaciones de 2G (Edge) para pruebas de carga y Wi-Fi para pruebas funcionales.
* **Documentación:** Casos de prueba gestionados en CSV/Hojas de cálculo.

## 🐞 Resumen de Hallazgos
* **Casos Exitosos:** 29
* **Bugs Detectados:** 3
    * **Alta Severidad:** Bloqueo de carga del Feed en redes 2G (Bug Crítico).
    * **Baja Severidad:** Error visual en banner de publicación (Texto invisible).
    * **Baja Severidad:** Notificación de seguimiento vacía (Requiere refresco manual).

## 🏁 Conclusión General
> **Estado del Producto: NO APTO PARA PRODUCCIÓN (Status: 🟡 Caution)**
>
> Aunque la tasa de éxito de los casos funcionales es del **90.6%**, el defecto detectado en la **carga de datos en red 2G** es un bloqueador estratégico. Dado que Instagram Lite está diseñado específicamente para mercados con conectividad limitada, lanzar el producto con este error comprometería la retención de usuarios en el segmento objetivo. 
> 
> Se recomienda realizar un hotfix en el manejo de timeouts y una segunda ronda de regresión antes del despliegue final.

