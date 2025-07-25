---
title: :optional
slug: Web/CSS/:optional
page-type: css-pseudo-class
browser-compat: css.selectors.optional
sidebar: cssref
---

The **`:optional`** [CSS](/en-US/docs/Web/CSS) [pseudo-class](/en-US/docs/Web/CSS/Pseudo-classes) represents any {{HTMLElement("input")}}, {{HTMLElement("select")}}, or {{HTMLElement("textarea")}} element that does not have the [`required`](/en-US/docs/Web/HTML/Reference/Elements/input#required) attribute set on it.

{{InteractiveExample("CSS Demo: :optional", "tabbed-standard")}}

```css interactive-example
label {
  display: block;
  margin-top: 1em;
}

.req {
  color: red;
}

*:optional {
  background-color: palegreen;
}
```

```html interactive-example
<form>
  <label for="name">Name: <span class="req">*</span></label>
  <input id="name" name="name" type="text" required />

  <label for="birth">Date of Birth:</label>
  <input id="birth" name="birth" type="date" />

  <label for="origin"
    >How did you find out about us? <span class="req">*</span></label
  >
  <select id="origin" name="origin" required>
    <option>Google</option>
    <option>Facebook</option>
    <option>Advertisement</option>
  </select>
  <p><span class="req">*</span> - Required field</p>
</form>
```

This pseudo-class is useful for styling fields that are not required to submit a form.

> [!NOTE]
> The {{cssxref(":required")}} pseudo-class selects _required_ form fields.

## Syntax

```css
:optional {
  /* ... */
}
```

## Accessibility

If a [form](/en-US/docs/Web/HTML/Reference/Elements/form) contains optional {{htmlelement("input")}}s, required inputs should be indicated using the [`required`](/en-US/docs/Web/HTML/Reference/Elements/input#required) attribute. This will ensure that people navigating with the aid of assistive technology such as a screen reader will be able to understand which inputs need valid content to ensure a successful form submission.

Required inputs should also be indicated visually, using a treatment that does not rely solely on color to convey meaning. Typically, descriptive text and/or an icon are used.

- [MDN Understanding WCAG, Guideline 3.3 explanations](/en-US/docs/Web/Accessibility/Guides/Understanding_WCAG/Understandable#guideline_3.3_%e2%80%94_input_assistance_help_users_avoid_and_correct_mistakes)
- [Understanding Success Criterion 3.3.2 | W3C Understanding WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/minimize-error-cues.html)

## Examples

### The optional field has a purple border

#### HTML

```html
<form>
  <div class="field">
    <label for="url_input">Enter a URL:</label>
    <input type="url" id="url_input" />
  </div>

  <div class="field">
    <label for="email_input">Enter an email address:</label>
    <input type="email" id="email_input" required />
  </div>
</form>
```

#### CSS

```css
label {
  display: block;
  margin: 1px;
  padding: 1px;
}

.field {
  margin: 1px;
  padding: 1px;
}

input:optional {
  border-color: rebeccapurple;
  border-width: 3px;
}
```

#### Result

{{EmbedLiveSample('Examples', 600, 120)}}

## Specifications

{{Specifications}}

## Browser compatibility

{{Compat}}

## See also

- Other validation-related pseudo-classes: {{ cssxref(":required") }}, {{ cssxref(":invalid") }}, {{ cssxref(":valid") }}
- [Form data validation](/en-US/docs/Learn_web_development/Extensions/Forms/Form_validation)
