---
title: "Sample Page"
permalink: /pagetest/
usemathjax: true
---

# Heading 1
## Heading 2
### Heading 3

Code snippet:

```python
def hat(w):
    w_hat = Matrix([[0,    -w[2], w[1] ],
                    [w[2],   0,  -w[0] ],
                    [-w[1], w[0],   0  ]])
    return w_hat
```

Latex:

$$  \hat{w} = \left[\begin{matrix}0 & - w_{3} & w_{2}\\w_{3} & 0 & - w_{1}\\- w_{2} & w_{1} & 0\end{matrix}\right] $$

### Images

(html)

<img src="\..\assets\images\mark.jpg" alt="mark" width="200"/>

(kramdown)

![its-me-mark](\..\assets\images\mark.jpg){:class="img-responsive"}

(wrap text around image?)

<!--i need to learn this better some time when i'm less zonked. here is some help https://talk.jekyllrb.com/t/inclusion-image-on-left-side-and-text-on-the-right-side-using-markdown-in-jekyll-site/3413/11 -->

![its-a-me-mark](\..\assets\images\mark.jpg){:style="float: left"} text text