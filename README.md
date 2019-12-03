# Lightweight CSS utility-first framework

Inspired by [Bootstrap grid](https://github.com/twbs/bootstrap) and
[Tailwindcss](https://github.com/tailwindcss/tailwindcss).

## Usage Examples


### Variables

A deep map helper function `get()` ([source](https://itnext.io/advanced-use-of-sass-maps-bd5a47ca0d1a))
allows us to retrieve nested map keys easily:
```scss
$font: (
    'heading': (
        ...
        'size': (
            'h1-display': 96px,
            ...
        ),
    ),

);

.display-h1 {
    font-size: get('heading.size.h1-display', $font);
}
```


### Responsive Classes

To add a utility but only have it take effect at a certain breakpoint, all you
need to do is prefix the utility with the breakpoint name, followed by
the : character:
```html
<div class="flex flex-wrap justify-center">
    <div class="w-full md:w-6/12 lg:w-4/12"></div>
    <div class="w-full md:w-6/12 lg:w-4/12"></div>
</div>
```
**This does not work for every utility class in the framework — only the most relevant ones.**
The classes are designed for a mobile first breakpoint system, similar to
Bootstrap, Foundation, Tailwind.


### Included Components

Images with ratios:
```html
<figure class="image image-1x1 lg:image-16x9">
    <img src="..." alt="...">
</figure>
```

Buttons:
```html
<button type="button" class="button button-icon-left button-primary">
    <i class="fa fa-pencil"></i>
    Iconed
</button>

<button type="button" class="button button-primary button-outlined">
    Outlined
</button>
```


### Typography

Basic text utilities:
```html
<article>
    <header>
        <h3 class="black font-bold">...</h3>
        <p class="text-black font-semibold uppercase italic">...</p>
    </header>

    <p>...</p>

    <footer class="font-xs border-t">
        ...
    </footer>
</article>
```
