---
title: Application launcher
section: components
cssPrefix: pf-c-app-launcher
---

import './AppLauncher.css'

## Examples
```hbs title=Collapsed
{{#> app-launcher id="app-launcher-collapsed"}}
  {{#> app-launcher-menu}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link{{/app-launcher-menu-item}}</li>
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--type="button"}}Action{{/app-launcher-menu-item}}</li>
    {{#> app-launcher-separator}}{{/app-launcher-separator}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-disabled" app-launcher-menu-item--attribute='href="#" aria-disabled="true" tabindex="-1"'}}Disabled link{{/app-launcher-menu-item}}</li>
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=Disabled
{{#> app-launcher id="app-launcher-disabled" app-launcher--IsDisabled="true"}}
  {{#> app-launcher-menu}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link{{/app-launcher-menu-item}}</li>
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--type="button"}}Action{{/app-launcher-menu-item}}</li>
    {{#> app-launcher-separator}}{{/app-launcher-separator}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-disabled" app-launcher-menu-item--attribute='href="#" aria-disabled="true" tabindex="-1"'}}Disabled link{{/app-launcher-menu-item}}</li>
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=Expanded
{{#> app-launcher id="app-launcher-expanded"  app-launcher--IsExpanded="true"}}
  {{#> app-launcher-menu}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link{{/app-launcher-menu-item}}</li>
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--type="button"}}Action{{/app-launcher-menu-item}}</li>
    {{#> app-launcher-separator}}{{/app-launcher-separator}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-disabled" app-launcher-menu-item--attribute='href="#" aria-disabled="true" tabindex="-1"'}}Disabled link{{/app-launcher-menu-item}}</li>
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=Aligned-right
{{#> app-launcher id="app-launcher-aligned-right" app-launcher--IsExpanded="true"}}
  {{#> app-launcher-menu app-launcher-menu--modifier="pf-m-align-right"}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link{{/app-launcher-menu-item}}</li>
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--type="button"}}Action{{/app-launcher-menu-item}}</li>
    {{#> app-launcher-separator}}{{/app-launcher-separator}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-disabled" app-launcher-menu-item--attribute='href="#" aria-disabled="true" tabindex="-1"'}}Disabled link{{/app-launcher-menu-item}}</li>
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=Aligned-top
{{#> app-launcher id="app-launcher-aligned-top" app-launcher--IsExpanded="true" app-launcher--modifier="pf-m-top"}}
  {{#> app-launcher-menu}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link{{/app-launcher-menu-item}}</li>
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--type="button"}}Action{{/app-launcher-menu-item}}</li>
    {{#> app-launcher-separator}}{{/app-launcher-separator}}
    <li>{{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-disabled" app-launcher-menu-item--attribute='href="#" aria-disabled="true" tabindex="-1"'}}Disabled link{{/app-launcher-menu-item}}</li>
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=With-sections-and-dividers-between-sections
{{#> app-launcher id="app-launcher-sections-and-dividers-between-sections" app-launcher--IsExpanded="true" app-launcher--IsGrouped="true"}}
  {{#> app-launcher-menu}}
    {{#> app-launcher-group}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link not in group{{/app-launcher-menu-item}}</li>
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-separator app-launcher-separator--IsHr="true"}}{{/app-launcher-separator}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 1
      {{/app-launcher-group-title}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 1 link{{/app-launcher-menu-item}}</li>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 1 link{{/app-launcher-menu-item}}</li>
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-separator app-launcher-separator--IsHr="true"}}{{/app-launcher-separator}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 2
      {{/app-launcher-group-title}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 2 link{{/app-launcher-menu-item}}</li>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 2 link{{/app-launcher-menu-item}}</li>
      </ul>
    {{/app-launcher-group}}
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=With-sections-and-dividers-between-items
{{#> app-launcher id="app-launcher-sections-and-dividers-between-items" app-launcher--IsExpanded="true" app-launcher--IsGrouped="true"}}
  {{#> app-launcher-menu}}
    {{#> app-launcher-group}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Link not in group{{/app-launcher-menu-item}}</li>
        {{#> app-launcher-separator}}{{/app-launcher-separator}}
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 1
      {{/app-launcher-group-title}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 1 link{{/app-launcher-menu-item}}</li>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 1 link{{/app-launcher-menu-item}}</li>
        {{#> app-launcher-separator}}{{/app-launcher-separator}}
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 2
      {{/app-launcher-group-title}}
      <ul>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 2 link{{/app-launcher-menu-item}}</li>
        <li>{{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}Group 2 link{{/app-launcher-menu-item}}</li>
      </ul>
    {{/app-launcher-group}}
  {{/app-launcher-menu}}
{{/app-launcher}}
```

