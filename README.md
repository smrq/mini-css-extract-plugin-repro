* Run `npm start`
* Check `dist/styles.chunk.css`

# Expected

```
@import url(https://fonts.googleapis.com/css?family=Open+Sans:400italic,600italic,400,600,300);
.z {}

.font {}

h1::before { content: "Broken!"; color: red; }

h1::before { content: "OK!"; color: green; }

.c1 {}

.c2 {}

.c3 {}

.c4 {}

.c5 {}

.index {}
```

# Actual

```
@import url(https://fonts.googleapis.com/css?family=Open+Sans:400italic,600italic,400,600,300);
.c1 {}

.index {}

.z {}

.font {}

h1::before { content: "OK!"; color: green; }

.c5 {}

.c3 {}

h1::before { content: "Broken!"; color: red; }

.c4 {}

.c2 {}
```
