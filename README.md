# sass-transition-mixin
SASS mixin for creating dynamic transitions. Uses 0.3s transition-duration if omitted.

Examples:

```
body
    +transition
    +transition()
    +transition(color)
    +transition(color 1s)
    +transition(opacity, width, height)
    +transition(opacity 1s, width, height)
    +transition(opacity, width 1s, height)
    +transition(opacity, width, height 1s)
    +transition(opacity 1s, width 2s, height 3s)
```

Result is:

```
body {
	transition: all 0.3s;
	transition: all 0.3s;
	transition: color 0.3s;
	transition: color 1s;
	transition: opacity 0.3s, width 0.3s, height 0.3s;
	transition: opacity 1s, width 0.3s, height 0.3s;
	transition: opacity 0.3s, width 1s, height 0.3s;
	transition: opacity 0.3s, width 0.3s, height 1s;
	transition: opacity 1s, width 2s, height 3s;
}
```
