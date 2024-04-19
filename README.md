# Fascinated-sassafras
ballstormmm

![buh](https://github.com/nicolasbaez/Fascinated-sassafras/blob/main/xp033.gif)
```javascript
q = 250;
w = [];
t = [];
setup = (_) => createCanvas((h = 500), h, WEBGL);
e = (i) => {
  if (!t[i] || t[i] > 18) {
    e[i] = random(h);
    w[i] = random(16, 32);
    t[i] = 0;
  }
  push();
  translate(e[i] - q, h - (h * sin(t[i])) / t[i] - q);
  fill("#F60");
  sphere(w[i]);
  pop();
  t[i] += w[i] / q;
};
draw = (_) => {
  clear();
  for (i = 0; i < q; i++) e(i);
};
keyPressed = (_) => {
  if (key === "s") {
    saveGif("xp033.gif", 400, { delay: 0, units: "frames" });
  }
};
