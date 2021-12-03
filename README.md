# Hikaru 2 - Sabaki Theme

Original theme is credited to Upsided, [found here](https://github.com/upsided/Upsided-Sabaki-Themes).

# Difference:
- Hikaru theme from Upsided-Sabaki-Themes but without the placement animation. 
- This theme uses the default Sabaki 2 placement animation.

# Default Animation

https://user-images.githubusercontent.com/950825/144647878-598f48dd-7a7c-419a-82eb-79eda4f192a4.mov

A crisp SVG theme with an anime feel.

[Download](https://github.com/jdriselvato/Hikaru-2-Sabaki-Theme/raw/main/hikaru2.asar)

----

# Removing Animations

If you want to rmeove animations from the other Upsided themes, here's a quick breakdown of how I did it.

Note: asar & npm need to be installed
```
npm install -g asar
```

1. Download the Theme
2. unpack the theme in terminal with `npx asar extract hikaru.asar ./theme`
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
