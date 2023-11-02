# React Folders Structure

React Folders Structure is an Atomic Design-based design system that provides an efficient folder structure for ReactJS projects. With intuitively organized components, services, and validations, this system facilitates code maintenance and scalability. It includes tools such as ESLint and Prettier, as well as a comprehensive style guide, to ensure clean and consistent code.

## Table of Contents

- [Getting started](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#getting-started)
- [Extensions](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#extensions)
- [Structure](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#structure)
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
- [Style Guide](https://github.com/Kevinparra535/design-sytem-and-gitflow/tree/master#style-guide)

![landing screenshot]('/screenshots/)

## Getting Started

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

## Extensions

##### Extensions that complement the structure:

- [ESLint](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)
- [Prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
- [GitLens](https://marketplace.visualstudio.com/items?itemName=eamodio.gitlens)
- [GitGraph](https://marketplace.visualstudio.com/items?itemName=mhutchie.git-graph)
- [GitHistory](https://marketplace.visualstudio.com/items?itemName=donjayamanne.githistory)

##### Optional extensions:

- [Icon Packages](https://marketplace.visualstudio.com/items?itemName=PKief.material-icon-theme)
- [Path Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.path-intellisense)
- [Color Highlight](https://marketplace.visualstudio.com/items?itemName=naumovs.color-highlight)
- [Color the Tag Name](https://marketplace.visualstudio.com/items?itemName=jzmstrjp.color-the-tag-name)
- [ES7+ React/Redux/React-Native Snippets](https://marketplace.visualstudio.com/items?itemName=dsznajder.es7-react-js-snippets)
- [GitHub Copilot](https://marketplace.visualstudio.com/items?itemName=GitHub.copilot)
- [JavaScript (ES6) Code Snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets)
- [JS JSX Snippets](https://marketplace.visualstudio.com/items?itemName=skyran.js-jsx-snippets)
- [npm Intellisense](https://marketplace.visualstudio.com/items?itemName=christian-kohler.npm-intellisense)
- [Settings Sync](https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync)

## Structure

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

- Here we group all our multimedia files.
- Contains subfolders such as **`Images, Icons, Videos, Audios`,** etc.

### **📁 Components**

- This folder contains all the presentation components of our application (Stateless Components).

  ```jsx
  import React from 'react';

  const Stateless = () => {
    return <h1>Hello!</h1>;
  };

  export default Stateless;
  ```

### **📁 Containers**

- In this folder, we have the Stateful (Smart component) components where we keep track of the state.

  ```jsx
  import React, { Component, useState } from 'react';

  const Stateful = () => {
    const [state, setState] = useState({ hello: 'hello world' });
    return <h1>{state.hello}</h1>;
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

- In this file, we group all the constants like regex.

### **📁 Helpers**

- Here we create and export functions that will be reused in different places of our application.

### **📁 Hooks**

- A folder made for custom hooks.

### **📁 Layouts**

- Contains layout files such as **`Navbar, Footer, Sidebar`**.
- Layouts are used to wrap a specific component.

### **📁 Pages**

- This folder contains page components such as **`Home, Contact`**.
- Each page is wrapped with a **`Layout

`**.

### **📁 Validations**

> Here we write our form validations and rules using a library like Formik or react-hook-form.

### **📁 Services**

- In this folder, we manage all the API requests by creating files for each service.

### **📁 Contexts**

- This folder contains all the context files where we manage and globalize the state in our application, like theme styles.

### **📁 Config**

- All the configuration of our application will be here in this folder.

### **📁 i18n**

- This folder is made for multi-language support.
- You can create subfolders with a file for each language you want to translate. **`JSON`**
- Check out their Step by Step Guide **_[HERE](https://react.i18next.com/latest/using-with-hooks)_**.

## GitFlow

The general Gitflow is as follows:

- A master branch is created from main.
- A release branch is created from master.
- Feature branches are created from master.
- When a feature branch is finished, it merges into master.
- When the release branch is ready, it merges into both master and main.
- If a problem is detected in main, a hotfix branch is created from main.
- Once the hotfix branch is finished, it merges into both master and main.

## Style Guide

### Principles

- Keep it simple and reuse as much as possible.
- Code that looks like it was written by one person.
- Write for scalability.

### Structure

![style_guide](/screenshots/style_guide.png)

### General

- We use **BEM** as a code creation methodology.
- File names in plural (**Example**: buttons.scss)
- Classes in singular and lowercase (Example: .gallery\_\_button)
- Name images relative to their block. (Example: hero_background.png)

### Syntax

1. Space after the selector and before {}
2. Spaces for indentation.
3. Space after the :
   1. CSS blocks separated by 2 lines
   2. Avoid nesting abuse. Limit 1 level
   3. Mixins for size, styles, and numerical font values.

### Property Management

Properties and selectors should be sorted as follows:

- Box model properties (display, width, height, margin, etc)
- Positioning (position, left, top, right, etc)
- Typography (text-transform, text-decoration)
- Decoration (background-image, color, etc)
- Variables
- Mixins

### Code Example:

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