```hbs title=With-sections,-dividers,-icons,-and-external-links
{{#> app-launcher id="app-launcher-sections-dividers-icons-and-external-links" app-launcher--IsExpanded="true" app-launcher--IsGrouped="true"}}
  {{#> app-launcher-menu}}
    {{#> app-launcher-group}}
      <ul>
        <li>
          {{#> app-launcher-menu-item app-launcher-menu-item--attribute='href="#"'}}
            {{#> app-launcher-menu-item-icon}}
              <img src="/assets/images/pf-logo-small.svg" alt="">
            {{/app-launcher-menu-item-icon}}
            Link not in group
          {{/app-launcher-menu-item}}
        </li>
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-separator app-launcher-separator--IsHr="true"}}{{/app-launcher-separator}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 1
      {{/app-launcher-group-title}}
      <ul>
        <li>
          {{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-external" app-launcher-menu-item--attribute='href="#" target="_blank"'}}
            {{#> app-launcher-menu-item-icon}}
              <img src="/assets/images/pf-logo-small.svg" alt="">
            {{/app-launcher-menu-item-icon}}
            Group 1 link
            {{> app-launcher-menu-item-external-icon}}
          {{/app-launcher-menu-item}}
        </li>
        <li>
          {{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-external" app-launcher-menu-item--attribute='href="#" target="_blank"'}}
            {{#> app-launcher-menu-item-icon}}
              <img src="/assets/images/pf-logo-small.svg" alt="">
            {{/app-launcher-menu-item-icon}}
            Group 1 link
            {{> app-launcher-menu-item-external-icon}}
          {{/app-launcher-menu-item}}
        </li>
        {{#> app-launcher-separator}}{{/app-launcher-separator}}
      </ul>
    {{/app-launcher-group}}
    {{#> app-launcher-group}}
      {{#> app-launcher-group-title}}
        Group 2
      {{/app-launcher-group-title}}
      <ul>
        <li>
          {{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-external" app-launcher-menu-item--attribute='href="#" target="_blank"'}}
            {{#> app-launcher-menu-item-icon}}
              <img src="/assets/images/pf-logo-small.svg" alt="">
            {{/app-launcher-menu-item-icon}}
            Group 2 link
            {{> app-launcher-menu-item-external-icon}}
          {{/app-launcher-menu-item}}
        </li>
        <li>
          {{#> app-launcher-menu-item app-launcher-menu-item--modifier="pf-m-external" app-launcher-menu-item--attribute='href="#" target="_blank"'}}
            {{#> app-launcher-menu-item-icon}}
              <img src="/assets/images/pf-logo-small.svg" alt="">
            {{/app-launcher-menu-item-icon}}
            Group 2 link
            {{> app-launcher-menu-item-external-icon}}
          {{/app-launcher-menu-item}}
        </li>
      </ul>
    {{/app-launcher-group}}
  {{/app-launcher-menu}}
{{/app-launcher}}
```

## Documentation
### Accessibility
| Attribute | Applied | Outcome |
| -- | -- | -- |
| `aria-label="Application launcher"` | `.pf-c-app-launcher` |  Gives the app launcher element an accessible name. **Required** |
| `aria-expanded="false"` | `.pf-c-button` |  Indicates that the menu is hidden. |
| `aria-expanded="true"` | `.pf-c-button` |  Indicates that the menu is visible. |
| `aria-label="Actions"` | `.pf-c-button` | Provides an accessible name for the app launcher when an icon is used. **Required** |
| `hidden` | `.pf-c-app-launcher__menu` | Indicates that the menu is hidden so that it isn't visible in the UI and isn't accessed by assistive technologies. |
| `disabled` | `.pf-c-app-launcher__toggle` | Disables the app launcher toggle and removes it from keyboard focus. |
| `disabled` | `button.pf-c-app-launcher__menu-item` | When the menu item uses a button element, indicates that it is unavailable and removes it from keyboard focus. |
| `aria-disabled="true"` | `a.pf-c-app-launcher__menu-item` | When the menu item uses a link element, indicates that it is unavailable. |
| `tabindex="-1"` | `a.pf-c-app-launcher__menu-item` | When the menu item uses a link element, removes it from keyboard focus. |
| `aria-hidden="true"` | `.pf-c-app-launcher__menu-item-external-icon` | Hides the icon from assistive technologies. |

### Usage
| Class | Applied | Outcome |
| -- | -- | -- |
| `.pf-c-app-launcher` | `<nav>` | Defines the parent wrapper of the app launcher. |
| `.pf-c-app-launcher__menu` | `<ul>`, `<div>` | Defines the parent wrapper of the menu items. Use a `<div>` if your app launcher has groups. |
| `.pf-c-app-launcher__group` | `<section>` | Defines a group of items. Required when there is more than one group. |
| `.pf-c-app-launcher__group-title` | `<h1>` | Defines a title for a group of items. |
| `.pf-c-app-launcher__menu-item` | `<a>`, `<button>` | Defines a menu item. |
| `.pf-c-app-launcher__menu-item-icon` | `<span>` | Defines the wrapper for the menu item icon. |
| `.pf-c-app-launcher__menu-item-external-icon` | `<i>` | Defines the external link icon that appears on hover/focus. Use with `.pf-m-external`. |
| `.pf-c-app-launcher__separator` | `<li>`, `<hr>` | Defines a separator within the menu. Can be used between items (`<li>`) or  between groups (`<hr>`). There are no visual differences between the types of elements used as a separator. The different elements allowed are only to support valid markup depending on where you place the separator. |
| `.pf-m-expanded` | `.pf-c-app-launcher` | Modifies for the expanded state. |
| `.pf-m-top` | `.pf-c-app-launcher` | Modifies to display the menu above the toggle. |
| `.pf-m-align-right` | `.pf-c-app-launcher__menu` | Modifies to display the menu aligned to the right edge of the toggle. |
| `.pf-m-hover` | `.pf-c-app-launcher__menu-item` | Forces display of the hover state of the element. This state is primarily for demonstration purposes and would not normally be used in lieu of the `:hover` pseudo-class. |
| `.pf-m-focus` | `.pf-c-app-launcher__menu-item` | Forces display of the focus state of the element. This state is primarily for demonstration purposes and would not normally be used in lieu of the `:focus` pseudo-class. |
| `.pf-m-disabled` | `a.pf-c-app-launcher__menu-item` | Modifies to display the menu item as disabled. |
| `.pf-m-external` | `.pf-c-app-launcher__menu-item` | Modifies to display the menu item as having an external link icon on hover/focus. |
