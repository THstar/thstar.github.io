---
title: "Use Latex Syntax"
last_modified_at: 2020-04-29
categories:
  - Blog
tags:
  - Github
  - Blog
  - Latex
---

## Setting
* To use Latex syntax using Markdown on the Github blog, you need to configure the following. [Check](https://www.janmeppe.com/blog/How-to-add-mathjax-to-minimal-mistakes/)
* Create a file with the following contents in the address below.
> _includes/head/custom.html

```html
<script type="text/javascript" async
	src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.5/latest.js?config=TeX-MML-AM_CHTML">
</script>

<script type="text/x-mathjax-config">
	MathJax.Hub.Config({
		extensions: ["tex2jax.js"],
		jax: ["input/TeX", "output/HTML-CSS"],
		tex2jax: {
			inlineMath: [ ['$','$'], ["\\(","\\)"] ],
			displayMath: [ ['$$','$$'], ["\\[","\\]"] ],
			processEscapes: true
		},
		"HTML-CSS": { availableFonts: ["TeX"] }
	});
</script>
```

## How to use Latex syntax

* Used inline:

> ex) 
> ```
> set parameter $\alpha$ as 0.05
> ``` 
 
result:  set parameter $\alpha$ as 0.05

* Equation:

> ex)
> ```
> $$
> \alpha + \beta = \gamma
> $$
> ```

result: 
$$
\alpha + \beta = \gamma
$$
