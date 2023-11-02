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
