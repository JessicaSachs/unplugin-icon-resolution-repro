Reproduction for icon reloading and resolution.

### SVG icon is cached and doesn't update after being modified
**Have to restart server to get icon changes to update**

1. `yarn dev`
2. See the icon render correctly

![Screen Shot 2021-09-23 at 11 21 34 PM](https://user-images.githubusercontent.com/2801156/134613231-9c823d82-7b32-4b9c-820d-c7681af8c69a.png)

4. Open `src/icons/code-editor_x24.svg`
5. Change the fill to be green

```html
<svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
<path d="M21 6C21 4.89543 20.1046 4 19 4H5C3.89543 4 3 4.89543 3 6V8H21V6Z" fill="green" class="icon-light"/>
<path fill-rule="evenodd" clip-rule="evenodd" d="M21 6C21 4.89543 20.1046 4 19 4H5C3.89543 4 3 4.89543 3 6V8H21V6Z" fill="green" class="icon-light"/>
<path d="M3 8V18C3 19.1046 3.89543 20 5 20H19C20.1046 20 21 19.1046 21 18V8M3 8V6C3 4.89543 3.89543 4 5 4H19C20.1046 4 21 4.89543 21 6V8M3 8H21M14 12L16 14L14 16M10 12L8 13.9286L10 15.8571" stroke="orange" class="icon-dark" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
</svg>
```

6. Hard refresh the app.
7. The only way the icons update is by killing and restarting the server.
