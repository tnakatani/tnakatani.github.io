# Adjusting CSS when using jupyter nb_convert

Problem: I couldn't figure out how to style the width of images when printing my jupyter notebooks.

Solution: The CSS file is stored under the nbconvert package.  I use anaconda, so the package was found under the path

```
/usr/local/Caskroom/miniconda/base/envs/my_env/lib/python3.8/site-packages/nbconvert/resources/style.min.css
```


Under the css file, there is a section specifically for print output.  It turns out that it had explicitly set the width and marked it as `!important`.

```
img {
max-width: 100% !important;
}
```

You can either edit the inline CSS in the html output, or edit it in the css file path above.
