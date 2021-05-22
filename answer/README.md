```py
img = Image.new("L", (256, 256), 255)
draw = ImageDraw.Draw(img)
cx = 128
cy = 128
r = 96
draw.ellipse((cx - r, cy - r, cx + r, cy + r))
N = 3
s = 2 * pi / N
for i in range(N):
    s1 = s*i + 0.5 * pi
    s2 = s1 + s
    x1 = r * cos(s1) + cx
    y1 = r * sin(s1) + cy
    x2 = r * cos(s2) + cx
    y2 = r * sin(s2) + cy
    draw.line((x1, y1, x2, y2))
    s1 = s*(i+0.5) + 0.5 * pi
    s2 = s1 + s
    x1 = r * cos(s1) + cx
    y1 = r * sin(s1) + cy
    x2 = r * cos(s2) + cx
    y2 = r * sin(s2) + cy
    draw.line((x1, y1, x2, y2))
```
