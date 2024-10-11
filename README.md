# Cagómetro Viewer

Cagómetro Viewer es una webapp divertida e interactiva desarrollada con **React** que permite a los usuarios visualizar y analizar datos relacionados con su tránsito intestinal recopilados por un bot de Telegram. La aplicación se conecta a **Firebase** para almacenar los datos y mostrar gráficos y visualizaciones interesantes.

## Tecnologías Utilizadas
- **React**: Framework de JavaScript para la creación de la interfaz de usuario.
- **Firebase**: Base de datos en la nube para almacenar y sincronizar datos.
- **Chart.js**: Librería para visualizaciones y gráficos interactivos.
- **GitHub Pages**: Hosting estático para desplegar la aplicación.

## Características
- Visualiza registros de tránsito con una interfaz simple y amigable.
- Gráficos interactivos para mostrar patrones y frecuencia del tránsito.
- Rankings y visualizaciones grupales para hacerlo más divertido.

## Instalación y Configuración
Sigue estos pasos para configurar el proyecto en tu entorno local o en GitHub Codespaces.

### 1. Clonar el Repositorio
```bash
 git clone https://github.com/tu-usuario/cagometro-viewer.git
 cd cagometro-viewer
```

### 2. Instalar Dependencias
Asegúrate de tener **Node.js** instalado y ejecuta:
```bash
npm install
```

### 3. Configurar Firebase
1. Crea un proyecto en [Firebase Console](https://console.firebase.google.com/).
2. Añade una aplicación web y copia la configuración de Firebase (API key, Auth domain, etc.).
3. Crea un archivo `src/firebaseConfig.js` y pega la configuración:
   ```javascript
   import { initializeApp } from 'firebase/app';
   import { getFirestore } from 'firebase/firestore';

   const firebaseConfig = {
     apiKey: "TU_API_KEY",
     authDomain: "TU_AUTH_DOMAIN",
     projectId: "TU_PROJECT_ID",
     storageBucket: "TU_STORAGE_BUCKET",
     messagingSenderId: "TU_MESSAGING_SENDER_ID",
     appId: "TU_APP_ID"
   };

   const app = initializeApp(firebaseConfig);
   const db = getFirestore(app);

   export { db };
   ```

### 4. Ejecutar la Aplicación en Local
Para arrancar la aplicación en desarrollo:
```bash
npm start
```
La aplicación estará disponible en [http://localhost:3000](http://localhost:3000).

## Despliegue en GitHub Pages
### 1. Instalar gh-pages
```bash
npm install gh-pages
```

### 2. Configurar `package.json`
Añade la propiedad `homepage` y los scripts de despliegue:
```json
"homepage": "https://tu-usuario.github.io/cagometro-viewer",
"scripts": {
  "predeploy": "npm run build",
  "deploy": "gh-pages -d build"
}
```

### 3. Desplegar
```bash
npm run deploy
```
Esto construirá la aplicación y la subirá al branch `gh-pages`, donde estará alojada.

## Contribuir
Si deseas contribuir al proyecto, eres bienvenido. Puedes abrir **issues** o **pull requests** para sugerir mejoras, reportar errores o añadir nuevas características.

## Licencia
Este proyecto está bajo la licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---
¡Diviértete con el **Cagómetro Viewer** y mantén tu tránsito controlado de la forma más entretenida posible! 😄💩
