# Vue Human Muscle Anatomy

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A customizable Vue 3 component for displaying a human muscle anatomy chart with highlighted muscle groups, using an SVG I created myself. Built with TypeScript for scalability and type safety.

![Screenshot of the muscle anatomy component](https://raw.githubusercontent.com/LucaWahlen/vue-human-muscle-anatomy/refs/heads/main/screenshot.png)

## Features

*   **Scalable SVG:** Renders a crisp SVG image that scales to any size.
*   **Customizable Colors:** Easily change the colors for default muscles, primary highlights, and secondary highlights.
*   **Opacity Control:** Adjust the opacity of highlighted muscle groups.
*   **Dynamic Highlighting:** Pass arrays of muscle groups to highlight them as primary or secondary.
*   **TypeScript Support:** Fully typed for a better development experience.
*   **Lightweight:** No external dependencies.

## Installation

Install the package using your favorite package manager:

```bash
# npm
npm install @lucawahlen/vue-human-muscle-anatomy

# yarn
yarn add @lucawahlen/vue-human-muscle-anatomy
```

## Usage

Import the component and use it in your Vue templates. You can control the highlighted muscles by passing arrays of muscle group names to the `selectedPrimaryMuscleGroups` and `selectedSecondaryMuscleGroups` props.

```vue
<template>
  <div>
    <h1>My Workout Plan</h1>
    <HumanAnatomy
      :selected-primary-muscle-groups="['triceps', 'lowerBack']"
      :selected-secondary-muscle-groups="['hamstrings', 'calves']"
      primary-highlight-color="#007bff"
      secondary-highlight-color="#5cafff"
    />
  </div>
</template>

<script setup lang="ts">
import HumanAnatomy from '@lucawahlen/vue-human-muscle-anatomy';
</script>
```

## Props

The component accepts the following props:

| Prop                          | Type             | Description                                                | Default         |
| ----------------------------- | ---------------- | ---------------------------------------------------------- | --------------- |
| `defaultMuscleColor`          | `string`         | The color for non-highlighted muscles.                     | `'#1f1f1f'`     |
| `backgroundColor`             | `string`         | The background color of the SVG.                           | `'#000000'`     |
| `primaryHighlightColor`       | `string`         | The highlight color for primary muscle groups.             | `'#ff0000'`     |
| `secondaryHighlightColor`     | `string`         | The highlight color for secondary muscle groups.           | `'#ff0000'`     |
| `primaryOpacity`              | `number`         | The opacity for primary highlights (0 to 1).               | `0.5`           |
| `secondaryOpacity`            | `number`         | The opacity for secondary highlights (0 to 1).             | `0.2`           |
| `selectedPrimaryMuscleGroups` | `MuscleGroup[]`  | An array of primary muscle groups to highlight.            | `[]`            |
| `selectedSecondaryMuscleGroups`| `MuscleGroup[]` | An array of secondary muscle groups to highlight.          | `[]`            |

## Available Muscle Groups

You can pass the following string values in the `selectedPrimaryMuscleGroups` and `selectedSecondaryMuscleGroups` arrays.

*   `triceps`
*   `forearms`
*   `abductors`
*   `adductors`
*   `hamstrings`
*   `quads`
*   `shins`
*   `calves`
*   `lowerBack`
*   `rotatorCuffs`
*   `rearDelts`
*   `lats`
*   `traps`
*   `glutes`
*   `neck`

## License

Distributed under the MIT License. See `LICENSE` for more information.
