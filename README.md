# hugo static site

### Making a static site with hugo
1. Download hugo.exe file 
2. Dowload a theme from gohugo.io
3. Open poweshell in windows
4. Make changes as shown in the below referenced video
5. To run: ./hugo server
6. add the following line to 'config.toml' file
```
canonifyURLs = true
```
7. To create html and css public files: ./hugo -D
8. Reference video: https://www.youtube.com/watch?v=mEZ1Hj5yQ-8&list=LLUBHsYKKuOKb09EZE-AOKIA&index=4&t=1012s

### Making 'mathjax' work in hugo static site

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
  
