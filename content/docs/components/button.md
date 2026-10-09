# Button

A customizable button component.

## Basic Usage

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">Button</button>
<a href="#" class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">Link Button</a>
{{< /component-preview >}}

```html
<c-button>Button</c-button>
<c-button href="#">Link Button</c-button>
```

> [!NOTE]
> When `href` is set, the component renders an `<a>` instead of a `<button>`.

## Variants

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">Default</button>
<button class="c-button" data-variant="odyssey" data-size="md" data-focus-outline="true" data-pill="false">Odyssey</button>
<button class="c-button" data-variant="light" data-size="md" data-focus-outline="true" data-pill="false">Light</button>
<button class="c-button" data-variant="dark" data-size="md" data-focus-outline="true" data-pill="false">Dark</button>
<button class="c-button text-gray-950 dark:text-gray-50" data-variant="text" data-size="md" data-focus-outline="true" data-pill="false">Text</button>
{{< /component-preview >}}

```html
<c-button>Default</c-button>
<c-button variant="odyssey">Odyssey</c-button>
<c-button variant="dark">Dark</c-button>
<c-button variant="light">Light</c-button>
<c-button variant="text" class="text-gray-950 dark:text-gray-50">Text</c-button>
```

> [!NOTE]
> The `text` variant has no fill, border, fixed height or horizontal padding, and the text colour is inherited.

### Custom variant

If you need a style the built-in variants don't cover, use `variant="custom"` and pass your own Tailwind CSS classes. The `custom` variant applies no variant styles (colours), so you have full control over the look. For example:

{{< component-preview >}}
<button class="c-button bg-fuchsia-700 text-white hover:bg-fuchsia-800 focus-visible:outline-fuchsia-600" data-variant="custom" data-size="sm" data-focus-outline="true" data-pill="false">Fuchsia</button>
<button class="c-button bg-linear-to-r from-[#4939d5] to-[#9c41d9] text-white" data-variant="custom" data-size="md" data-focus-outline="true" data-pill="false">Gradient</button>
{{< /component-preview >}}

```html {hl_lines=["2-4","9-10"]}
<c-button
  variant="custom"
  size="sm"
  class="bg-fuchsia-700 text-white hover:bg-fuchsia-800 focus-visible:outline-fuchsia-600 ..."
>
  Fuchsia
</c-button>
<c-button
  variant="custom"
  class="bg-linear-to-r from-[#4939d5] to-[#9c41d9] text-white ..."
>
  Gradient
</c-button>
```

## Sizes

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="xs" data-focus-outline="true" data-pill="false">Extra Small</button>
<button class="c-button" data-variant="default" data-size="sm" data-focus-outline="true" data-pill="false">Small</button>
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">Default</button>
<button class="c-button" data-variant="default" data-size="lg" data-focus-outline="true" data-pill="false">Large</button>
<button class="c-button" data-variant="default" data-size="xl" data-focus-outline="true" data-pill="false">Extra Large</button>
{{< /component-preview >}}

```html
<c-button size="xs">Extra Small</c-button>
<c-button size="sm">Small</c-button>
<c-button>Default</c-button>
<c-button size="lg">Large</c-button>
<c-button size="xl">Extra Large</c-button>
```

## Focus Outline

By default, buttons show a dashed outline, offset from the button, when focused with the keyboard. Set `focus_outline` to `False` to remove it.

> [!NOTE]
> Press <kbd>Tab</kbd> to move focus to each button and compare the two.

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">With Focus Outline</button>
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="false" data-pill="false">No Focus Outline</button>
{{< /component-preview >}}

```html
<c-button>With Focus Outline</c-button>
<c-button :focus_outline="False">No Focus Outline</c-button>
```

## Pill

Set `pill` to `True` for fully rounded ends.

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false">Default</button>
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="true">Pill-Shaped Button</button>
{{< /component-preview >}}

```html
<c-button>Default</c-button>
<c-button pill>Pill-Shaped Button</c-button>
```

## Disabled

Set `disabled` to `True` to disable a button.

{{< component-preview >}}
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false" disabled>Disabled</button>

{{< /component-preview >}}

```html
<c-button disabled>Disabled</c-button>
```

> [!NOTE]
> The `disabled` prop has no effect on link buttons (when `href` is set).

## Icons

Add an icon through the `icon` named slot (`<c-slot name="icon">...</c-slot>`). The icon will be rendered before the button label.

{{< component-preview >}}
<button class="c-button aspect-square px-0" data-variant="light" data-size="md" data-focus-outline="true" data-pill="true" aria-label="Next"><svg class="size-6" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M9 6l6 6l-6 6"></path></svg></button>
<button class="c-button" data-variant="default" data-size="md" data-focus-outline="true" data-pill="false"><svg class="size-6" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M12 5l0 14"></path><path d="M5 12l14 0"></path></svg>New Project</button>
{{< /component-preview >}}

```html {hl_lines=["2-4","7-9"]}
<c-button variant="light" pill class="aspect-square px-0" aria-label="Next">
  <c-slot name="icon">
    <c-tablericon.chevron-right class="size-6" />
  </c-slot>
</c-button>
<c-button>
  <c-slot name="icon">
    <c-tablericon.plus class="size-6" />
  </c-slot>
  New Project
</c-button>
```

> [!NOTE]
> Icon-only buttons should have an `aria-label` so screen readers can announce them.

## API Reference

### Props

| Prop            | Type | Default | Options                                  | Description                                                                                     |
| --------------- | ---- | ------- | ---------------------------------------- | ----------------------------------------------------------------------------------------------- |
| `href`          | str  | -       | -                                        | When set, renders an `<a>` instead of a `<button>`.                                             |
| `type`          | str  | button  | `button` `submit` `reset`                | The `type` attribute of the `<button>`. Ignored when `href` is set.                             |
| `variant`       | str  | default | `default` `dark` `light` `text` `custom` | The visual style variant of the button. 'text' variant renders a link-like button with no fill. |
| `size`          | str  | md      | `xs` `sm` `md` `lg` `xl`                 | The size of the button.                                                                         |
| `focus_outline` | bool | True    | `True` `False`                           | Show a dashed outline when focused with the keyboard.                                           |
| `pill`          | bool | False   | `True` `False`                           | Use fully rounded ends instead of the default radius.                                           |
| `class`         | str  | -       | -                                        | Extra classes. Utility classes override the component's styles.                                 |
| `disabled`      | bool | False   | `True` `False`                           | Disable the button. Ignored when `href` is set.                                                 |     |

### Additional attributes

You can add any standard HTML attribute, such as `target` or `rel`, and it will be passed through to the rendered element.

```html
<c-button href="https://example.org" target="_blank" rel="noopener noreferrer">
  External Site
</c-button>

<!-- html output
<a href="https://example.org" target="_blank" rel="noopener noreferrer" class="c-button" data-variant="default" data-size="md" data-pill="false" data-focus-outline="true">External Site</a>
-->
```
