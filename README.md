# React Folders Structure

Aplicación ReactJS con estructura de carpetas intermedia. Artículo completo donde explico todas las carpetas y sus funciones.

## Tabla de contenido

- [Getting started](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#getting-started)

- [Extensiones](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#extensiones)

- [Estructura](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#estructura)

  - [Assets](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-assets)
  - [Components](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-components)
  - [Containers](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-containers)
  - [Constants](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-constants)
  - [Helpers](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-helpers)
  - [Hooks](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-hooks)
  - [Layouts](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-layouts)
  - [Pages](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-pages)
  - [Validations](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-validations)
  - [Services](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-services)
  - [Contexts](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-contexts)
  - [Config](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-config)
  - [i18n](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#-i18n)

- [GitFlow](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#gitflow)

- [Guia de estilos](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#guia-de-estilos)

![landing screenshot]('/screenshots/)

## Getting started

```js

  // install all dependencies
  npm install

  // run react server
  npm run start

  // run docs server
  npm run styleguide

  // build final doc
  npm run styleguide:build
```

## Extensiones

##### Extensiones que complementan la estructura:

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [GitGraph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
- [GitHistory](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)

##### Extensiones opcionales:

- [Paquetes de iconos](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
- [Color the tag name](https://marketplace.visualstudio.com/items?itemName=jzmstrjp.color-the-tag-name)
- [ES7+ React/Redux/React-Native snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets)
- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [JavaScript (ES6) code snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)
- [JS JSX Snippets](https://marketplace.visualstudio.com/items?itemName=skyran.js-jsx-snippets)
- [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
- [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

## Estructura

```cmd
src/
├─ assets/
│  ├─ fonts/
│  ├─ images/
│  ├─ scss/
├─ components/
├─ config/
├─ containers/
├─ context/
├─ hooks/
├─ helpers/
├─ i18n/
│  ├─ en/
│  ├─ fr/
│  ├─ es/
├─ layouts/
├─ pages/
├─ services/
├─ validations/
```

### **📁 Assets**

- Aquí agrupamos todos nuestros archivos multimedia.
- Contiene subcarpetas como **`Images, Icons, Videos, Audios`,** etc.

### **📁 Components**

- Esta carpeta contiene todos los componentes de presentación de nuestra aplicación (Stateless Components).

  ```jsx
  import React from 'react';

  const Stateless = () => {
    return <h1>¡Hola!</h1>;
  };

  export default Stateless;
  ```

### **📁 Containers**

- En esta carpeta tenemos los componentes Stateful (Smart component) donde seguimos rastreando el estado.

  ```jsx
  import React, { Component, useState } from 'react';

  const Stateful = () => {

    const [state, setState] = useState({ hello: 'hello world' })

  	return <h1>{this.state.hello}</h1>;
  };

  export default Stateful;

  // or

  class Stateful extends Component {
    constructor(props) {
      super(props);

      this.state = { hello: 'hello world' };
    }

    render() {
      return <h1>{this.state.hello}</h1>;
    }
  }

  export default Stateful;
  ```

### **📁 Constants**

- En este archivo agrupamos todas las constantes como regex.

### **📁 Helpers**

- Aquí creamos y exportamos funciones que serán reutilizadas en diferentes lugares de nuestra aplicación.

### **📁 Hooks**

- Una carpeta hecha para ganchos personalizados.

### **📁 Layouts**

- Contiene archivos de diseño como .**`Navbar, Footer, Sidebar`**
- Los diseños se utilizan para envolver un componente específico.

### **📁 Pages**

- Esta carpeta contiene componentes de páginas como etc...**`Home, Contact`**
- Cada página envuelta con un **`Layout`**

### **📁 Validations**

> Aquí escribimos nuestra validación de formularios y reglas utilizando una biblioteca como Formik o react-hook-form.

### **📁 Services**

- En esta carpeta gestionamos todas las solicitudes de API creando archivos para cada servicio.

### **📁 Contexts**

- Esta carpeta contiene todos los archivos de contexto donde gestionamos y globalizamos el estado en nuestra aplicación como estilos de tematización.

### **📁 Config**

- Toda la configuración de nuestra aplicación estará aquí en esta carpeta.

### **📁 i18n**

- Esta carpeta está hecha para soporte multi-idioma.
- Puede crear subcarpetas con un archivo para cada idioma que desee traducir.**`JSON`**
- Echa un vistazo a su guía Paso a Paso **_[AQUÍ](https://react.i18next.com/latest/using-with-hooks)_**.

## GitFlow

El flujo general de Gitflow es el siguiente:

- Se crea una rama master a partir de main.
- Se crea una rama release a partir de la master.
- Se crean ramas feature a partir de la master.
- Cuando se termina una rama feature, se fusiona en la rama master.
- Cuando la rama release está lista, se fusiona en las ramas master y main.
- Si se detecta un problema en main, se crea una rama hotfix a partir de main.
- Una vez terminada la rama hotfix, esta se fusiona tanto en master como en main.

## Guia de estilos

### Principios

- Mantenerlo simple y reusar lo más posible.
- Un código que luzca como si una sola persona lo haya escrito
- Escribir para escalabilidad.

### Estructura

![style_guide](/screenshots/style_guide.png)

### Generales

- Usamos **BEM** como metodología de creación de código.
- Nombre de archivos en plural (**Ejemplo**: buttons.scss)
- Clases en singular y minúsculas (Ejemplo: .gallery\_\_button)
- Nombrar imágenes relativas a su bloque. (Ejemplo: hero_background.png)

### Sintaxis

1.  Espacio después del selector y antes de {}
2.  Espacios para indentación.
3.  Espacio después del :
    1. Bloques de CSS separados por 2 líneas
    2. Evitar abuso de anidaciones. Limite 1 nivel
    3. Mixins para tamaño, estilos y valores numéricos de fuentes.

### Manejo de propiedades

Propiedades y selectores deben ordenarse de la siguiente forma:

- Propiedades del modelo de caja (display, width, height, margin, etc)
- Posicionamiento (position, left, top, right, etc)
- Tipografía (text-transform, text-decoration)
- Decoración (background-image, color, etc)
- Variables
- Mixins

### Ejemplo de código:

```scss
.button {
  padding: 20px 30px;
  display: block;
  position: relative;
  width: 220px;
  height: 40px;
  text-transform: uppercase;
  font-weight: $semibold;
  color: #ffff;
  background-color: #333333;
  @include font-size(13px);
}
```
