# babel-plugin-inline-invariant

## Purpose

Eliminates function call to `invariant` if the condition is met.

Transforms:

```language=javascript
invariant(<cond>, ...)
```

to:

```language=javascript
!<cond> ? invariant(0, ...) : undefined;
```
