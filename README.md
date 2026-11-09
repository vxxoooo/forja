# FORJA — prototipo de app de entrenamiento

## Qué incluye
- Perfil físico (edad, estatura, peso, nivel).
- Objetivos: hipertrofia, fuerza/potencia, resistencia, movilidad y rendimiento deportivo.
- Disponibilidad, tiempo por sesión y equipamiento.
- Generación local de una rutina base.
- Registro local de sesiones y progreso.
- Diseño adaptable a móvil y PWA instalable.

## Ejecutar en el computador
Abre `www/index.html` en un navegador. Para probar instalación PWA, sírvelo por HTTPS o localhost.

## Convertir a APK
Este paquete incluye la app web. No incluye un APK compilado: el entorno de esta sesión no tiene Android SDK/Gradle instalados.
Para generar APK, se puede envolver `www/` con Capacitor en un equipo con Android Studio:
1. Instala Node.js y Android Studio.
2. Ejecuta en una carpeta de proyecto:
   `npm init -y`
   `npm install @capacitor/core @capacitor/cli @capacitor/android`
3. Crea `capacitor.config.json` con:
   `{ "appId": "com.forja.fit", "appName": "FORJA", "webDir": "www" }`
4. Ejecuta:
   `npx cap add android`
   `npx cap sync android`
   `npx cap open android`
5. En Android Studio: Build > Build Bundle(s) / APK(s) > Build APK(s).

## Seguridad y alcance
Este es un MVP educativo, no un entrenador clínico. Las rutinas son plantillas generales, no usan IA generativa ni evaluación médica. No se recomiendan cargas máximas. Las personas menores de edad, con lesiones o condiciones médicas deben entrenar con supervisión adecuada. Antes de publicar, añadir backend seguro, consentimiento, privacidad, revisión profesional y pruebas.
