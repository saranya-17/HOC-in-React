# HOC-in-React
Higher Order Component concept in React
Higher order component is an advanced concept of React. It’s not part of the React Api
	Components transform props from one to another component whereas, Higher order component transform a component into another component
	HOC is a function that takes a new component and returns a component
	const EnhancedComponent = higherOrderComponent(WrappedComponent);

Don’t use HOC inside render() method
After each rendering React diffing algorithm Reconciliation will check whether it should update the existing subtree or throw it away and mount a new one. If the previous the component return from the render method is identical to the component of previous render, then React will update the subtree by diffing with the new render component. If they are not equal the previous subtree will unmounts completely.
If the HOC implement in render method a new version of enhanced component will create in every render, which leads to unmounts/remount the sub tree always. Remounting will cause lose in state of the component and child components.
