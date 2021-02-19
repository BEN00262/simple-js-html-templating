### A stupidly simple addons for manipulating html from javascript without Reactjs
### NOTE: do not use in production!!

### simple documentation
```
<% VARIABLE %>

<% if|for|else|switch {%>
<%}%> end of the javascript block

supports if|for|else|switch in javascript
```

```html
<!DOCTYPE html>
<html>
<head>
	<title>example</title>
</head>
<body>
	<div id="root"></div>

	<script type="text/javascript" src="../dist/demo.js"></script>
	<script type="text/javascript">
		let render = RenderComponent(`
			<% for( let r = 0;r < data.length; r++){%>
				<p><% data[r].name %></p>
				<p><% data[r].age %></p>
			<%}%>
		`,document.getElementById("root"));

		render([
		{
			name:"john",
			age:22
		},
		{
			name:"Kelvin",
			age:23
		},
		{
			name: "Kudush",
			age: 22
		}])

	</script>
</body>
</html>
```

### sample output
![Alt text](examples/output.png?raw=true "Example Output")