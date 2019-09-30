# Vue Drip Button 
![version](https://img.shields.io/npm/v/@arikardnoir/vue-drip-button) [![npm downloads](https://img.shields.io/npm/dt/@arikardnoir/vue-drip-button.svg)](https://www.npmjs.com/package/@arikardnoir/vue-drip-button) <a href="https://www.npmjs.com/package/@arikardnoir/vue-drip-button"> [![Software License](https://img.shields.io/npm/l/@arikardnoir/vue-drip-button)](LICENSE)
> A Vue.js plugin to easily integrate button in your projects.

Vue Drip Button is a simple button that give a lot of alternatives to work with, instead of using a predefined button.


## Instalation
Install the package from npm by running:
``` bash
# install dependencies
npm i @arikardnoir/vue-drip-button
```

## Usage
Import, register and place the component in your Vue app.
```html
<template>
  <VueDripButton />
</template>
```

```html
import VueDripButton from 'vue-drip-button'

export default {
  components: {
    VueDripButton,
  }
}
```

## Accessibility
Apply attributes, directly on the element to apply them to the button.
```html
<template>
  <VueDripButton
    classType="button success"
    text="New Product"
    :needSpinner="true"
    :isRequesting="true"
  />
</template>
```

## Props
Components Property that make him cool

|Name              |Type          |Default           |Description                                           |
|------------------|--------------|------------------|------------------------------------------------------|
|classType         |String        |button success    |This prop allow to change button color,according to our terms
|text              |String        |                  |This prop allow you to change the button text
|needSpinner       |Boolean       |false             |With this prop you make choice if you want to use spinner on this button
|isRequesting      |Boolean       |false             |This prop make sense if you will use the Spinner, i could help your button spinner work if the two are in TRUE mode.
|isDisabled        |Boolean       |false             |This prop is for disable your button


## Button Colour Styles
Component classType for change the Style

|classType                 |Type              |Image                                      |
|--------------------------|------------------|-------------------------------------------|
|primary                   |String            |   ![picture](./img/primary.png)           |
|secondary                 |String            |   ![picture](./img/secondary.png)         |
|warning                   |String            |   ![picture](./img/warning.png)           |
|danger                    |String            |   ![picture](./img/danger.png)            |
|success                   |String (default)  |   ![picture](./img/success.png)           |
|info                      |String            |   ![picture](./img/info.png)              |
|primary-outline           |String            |   ![picture](./img/primary-outline.png)   |
|secondary-outline         |String            |   ![picture](./img/secondary-outline.png) |
|warning-outline           |String            |   ![picture](./img/warning-outline.png)   |
|danger-outline            |String            |   ![picture](./img/danger-outline.png)    |
|success-outline           |String            |   ![picture](./img/success-outline.png)   |
|info-outline              |String            |   ![picture](./img/info-outline.png)      |
