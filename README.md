# Hikaru 2 - Sabaki Theme

![hikaru-screenshot](https://user-images.githubusercontent.com/950825/144652487-cf748c64-48a2-4056-bb7a-4556babdd0ab.jpg)

"A crisp SVG theme with an anime feel." - Upsided

Original theme: [Download](https://github.com/upsided/Upsided-Sabaki-Themes).

Removed animation theme: [Download](https://github.com/jdriselvato/Hikaru-2-Sabaki-Theme/raw/main/hikaru2.asar)

# Difference:
- Hikaru theme from [Upsided Sabaki Themes](https://github.com/upsided/Upsided-Sabaki-Themes) but using the default Sabaki 2 placement animation.

# Default Animation

https://user-images.githubusercontent.com/950825/144647878-598f48dd-7a7c-419a-82eb-79eda4f192a4.mov

[Download](https://github.com/jdriselvato/Hikaru-2-Sabaki-Theme/raw/main/hikaru2.asar)

----

# Removing Animations

If you want to remove animations from the other Upsided themes, here's a quick breakdown of how I did it.

Note: asar & npm need to be installed
```
npm install -g asar
```

1. Download the Theme
2. Unpack the theme in terminal with `npx asar extract hikaru.asar ./theme`
3. All the files will be extracted in a folder called `theme`
4. In the `theme` folder edit the `styles.css` file
5. Remove the following lines:

```
/* ANIMATIONS */
/* make the markers wait until stone arrives*/
@keyframes marker-wait {
    from {opacity: 0;}
}

/* move in stones from black or white player */
@keyframes stone-drop-black {
  from { transform: scale(1.0, 1.5) translate(2em,8em); }
  opacity: 0.2;
}

@keyframes stone-drop-white {
  from { 
  transform: scale(1.0,  1.5) translate(-2em, -8em); 
  opacity: 0.2;
  }
}
```

6. Save the file
7. In terminal `asar pack ./theme ./hikaru2.asar`
8. In Sabaki, you can install the theme file under Preferences -> Themes -> Install Theme.
