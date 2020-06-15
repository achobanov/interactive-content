# Media Feature Rules

[slide]
# Media Feature Rules

After specifying the type, you can then target a media feature with a **rule**.

## Width and Height

`width` and `height` – we can apply CSS if the viewport is above or below a certain **width/height**, using **width/height**.

**Example:**
```html
@media screen and (width: 500px) {
    body {
        color: red;
  }
}
```

## Min-width and Min-height

We can apply CSS if the viewport is with an exact width – using `min-width`, `max-width`.

**Example:**
```html
@media screen and (max-width: 400px) {
    body {
        color: blue;
  }
}
```

## Orientation

`orientation` property allows us to test for **portrait** or **landscape** mode.
To change the body text color if the device is in landscape orientation:

**Example:**
```html
@media (orientation: landscape) {
    body {
        color: red;
  }
}
```

## Hover

`hover` is used to querying the user’s ability to **hover** over elements on the page with the primary pointing device:

* `hover: hover;` - hover over elements with ease;
* `hover: none;` - can’t hover over elements.

**Example:**
```html
@media (hover: hover) {
    /* ... *
}
```

## Pointer

`pointer` is used to query the presence and accuracy of a **pointing** device such as a mouse.

If the primary input mechanism of the device includes:
* a pointing device of limited accuracy, we use `coarse`;
* an accurate pointing device, we use `fine`;
* **not include** a pointing device, we use `none`;

**Example:**
```html
/* define styles based on input device pointer accuracy */
@media(pointer: course) {
   /* ... *
}
```

## Target specific existing device

**Example:**
```html
/* smartphones, touchscreens */
@media (hover: none) and (pointer: coarse) {
    /* ... */
}

/* stylus-based screens */
@media (hover: none) and (pointer: fine) {
    /* ... */
}

/* mouse, touch pad */
@media (hover: hover) and (pointer: fine) {
    /* ... */
}
```

[/slide]