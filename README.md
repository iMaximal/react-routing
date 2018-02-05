For study

Examples. How to use axios and routes.


React router makes it easy to get access to the search string: props.location.search .
 
 But that will only give you something like ?start=5 
 
 You probably want to get the key-value pair, without the ?  and the = . Here's a snippet which allows you to easily extract that information:
 
 `props.location.search`
 `props.location.hash`
 
 ````
 componentDidMount() {
     const query = new URLSearchParams(this.props.location.search);
     for (let param of query.entries()) {
         console.log(param); // yields ['start', '5']
     }
 }
 ````

URLSearchParams  is a built-in object, shipping with vanilla JavaScript.
