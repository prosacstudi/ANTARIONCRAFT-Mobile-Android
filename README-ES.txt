ANTARIONCRAFT Mobile — proyecto Android inicial

Incluye interfaz Kotlin de estilo cósmico/azul eléctrico, dirección del servidor,
botón para abrir Minecraft Bedrock y botón para copiar la dirección.

Servidor según los datos compartidos:
  va28.holy.gg
  Puerto Bedrock: 19551 UDP
La captura confirma que Geyser está configurado con ese puerto; no confirma que el
hosting permita tráfico UDP desde Internet. Ejecuta en la consola del servidor:
  geyser connectiontest va28.holy.gg 19551

Limitación: el botón abre Minecraft, pero Android no garantiza que Minecraft agregue
automáticamente un servidor externo. Si no aparece, el jugador debe añadirlo en
Servidores con host va28.holy.gg y puerto 19551.

Generar APK:
1. Abrir esta carpeta en Android Studio.
2. Esperar la sincronización de Gradle.
3. Build > Build APK(s).
4. APK debug: app/build/outputs/apk/debug/app-debug.apk

Este proyecto no modifica el launcher Java EXE.

COMPILACIÓN EN LA NUBE (sin instalar Android Studio en tu PC)
1. Crea un repositorio en GitHub y sube el CONTENIDO de esta carpeta a la raíz del repositorio.
2. Asegúrate de incluir la carpeta .github/workflows/build-apk.yml.
3. En GitHub abre la pestaña Actions.
4. Si aparece un aviso para habilitar Actions, actívalo.
5. Abre “Compilar APK ANTARIONCRAFT Mobile” y pulsa “Run workflow”.
6. Cuando termine en verde, abre la ejecución y descarga “ANTARIONCRAFT-Mobile-debug-APK” en Artifacts.
7. Descomprime ese archivo en el teléfono y abre app-debug.apk para instalarlo.

NOTAS:
- Esta compilación se ejecuta en servidores de GitHub, no en tu PC.
- Este flujo genera un APK de depuración para probar, no una versión firmada para publicar.
- La compilación no verifica por sí sola que el puerto UDP de Geyser sea accesible desde Internet.
