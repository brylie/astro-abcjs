
# astro-abcjs

An abcjs component for Astro projects.

## Usage

### In .astro files

Import the component and use it in your Astro page or component:

```astro
---
import AbcjsPlayer from 'astro-abcjs/AbcjsPlayer.astro';
---

<AbcjsPlayer
  notation={`X:1\nT:Scale\nM:4/4\nK:C\nC D E F | G A B c |`}
  showControls={true}
  responsive={true}
  abcjsVersion="6.6.0"
/>
```

### In MDX files

First, make sure your project supports MDX and components in MDX.

Import the component at the top of your MDX file:

```mdx
import AbcjsPlayer from 'astro-abcjs/AbcjsPlayer.astro';

<AbcjsPlayer
  notation={`X:1\nT:Scale\nM:4/4\nK:C\nC D E F | G A B c |`}
  showControls={true}
  responsive={true}
  abcjsVersion="6.6.0"
/>
```

#### Props

- `notation` (string, required): The ABC notation string to render.
- `showControls` (boolean, default: true): Show audio playback controls.
- `responsive` (boolean, default: true): Make the notation responsive to container size.
- `abcjsVersion` (string, optional, default: "6.6.0"): The abcjs version to load from CDN. Override to pin or upgrade/downgrade.

## Credits & Inspiration

This component was inspired by the article [Building a Reusable Music Component in Astro using ABCjs](https://www.pavlinbg.com/posts/building-a-reusable-music-component-in-astro-using-abcjs) by [Pavlin Gunov](https://www.pavlinbg.com/).
