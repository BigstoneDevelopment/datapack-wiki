---
title: Home
layout: default
---

# Welcome to the Bigstone Wiki

> _**The Bigstone Sandbox Datapack is currently under revision. Some information and links might be outdated or upcoming. For clarifications, please query the [Bigstone Devlopment Discord](https://discord.gg/u3dQCxGT).**_

## FAQ

### What is Bigstone?

Bigstone is a custom redstone-like system where components are supersized to a 16x16x16 block scale. Each Bigstone component simulates its function using regular redstone.

While scaling redstone components to larger sizes like this isn’t a new idea, Bigstone goes further by:

- Adding unique functionality to familiar components
- Introducing entirely new types of components (heavy repeaters, chain lamps, dust bridges, etc...)
- Following a consistent set of design rules to make components compatible with each other

At this point, it’s no longer just “big redstone”, which is why we call it Bigstone!

### What Platforms are Supported?

Currently only Minecraft Java Edition is supported, with no current plans to standardize for Bedrock Edition.

### Who created Bigstone?

Bigstone was originally created by [Daxis1](https://www.youtube.com/@Daxis1) (see [here](https://www.youtube.com/watch?v=0IJjAAtt9Z0)). [Bigstone Development](https://github.com/BigstoneDevelopment) has no offical connection to Daxis1.

## How Bigstone Works

Even though Bigstone isn’t meant to behave exactly like redstone, everything is still built using redstone. That means:

<!--TODO: replace 10 hz with a gt count-->
1. While Bigstone components have the opportunity to be very unique and interesting, they—and you by proxy—are still limited to what’s possible with vanilla redstone. You can’t, for example, make a Bigstone component that can instantly and wirelessly send a 10 Hz signal across dimensions.

1. Almost anyone can contribute! If you have Java Edition and a decent understanding of redstone, you can absolutely make your own Bigstone components! That’s one of the biggest reasons we created Bigstone Development and the Bigstone Sandbox Datapack: to give people a space to build and share their ideas.

## Compatibility Information

To keep Bigstone components consistent and cross compatible, we’ve followed a few core standards when building our own Bigstone components. Most importantly, we've standardized the input and output locations of components. This makes it easy to chain components without worrying about individually interfacing each one.

> For more information on standards, compatibility, and ports, see [Standards](https://wiki.bigstone.dev/standards).

### Bigstone Wires

All signal wires should use instant wire, meaning signals travel instantly down wire chains, regardless of the distance. Each wire should also be bidirectional, allowing for an input adjacent to each output.

### Directional Components

Some components, however—such as Bigstone Repeaters—are directional. These will only have one input and one output, typically on opposite sides. Even so, the output will still be aligned properly so it can connect with other wires and components that are bidirectional.

If you are planning to make your own Bigstone components, we recommend you follow the same standard so that your designs are easiest to use and compatible with the Bigstone Sandbox Datapack.

That being said, you are welcome to come up with your own standard, or, better yet, [contribute to our standard](https://github.com/BigstoneDevelopment/datapack-wiki).

_Last updated: 15/08/2025 at 03:48:00.045 UTC_
