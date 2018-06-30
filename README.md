# AJAX nanobar

Fork of **nanobar** to bind with JSF ajax status events.
Basically a clean replacement for the Primefaces `AjaxStatus` widget.

### Load

Load either the full or minified JS file on your JSF page by adding `ajaxnanobar.js`  or `ajaxnanobar.min.js` to your xhtml file

```xml
<h:outputScript library="js" name="ajaxnanobar.min.js"/>
```

Everything else is automatic.


### Move bar

If you want to tinker you can manually resize the bar with `nanobar.go(percentage)`

**arguments**

  * `percentage` `<Number>` : percentage width of nanobar


## Example

```javascript
//move bar
nanobar.go( 30 ); // size bar 30%
nanobar.go( 76 ); // size bar 76%


// size bar 100% and and finish
nanobar.go(100);
```

### Customize bars

Nanobar injects a style tag in your HTML head. Bar divs has class `.bar`, and its containers `.nanobar`, so you can overwrite its values.

Default css:

```css
.nanobar {
  width: 100%;
  height: 4px;
  z-index: 9999;
  top:0
}
.bar {
  width: 0;
  height: 100%;
  transition: height .3s;
  background:#000;
}
```
   
## References

  * [nanobar]()https://github.com/jacoborus/nanobar)
  * [ajax status](https://stackoverflow.com/questions/7880843/show-loading-progress-when-making-jsf-ajax-request)
  * Chapter 13.3.5.2 of the [JSF 2.0 specification](https://jcp.org/aboutJava/communityprocess/final/jsr314/index.html)


© 2016/2018 the authors [jacoborus](https://github.com/jacoborus) and [keybridge](https://github.com/keybridge) - Released under **MIT License**
