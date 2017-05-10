# WARP SCSS lint Configuration
WeAreReasonablePeople SCSS linting rules

> npm install --save-dev git@github.com:wearereasonablepeople/scss-lint-config-warp.git

This automatically copies the .scss-lint.yml to the project root after installation.

## Usage

### Disabling linter

#### Disable for the entire file

> // scss-lint:disable BorderZero </br>
> p { </br>
>   border: none; // No lint reported </br>
> }

#### Disable a few linters

**Disable for the entire file**
```scss
// scss-lint:disable BorderZero
p {
  border: none; // No lint reported
}
```

**Disable a few linters**
```scss
// scss-lint:disable BorderZero, StringQuotes
p {
  border: none; // No lint reported
  content: "hello"; // No lint reported
}
```

**Disable all lints within a block (and all contained blocks)**
```scss
p {
  // scss-lint:disable BorderZero
  border: none; // No lint reported
}

a {
  border: none; // Lint reported
}
```

**Disable and enable again**
```scss
// scss-lint:disable BorderZero
p {
  border: none; // No lint reported
}
// scss-lint:enable BorderZero

a {
  border: none; // Lint reported
}
```

**Disable/enable all linters**
```scss
// scss-lint:disable all
p {
  border: none; // No lint reported
}
// scss-lint:enable all

a {
  border: none; // Lint reported
}
```

### More info

[RTFM](https://github.com/brigade/scss-lint)
