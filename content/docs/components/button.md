# Button

A customizable button component.

## Basic Usage

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] outline-dashed transition-[background-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Button</button>
  <a href="#" class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] outline-dashed transition-[background-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Link Button</a>
</div>

```html
<c-button>Button</c-button>
<c-button href="#">Link Button</c-button>
```

> [!NOTE]
> When `href` is set, the component renders an `<a>` instead of a `<button>`.

## Variants

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-fit items-center justify-center rounded-none px-0 text-base font-semibold outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:underline focus-visible:outline-3 active:scale-none">Text</button>
</div>

```html
<c-button variant="primary">Default</c-button>
<c-button variant="text">Text</c-button>
```

You can customize any variant's default styles by passing Tailwind CSS classes. For example, to change the `background-color`:

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-linear-to-r from-[#4939d5] to-[#9c41d9] px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Customized Button</button>
</div>


```html
<c-button class="bg-linear-to-r from-[#4939d5] to-[#9c41d9] ...">Customized Button</c-button>
```

## Sizes

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-6 items-center justify-center rounded-[1.2ch] bg-rose-700 px-3 text-xs font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Small</button>
  <button class="flex h-8 items-center justify-center rounded-[1.2ch] bg-rose-700 px-3.5 text-sm font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Medium</button>
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-12 items-center justify-center rounded-[1.2ch] bg-rose-700 px-5 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Extra Large</button>
</div>

```html
<c-button size="sm">Small</c-button>
<c-button size="md">Medium</c-button>
<c-button>Default</c-button>
<c-button size="xl">Extra Large</c-button>
```

## Focus Outline

By default, buttons show a dashed outline, offset from the button, when focused with the keyboard. Set `focus_outline` to `False` to remove it.

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default: With Focus Outline</button>
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white transition-[background-color,scale] duration-300 [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus:outline-hidden focus-visible:outline-rose-600 active:scale-95">No Focus Outline</button>
</div>

```html
<c-button>Default: With Focus Outline</c-button>
<c-button :focus_outline="False">No Focus Outline</c-button>
```

## Pill

Set `pill` to `True` for fully rounded ends.

<div class="preview not-prose flex items-center justify-center gap-4 border border-b-0 border-zinc-700 p-8">
  <button class="flex h-10 items-center justify-center rounded-[1.2ch] bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Default</button>
  <button class="flex h-10 items-center justify-center rounded-full bg-rose-700 px-4 text-base font-semibold text-white outline-0 outline-offset-[.25em] transition-[background-color,scale] duration-300 outline-dashed [text-box:trim-both_cap_alphabetic] hover:bg-rose-800 focus-visible:outline-3 focus-visible:outline-rose-600 active:scale-95">Pill-Shaped Button</button>
</div>

```html
<c-button>Default</c-button>
<c-button pill>Pill-Shaped Button</c-button>
```

## API Reference

### Props

| Prop            | Type | Default | Options                   | Description                                                                                     |
| --------------- | ---- | ------- | ------------------------- | ----------------------------------------------------------------------------------------------- |
| `href`          | str  | -       | -                         | When set, renders an `<a>` instead of a `<button>`.                                             |
| `type`          | str  | button  | `button` `submit` `reset` | The `type` attribute of the `<button>`. Ignored when `href` is set.                             |
| `variant`       | str  | primary | `primary` `text`          | The visual style variant of the button. 'text' variant renders a link-like button with no fill. |
| `size`          | str  | lg      | `sm` `md` `lg` `xl`       | The size of the button.                                                                         |
| `focus_outline` | bool | True    | `True` `False`            | Show a dashed outline when focused with the keyboard.                                           |
| `pill`          | bool | False   | `True` `False`            | Use fully rounded ends instead of the default radius.                                           |
| `class`         | str  | -       | -                         | Extra classes, merged with the defaults (later classes win).                                    |

You can add any standard HTML attribute, such as `target` or `rel`, and it will be passed through to the rendered element.

```html
<c-button href="https://example.org" target="_blank" rel="noopener noreferrer">External Site</c-button>

<!-- html output
<a href="https://example.org" target="_blank" rel="noopener noreferrer">External Site</a>
-->
```
