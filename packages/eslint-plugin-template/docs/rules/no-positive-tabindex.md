<!--

  DO NOT EDIT.

  This markdown file was autogenerated using a mixture of the following files as the source of truth for its data:
  - ../../src/rules/no-positive-tabindex.ts
  - ../../tests/rules/no-positive-tabindex/cases.ts

  In order to update this file, it is therefore those files which need to be updated, as well as potentially the generator script:
  - ../../../../tools/scripts/generate-rule-docs.ts

-->

# `@angular-eslint/template/no-positive-tabindex`

Ensures that the `tabindex` attribute is not positive

- Type: suggestion
- Category: Best Practices

<br>

## Rule Options

The rule does not have any configuration options.

<br>

## Usage Examples

> The following examples are generated automatically from the actual unit tests within the plugin, so you can be assured that their behavior is accurate based on the current commit.

<br>

❌ - Examples of **incorrect** code for this rule:

```html
<div tabindex="5"></div>
               ~
```

```html
<div [attr.tabindex]="21"></div>
                      ~~
```

<br>

---

<br>

✅ - Examples of **correct** code for this rule:

```html
<span></span>
```

```html
<span id="2"></span>
```

```html
<span tabindex></span>
```

```html
<span tabindex="-1"></span>
```

```html
<span tabindex="0"></span>
```

```html
<span [attr.tabindex]="-1"></span>
```

```html
<span [attr.tabindex]="0"></span>
```

```html
<span [attr.tabindex]="tabIndex"></span>
```

```html
<span [attr.tabindex]="null"></span>
```

```html
<span [attr.tabindex]="undefined"></span>
```

```html
<app-test [tabindex]="1"></app-test>
```