# Vue Animation Notes
- Wrap the vue component with the `<transition>` component tag
```html
<transition name="banana">
  <p>the element to be animated</p>
</transition>
```

- CSS transition classes
Using the transition name, you can prefix the CSS classes using that name:
```css
.banana-enter {}
.banana-enter-active {}
.banana-leave {}
.banana-leave-active {}
```

- Animate onload
Use the `appear` attribute in the transition element to trigger the animation on load
```html
<transition name="banana" appear>
  <p>the element to be animated</p>
</transition>
```

- Overwriting the default transition CSS classes
```html
<transition
  enter-class=""
  enter-active-class="potato bounce"
  leave-class=""
  leave-active-class="potato shake"
>
  <p>the element to be animated</p>
</transition>
```
Note: if you don't use the attribute, don't leave it empty. Remove them
```html
<transition
  enter-active-class="potato bounce"
  leave-active-class="potato shake"
>
  <p>the element to be animated</p>
</transition>
```
