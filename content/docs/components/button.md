# Button

A customizable button component.

## Basic Usage

{{< component-preview >}}
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] outline-dashed transition-[background-color,border-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Button</button>
  <a href="#" class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] outline-dashed transition-[background-color,border-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Link Button</a>
{{< /component-preview >}}

```html
<c-button>Button</c-button>
<c-button href="#">Link Button</c-button>
```

> [!NOTE]
> When `href` is set, the component renders an `<a>` instead of a `<button>`.

## Variants

{{< component-preview >}}
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] border border-gray-200 bg-white px-4 text-base font-semibold text-gray-900 outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:border-gray-400 hover:bg-gray-50 focus-visible:border-gray-400 focus-visible:outline-3 active:scale-95">White</button>
  <button class="flex h-auto items-center justify-center gap-x-[.5em] rounded-none px-0 text-base font-semibold text-gray-50 outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:underline focus-visible:outline-3 focus-visible:outline-current active:scale-none">Text</button>
{{< /component-preview >}}

```html
<c-button>Default</c-button>
<c-button variant="white">White</c-button>
<c-button variant="text" class="text-gray-50">Text</c-button>
```

If you need a style the built-in variants don't cover, use `variant="custom"` and pass your own Tailwind CSS classes. The `custom` variant applies no variant styles (colours), so you have full control over the look. For example:

{{< component-preview >}}
  <button class="flex h-8 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-fuchsia-700 px-3.5 text-sm font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-fuchsia-800 focus-visible:outline-3 focus-visible:outline-fuchsia-600 active:scale-95">Fuchsia</button>
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-linear-to-r from-[#4939d5] to-[#9c41d9] px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] focus-visible:outline-3 active:scale-95">Gradient</button>
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
  <button class="flex h-6 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-3 text-xs font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Extra Small</button>
  <button class="flex h-8 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-3.5 text-sm font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Small</button>
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-12 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-5 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Large</button>
  <button class="flex h-14 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-6 text-lg font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Extra Large</button>
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
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">With Focus Outline</button>
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white transition-[background-color,border-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus:outline-hidden focus-visible:outline-rose-600 active:scale-95">No Focus Outline</button>
{{< /component-preview >}}

```html
<c-button>With Focus Outline</c-button>
<c-button :focus_outline="False">No Focus Outline</c-button>
```

## Pill

Set `pill` to `True` for fully rounded ends.

{{< component-preview >}}
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-[1.5ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-10 items-center justify-center gap-x-[.5em] rounded-full bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,border-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Pill-Shaped Button</button>
{{< /component-preview >}}

```html
<c-button>Default</c-button>
<c-button pill>Pill-Shaped Button</c-button>
```

## API Reference

### Props

| Prop            | Type | Default | Options                           | Description                                                                                     |
| --------------- | ---- | ------- | --------------------------------- | ----------------------------------------------------------------------------------------------- |
| `href`          | str  | -       | -                                 | When set, renders an `<a>` instead of a `<button>`.                                             |
| `type`          | str  | button  | `button` `submit` `reset`         | The `type` attribute of the `<button>`. Ignored when `href` is set.                             |
| `variant`       | str  | default | `default` `white` `text` `custom` | The visual style variant of the button. 'text' variant renders a link-like button with no fill. |
| `size`          | str  | md      | `xs` `sm` `md` `lg` `xl`          | The size of the button.                                                                         |
| `focus_outline` | bool | True    | `True` `False`                    | Show a dashed outline when focused with the keyboard.                                           |
| `pill`          | bool | False   | `True` `False`                    | Use fully rounded ends instead of the default radius.                                           |
| `class`         | str  | -       | -                                 | Extra classes, merged with the defaults.                                                        |

You can add any standard HTML attribute, such as `target` or `rel`, and it will be passed through to the rendered element.

```html
<c-button href="https://example.org" target="_blank" rel="noopener noreferrer">
  External Site
</c-button>

<!-- html output
<a href="https://example.org" target="_blank" rel="noopener noreferrer">External Site</a>
-->
```
