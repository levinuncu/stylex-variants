# StyleX Variants

## Documentation

The Documentation is available [here](https://stylex-variants.vercel.app/).

## Quick Start

### 1. Installation

```bash
npm add stylex-variants
# or
yarn add stylex-variants
# or
pnpm add stylex-variants
```

### 2. Usage

```js
import { sv } from 'stylex-variants';
import stylex from '@stylexjs/stylex';

const styles = stylex.create({
  // Your Styles
});

const buttonVariants = sv({
  base: styles.base,
  variants: {
    color: {
      primary: styles.primary,
      error: styles.error,
      succes: styles.succes,
    },
    size: {
      sm: styles.sm,
      md: styles.md,
      lg: styles.lg,
    },
  },
  defaultVariants: {
    size: 'md',
    color: 'primary',
  },
});

function Button() {
  return <button {...stylex.props(variants({ size: 'lg' }))}>Click me</button>;
}
```
