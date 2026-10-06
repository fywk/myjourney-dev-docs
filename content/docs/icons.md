# Icons

Icons in this project are provided by [cotton-icons](https://github.com/wrabit/cotton-icons/tree/main), a package that ships popular icon packs as [Django Cotton](https://django-cotton.com) components. Instead of pasting inline SVG into templates, you write an icon as an HTML-style tag, for example `<c-heroicon.home />`.

Three packs are available, all with the same syntax:

- **Heroicons**
- **Tabler Icons**
- **Lucide Icons**

## Basic Usage

### Heroicons

```html
<c-heroicon.chevron-down class="size-5" />
<c-heroicon.chevron-down variant="solid" class="size-5" />
<c-heroicon.chevron-down variant="mini" class="size-5" />
```

### Tabler

```html
<c-tablericon.graph class="size-6" />
<c-tablericon.graph variant="filled" class="size-6" />
```

### Lucide

```html
<c-lucideicon.arrow-down class="size-5" />
<c-lucideicon.search class="size-5" stroke-width="3" />
```

## Sizing

Always set an explicit size class on every icon (for example `class="size-5"`). Icons do not come with a default size, so without one they may not render as expected.

```html
<!-- Don't: no size -->
<c-tablericon.chevron-down />

<!-- Do: explicit size -->
<c-tablericon.chevron-down class="size-6" />
```

Pick a size that fits the context (for example `size-4` inline with text, `size-5` in buttons and navigation) and use it consistently.

## API Reference

### Props

| Prop                | Description                                                                | Applies to         |
| ------------------- | -------------------------------------------------------------------------- | ------------------ |
| `variant`           | Selects the icon style. See [Variants](#variants).                         | Heroicons, Tabler  |
| `class`             | CSS classes for the `<svg>`. Use it to set the size (required) and colour. | All                |
| `stroke-width`      | Thickness of the icon's stroke.                                            | Stroke-based icons |
| `stroke-linecap`    | Shape of stroke ends.                                                      | Stroke-based icons |
| `stroke-linejoin`   | Shape of stroke corners.                                                   | Stroke-based icons |
| any other attribute | Passed through to the `<svg>` tag (`id`, `style`, `aria-*`, `data-*`).     | All                |

### Variants

| Library   | Variants                            | Default   |
| --------- | ----------------------------------- | --------- |
| Heroicons | `outline`, `solid`, `mini`, `micro` | `outline` |
| Tabler    | `outline`, `filled`                 | `outline` |
| Lucide    | -                                   | -         |
