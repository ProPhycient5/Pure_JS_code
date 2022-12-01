#### - Below code is meant for creating basic slider-type component where one change(or swipe in real slider component) smoothly. 
#### - It demonstrates how we can change the slide(here it is simple `<div>`) from the extreme end(i.e. first or last slide).

```
<!DOCTYPE html>
<html>
<head>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<title>slider-type-co</title>
</head>
<body>

	<div style="width: 100%;">
		<h1>Slider-type-component</h1>
		<div
		id="parent"
		style="display: flex; flexDirection: row; justifyContent: space-between; marginBottom: 20px;">
		<div id="child-1">child-1</div>
		<div id="child-2">child-2</div>
		<div id="child-3">child-3</div>
		<div id="child-4">child-4</div>
	</div>
	<button onclick="bringToLast()">Bring last item to 1st</button>
	<button onclick="bringToFirst()"}>Bring 1st item to last</button>
</div>
<script type="text/javascript">
	const parent = document.getElementById("parent");
	console.log("parent :", parent);
	const bringToFirst = () => {
		let firstItem = parent?.firstElementChild;
		parent.append(firstItem);
	};

	const bringToLast = () => {
		let lastItem = parent?.lastElementChild;
		parent.prepend(lastItem);
	};
</script>

</body>
</html>
```
