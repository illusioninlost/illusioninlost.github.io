---
layout: post
title:      "React Lifecycle Events"
date:       2018-11-10 18:05:28 +0000
permalink:  react_lifecycle_events
---



React creates components as classes or functions. One of the most unique aspects in React is the idea of lifecycle events in the making of such components. First off, a component looks like this:

```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

One thing to note is you must include a subclass called render() in a class component.


According to the React documentation on lifecycle events, there are three phases in a component lifecycle.

The mounting phase, the first phase, consists of these items:

* 	constructor()
* 	static getDerivedStateFromProps()
* 	render()
* 	componentDidMount()

componentWillMount() is also part of this phase but has been transitioning to be out of use. In this phrase, components are initialized.

The updating phase is the second phase:

* 	static getDerivedStateFromProps()
* 	shouldComponentUpdate()
* 	render()
* 	getSnapshotBeforeUpdate()
* 	componentDidUpdate()

componentWillUpdate() and componentWillReceiveProps() are also part of this phase but has been transitioning to be out of use. In this phrase, components are set up by conditions and therefore, set a change in State or Props. The use of these methods triggers the component re-render.

The unmounting phase, the last of three phases, consists of:

*	componentWillUnmount()

In this final phase, components should be removed from the DOM (Document Object Model). As you can see, it is one of the simpler phases to be recognized.



**constructor()**

>  If you don’t initialize state and you don’t bind methods, you don’t need to implement a constructor for your React component.
 
Constructor are useful for creating state and binding event handler. super(props) can be used in the constructor to define Props, or otherwise Props becomes undefined. The constructor is where you use this.state; for all other instances, you use this.setState().


**componentDidMount()**

In this function and part of the mounting phase, data from a remote API can be placed to setState(). As an added bonus, this triggers a second re-render.


**componentDidUpdate(prevProps, prevState, snapshot)**

Notice in this method above, you have some arguments, which are prevProps(the properties in the previous state),prevState,snapshot. And as an example, see below for details

```
 componentDidUpdate(prevProps) {

   // Typical usage (don't forget to compare props):
   if (this.props.userID !== prevProps.userID) {
     this.fetchData(this.props.userID);
   }
 }
```

The example has a method called fetchData(network request),wrapped inside a condition; it uses prevProps as an argument.
Using componentDidUpdate, you may call this.setState() as long as you set a condition like in the example above.

**componentWillUnmount()**

The method performs cleanup duties such as invalidating timers, removing subscriptions, and removing graphics, and  etc. The use of setState() in this method is prohibited and should not be called(see above for use of setState()).

Other rarely used lifecycle methods include shouldComponentUpdate(nextProps, nextState), static getDerivedStateFromProps(props, state), getSnapshotBeforeUpdate(prevProps, prevState),componentDidCatch(). As you can see, React is continually developing and produces methods that later cause programmers to ease out of use. Errors do occur and JavaScript displays errors in the rendering and lifecycle methods. So now you may have gained some knowledge on lifecycle methods. Happy coding.

