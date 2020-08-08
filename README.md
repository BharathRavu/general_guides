# General Guides

## Making 'mathjax' work in hugo static site

1. Create a file in hugo theme directory layouts/partials/mathjax_support.html as the following
```
<script>
MathJax = {
  tex: {
    inlineMath: [['$', '$'], ['\\(', '\\)']],
    tags: 'ams'
  },
  svg: {
    fontCache: 'global'
  }
};
</script>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-svg.js">
</script>
```
2. Add the following line to the 'site-header.html' file at the bottom before <header>

```
  {{ partial "mathjax_support.html" . }}
```
References:
```
http://docs.mathjax.org/en/latest/web/configuration.html#configuration
https://geoffruddock.com/math-typesetting-in-hugo/
http://docs.mathjax.org/en/latest/input/tex/eqnumbers.html
```
  
