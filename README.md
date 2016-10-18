# Practical Custom Selectors

**[Practical Custom Selectors]** are a collection of meaningful selector patterns designed to help you write cleaner, scalable, and easier to maintain CSS.

They are built upon [W3C CSS Extensions] and inspired by [Nicole Sullivan]’s fantastic [Object Oriented CSS].

```sh
npm install --save-dev jonathantneal/practical-custom-selectors
```

## Usage

Practical Custom Selectors are used like pseudo-classes. Their purposeful names make them highly readable and reusable.

*Before*:
```css
a, area, button, input, label, select, textarea, [tabindex] {
	cursor: pointer;
	touch-action: manipulation;
}
```

*After*:
```css
:--clickable {
	cursor: pointer;
	touch-action: manipulation;
}
```

---

They become even more helpful when nesting is required.

*Before*:
```css
button, [type="button"], [type="reset"], [type="submit"] {
	background-color: #44f;

	& :hover, & :focus {
		background-color: #22A;
	}
}
```

*After*:
```css
:--control-button {
	background-color: #44f;

	&:--enter {
		background-color: #22A;
	}
}
```

[Practical Custom Selectors]: https://github.com/jonathantneal/practical-custom-selectors
[W3C CSS Extensions]: https://drafts.csswg.org/css-extensions/#custom-selectors
[Nicole Sullivan]: https://github.com/stubbornella
[Object Oriented CSS]: https://www.smashingmagazine.com/2011/12/an-introduction-to-object-oriented-css-oocss/
