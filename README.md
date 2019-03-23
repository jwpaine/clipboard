
### reducer
```javascript
	...
	return {
			...state,
			place: {'place' : action.place.place, 'categories': action.place.categories["Items"]}
		}
	...
```

### component
```javascript
	...
	{console.log(this.props.place.categories)}
	...
```
which shows the following in console:

```console
(2) [{...}, {...}]
	>0: {key: "value"}
	>1: {key: "value"}
		length: 2
	>__proto__: Array(0)
```
As expected. However, if I call:

```javascript
	...
	{console.log(this.props.place.categories[0])}
	...
```

I get a nasty error: TypeError: Cannot read property '0' of undefined
