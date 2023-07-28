# Yes or Not App con Vite y Vue

Este es un proyecto que implementa una aplicación "Yes or Not" utilizando Vite y Vue, y consumiendo la API de yesnot.wtf para obtener respuestas aleatorias de "sí" o "no".

## Requisitos previos

Asegúrate de tener instalado Node.js en tu sistema. Puedes descargarlo e instalarlo desde el sitio web oficial de Node.js: https://nodejs.org/

## Instalación

Clona este repositorio en tu máquina local usando el siguiente comando:

```bash
git clone https://github.com/tu-usuario/yes-or-not-app.git
```

Navega al directorio del proyecto:

```bash
cd yes-or-not-app
```

Instala las dependencias del proyecto:

```bash
npm install
```

## Uso

Una vez que hayas instalado todas las dependencias, puedes iniciar la aplicación usando el siguiente comando:

```bash
npm run dev
```

Esto iniciará la aplicación en modo de desarrollo. Luego, puedes abrir tu navegador y acceder a http://localhost:5173 para ver la aplicación en funcionamiento.

En la página web, simplemente haz clic en el botón "Obtener respuesta" para obtener una respuesta aleatoria de "sí" o "no" de la API de yesnot.wtf.

## Despliegue

En caso de requerir desplegar en un hosting como netlify, heroku, etc., puedes construir la aplicación con el siguiente código:

```bash
npm run build
```

Esto generara una carpeta de distribución en la raíz del proyecto.

## Personalización

Si deseas personalizar o modificar la aplicación, aquí hay algunos puntos importantes que podrías considerar:

Estilos: Los estilos de la aplicación se encuentran en el archivo src/components/YesOrNot.vue en el tag de styles. Siéntete libre de modificarlos para adaptar el diseño a tus necesidades.

Componentes: Los componentes de Vue se encuentran en el directorio src/components. Puedes agregar nuevos componentes o modificar los existentes para ampliar las funcionalidades.

API: Si por alguna razón la API de yesnot.wtf ya no está disponible o deseas cambiarla por otra, puedes modificar la llamada a la API en el archivo src/components/YesOrNot.vue. Asegúrate de adaptar el formato de la respuesta según corresponda.

## Contribución

¡Las contribuciones son bienvenidas! Si encuentras errores, tienes ideas para nuevas características o mejoras, o simplemente deseas colaborar, siéntete libre de crear un issue o enviar un pull request.

## Licencia

Este proyecto está bajo la licencia MIT. Si utilizas o te inspiras en este proyecto, te agradeceríamos que menciones el repositorio original.

## Agradecimientos

Este proyecto fue creado con Vite y Vue, dos herramientas poderosas para el desarrollo web. También agradecemos a la API de yesnot.wtf por proporcionar respuestas divertidas y aleatorias.

¡Esperamos que disfrutes usando esta aplicación "Yes or Not"! Si tienes alguna pregunta o sugerencia, no dudes en contactarnos. ¡Diviértete!
