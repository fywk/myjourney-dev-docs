# Input

A customizable input component with support for icons.

## Basic Usage

{{< component-preview flexDirection="column" >}}
<input type="text" class="c-input" placeholder="Enter your name" data-size="md">
{{< /component-preview >}}

```html
<c-input placeholder="Enter your name" />
```

## Types

{{< component-preview flexDirection="column" >}}
<input type="text" class="c-input" placeholder="Text (default)" data-size="md">
<input type="email" class="c-input" placeholder="Email address" data-size="md">
<input type="password" class="c-input" placeholder="Password" data-size="md">
<input type="number" class="c-input" placeholder="Number" data-size="md">
<input type="url" class="c-input" placeholder="URL" data-size="md">
{{< /component-preview >}}

```html
<c-ui.input type="text" placeholder="Text (default)" />
<c-ui.input type="email" placeholder="Email address" />
<c-ui.input type="password" placeholder="Password" />
<c-ui.input type="number" placeholder="Number" />
<c-ui.input type="url" placeholder="URL" />
```

## Sizes

{{< component-preview flexDirection="column" >}}
<input type="text" class="c-input" placeholder="Extra Small" data-size="xs">
<input type="text" class="c-input" placeholder="Small" data-size="sm">
<input type="text" class="c-input" placeholder="Medium (default)" data-size="md">
<input type="text" class="c-input" placeholder="Large" data-size="lg">
<input type="text" class="c-input" placeholder="Extra Large" data-size="xl">
{{< /component-preview >}}

```html
<c-input placeholder="Extra Small" size="xs" />
<c-input placeholder="Small" size="sm" />
<c-input placeholder="Medium (default)" size="md" />
<c-input placeholder="Large" size="lg" />
<c-input placeholder="Extra Large" size="xl" />
```

## Icons

Use the `left_icon` or `right_icon` named slots to place an icon on either edge of the input.

{{< component-preview flexDirection="column" >}}
<div class="relative flex w-full items-center">
    <div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-[1.75ch] text-gray-500"><svg class="size-4.5" aria-hidden="true" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M3 10a7 7 0 1 0 14 0a7 7 0 1 0 -14 0"></path><path d="M21 21l-6 -6"></path></svg></div>
    <input type="text" class="c-input pl-[5.5ch] pr-[5.5ch]" placeholder="Search" data-size="md">
    <div class="pointer-events-none absolute inset-y-0 right-0 flex items-center pr-[1.75ch] text-gray-500"><svg class="size-4.5" aria-hidden="true" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M17 5l-10 14"></path></svg></div>
</div>
<div class="relative flex w-full items-center">
    <div class="pointer-events-none absolute inset-y-0 left-0 flex items-center pl-[1.75ch] text-gray-500"><svg class="size-5" aria-hidden="true" fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path d="M3 7a2 2 0 0 1 2 -2h14a2 2 0 0 1 2 2v10a2 2 0 0 1 -2 2h-14a2 2 0 0 1 -2 -2v-10"></path><path d="M3 7l9 6l9 -6"></path></svg></div>
    <input type="email" class="c-input pl-[5.5ch]" placeholder="name@example.com" data-size="md">
</div>
{{< /component-preview >}}

```html {hl_lines=["2-7","10-12"]}
<c-input placeholder="Search">
  <c-slot name="left_icon">
    <c-tablericon.search class="size-4.5">
  </c-slot>
  <c-slot name="right_icon">
    <c-tablericon.slash class="size-4.5">
  </c-slot>
</c-input>
<c-input type="email" placeholder="name@example.com">
  <c-slot name="left_icon">
    <c-tablericon.mail class="size-4.5">
  </c-slot>
</c-input>
```

## States

{{< component-preview flexDirection="column" >}}
<input type="text" class="c-input" placeholder="You can't edit this" data-size="md" disabled>
<input type="text" class="c-input" value="This is a read-only text input" data-size="md" readonly>
{{< /component-preview >}}

```html
<c-input placeholder="You can't edit this" disabled />
<c-input value="This is a read-only text input" readonly />
```

## API Reference

### Props

| Attribute     | Type    | Default  | Description                                                                               |
| ------------- | ------- | -------- | ----------------------------------------------------------------------------------------- |
| `type`        | string  | `"text"` | The HTML input type, e.g. `text`, `email`, `password`, `number`, `url`.                   |
| `name`        | string  | `""`     | The input's `name` attribute. Only rendered when set.                                     |
| `value`       | string  | `""`     | The initial value of the input. Only rendered when set.                                   |
| `placeholder` | string  | `""`     | Placeholder text shown when the input is empty. Only rendered when set.                   |
| `size`        | string  | `"md"`   | Controls the input size via `data-size`. One of `xs`, `sm`, `md`, `lg`, `xl`.             |
| `disabled`    | boolean | `False`  | Disables the input. Pass with `:disabled="True"` or the bare `disabled` attribute.        |
| `readonly`    | boolean | `False`  | Makes the input read-only. Pass with `:readonly="True"` or the bare `readonly` attribute. |
| `class`       | string  | `""`     | Additional CSS classes appended to the `<input>` element.                                 |

Any other attributes (e.g. `id`, `required`, `autocomplete`, `hx-*`, `x-*`) are passed through to the underlying `<input>` element.

### Slots

| Slot         | Description                                                                      |
| ------------ | -------------------------------------------------------------------------------- |
| `left_icon`  | Icon displayed on the left edge of the input. Adds left padding automatically.   |
| `right_icon` | Icon displayed on the right edge of the input. Adds right padding automatically. |
