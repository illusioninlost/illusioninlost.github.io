---
layout: post
title:      "State vs Props"
date:       2018-10-30 20:06:16 +0000
permalink:  state_vs_props
---

**I**n react, each component has State and Props. Props is short for "properties" which the idea becomes obvious. Props contain data that directly relate to the component itself. State also contains data but that data is classified and handled differently.
For general use, in a parent component to child component communication, coders pass the parent's State to the child's Props. Props are immutable, typically used when the data is passed down from parent to child, and have better performance. On the other hand, State is mutable, has worse performance, can not be accessed from a child component. One thing to note is that since the props are immutable, the component becomes more reusable.

**I**f someone has three fruits: a banana, an apple, and an orange. the parent component is a human object with an array of fruits and the number of fruits as State and the name of the person as Props. When the array of fruits and the number of fruits are passed down to a child component, fruit component. The fruit component  doesn't have a State but has Props which contain have the name of fruits. If that someone gets an extra watermelon, the fruit component doesn't update to the parent from the fruit component's Props. The parent's State changes with the additional fruit and passes the fruit count and fruit name from State to Props. The parents' State updates the child's Props.

**C**omponents  have a built-in method called setState().
```
class Counter extends Component{
  
  constructor(props){
    super(props);
    this.state = {counter: 0}
    this.increment = this.increment.bind(this);
  }
  increment(){
    this.setState({counter: this.state.counter + 1})
  }
render(){
    return(
      <button onClick={this.increment}>Like</button>
      <p>{this.state.counter}</p>
  )
}
```

**T**his example was taken from a blog but the React DOCS have a similar example. This example serves the idea of using State because State is mutable. The code has a Counter class and creates an object with a state.counter initialized to zero. An event function is placed in the return of the rendered component that acts a button and when clicked, it calls the object itself and since it is that function is bound to the object itself, increment function is called. This changes the State from 0 to 1, 1 to 2, and etc. React will rerender and thus a change was made with just a click of a button.


```
const mapStateToProps = state => {

    return { myTools: state.tools.tools };
}
```

**U**sing Redux in an application, mapStateToProps takes State data from the store and creates your component’s Props. In my tool-rental app, this takes the State from tools.tools (the store wrapper, similar to a parent) to the component(child)’s Props called myTools. As a result, I can find the objects in the array by calling this.props.myTools

**I**n conclusion, State and Props functionally work and almost identify similarly but they are kept as separate entities in React.

