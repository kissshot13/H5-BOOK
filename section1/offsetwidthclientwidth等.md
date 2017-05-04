###offsetwidth/clientwidth

- clientWidth是对象看到的宽度（不含边线,即border）
- scrollWidth是对象实际内容的宽度（若无padding，那就是边框之间距离，如有padding，就是左padding和右padding之间距离）
- offsetWidth是指对象自身的宽度，整型，单位像素（含边线，如滚动条的占用的宽，值会随着内容的输入而不断改变）
- clientWidth = width + padding
- offsetWidth = width + padding + border