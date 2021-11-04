# Ng Icons

The all-in-one icon library for Angular. This allows you to use icons from multiple icon sets with a single icon component.

Currently, we support the following libraries:

- [Heroicons](https://heroicons.com/)
- [Feather Icons](https://feathericons.com/)
- [Jam Icons](https://jam-icons.com/)
- [Octicons](https://github.com/primer/octicons)
- [Radix UI Icons](https://icons.modulz.app/)
- [Tabler Icons](https://tabler-icons.io/)

Got suggestions for additional iconsets? Create an issue and we can consider adding them!

## Installation

Ng Icons consists of multiple packages:

- `@ng-icons/core` - This contains the icon component and the `NgIconsModule` that is used to register the icons you want to include in your application.
- `@ng-icons/heroicons` - The Heroicons iconset including both outline and solid variants.
- `@ng-icons/feather-icons` - The Feather Icons iconset.
- `@ng-icons/jam-icons` - The Jam Icons iconset.
- `@ng-icons/octicons` - The Octicons iconset.
- `@ng-icons/radix-icons` - The Radix UI iconset.
- `@ng-icons/tabler-icons` - The Tabler iconset.

You must install the `@ng-icons/core` package, however you only need to install the iconset libraries you intend to use.

E.g:

```bash
npm i @ng-icons/core @ng-icons/heroicons ...
```

or

```bash
yarn add @ng-icons/core @ng-icons/heroicons ...
```

## Usage

Import the `NgIconsModule` and register the icons you wish to use:

```ts
import { NgIconsModule } from '@ng-icons/core';
import { FeatherAirplay } from '@ng-icons/feather-icons';
import { HeroUsers } from '@ng-icons/heroicons';

@NgModule({
  imports: [
    BrowserModule,
    NgIconsModule.withIcons({ FeatherAirplay, HeroUsers }),
  ],
})
export class AppModule {}
```

You can register icons in multiple modules, this allows icons to be lazy loaded in child modules.

You can then use the icon in your templates:

```html
<ng-icon name="feather-airplay"></ng-icon>
```

| Name        | Type             | Description                          |
| ----------- | ---------------- | ------------------------------------ |
| size        | string           | Define the size of the icon.         |
| strokeWidth | string \| number | Define the stroke-width of the icon. |