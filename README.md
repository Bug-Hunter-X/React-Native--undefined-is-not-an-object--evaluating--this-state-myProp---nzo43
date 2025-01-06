# React Native: undefined is not an object (evaluating 'this.state.myProp')

This repository demonstrates a common React Native error: attempting to access component state or props before the component has fully mounted.  The bug showcases the error, and the solution provides a corrected approach ensuring safe access to state and props.

## Bug
Attempting to access `this.state` or `this.props` within the constructor or immediately after setting state in `componentDidMount` can lead to unexpected behavior.  This is because React's lifecycle ensures that state and props are available only *after* mounting.

## Solution
The solution involves accessing `this.state` and `this.props` only after the component has mounted. This is typically done within the `componentDidMount` lifecycle method or through the use of the `useEffect` hook (for functional components).