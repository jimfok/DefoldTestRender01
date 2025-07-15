# Defold Draw Primitives Sandbox

This sandbox project began as the standard Defold mobile template.
All repository changes are tracked in `codexlog.md`.

- move default.render to custom.render > it works
- render script exposes `draw_line` and `draw_text` messages. Example:

```lua
function update(self, dt)
    msg.post("@render:", "draw_line", {
        start = vmath.vector3(0, 0, 0),
        ["end"] = vmath.vector3(100, 100, 0),
        color = vmath.vector4(1, 0, 0, 1)
    })
end
```
