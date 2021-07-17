---
layout: "posts"
title: "Whisker Frames!"
collection: whiskerframes
sidebar:
        nav: "wfnav"
author_profile: true
usemathjax: true
---
![banner](\..\assets\images\notbad2.jpg){:class="img-responsive"}
**Whisker Frames** is an independent research project


Code snippet:

```python
def hat(w):
    w_hat = Matrix([[0,    -w[2], w[1] ],
                    [w[2],   0,  -w[0] ],
                    [-w[1], w[0],   0  ]])
    return w_hat
```

Latex:

$$  
\hat{w} = \left[\begin{matrix}0 & - w_{3} & w_{2}\\w_{3} & 0 & - w_{1}\\- w_{2} & w_{1} & 0\end{matrix}\right] $$

### Images

(html)

<img src="\..\assets\images\mark.jpg" alt="mark" width="200"/>

(kramdown)
