# Beginner's Guide Of Phaser

By, Xavier Hertzog

## Overview

If your someone like me, this is probably your first time hearing about Phaser. As of right now, I am on the road of building my first ever game, and about a week or two ago I came across Phaser. This guide will help you learn about Phaser and the basics of how to use it.

## About Phaser

Phaser is a popular HTML5 gaming framework that allows developers to create 2D games using languages JavaScript or TypeScript. It provides pre-written tools for physics engines, animations, audio, and asset management, making it quick and easy to make browser-based games. And it is also beginner friendly, with lots of tutorials, examples, and documentation you can learn from.

## How To Get Started

1. Open a new file in Vscode
2. Run npm create vite@latest

   ![alt text](<Screenshot 2025-06-20 143740.png>)

3. Choose Framework: Vanilla, and Variant: JavaScript or TypeScript
   ![alt text](<Screenshot 2025-06-20 143819.png>)

   ![alt text](<Screenshot 2025-06-20 143831.png>)

4. Cd into folder and run npm install
   ![alt text](<Screenshot 2025-06-20 143906.png>)

5. Run npm install phaser
   ![alt text](<Screenshot 2025-06-20 144343.png>)

6. And lastly, Run npm run dev

![alt text](<Screenshot 2025-06-20 145624.png>)

And then your good to go. Happy Building!

## Key Features of Phaser

Alright, we just went over how to create a file using Phaser. So now, we will talk about the key features of Phaser and the many things we can build to make our very own video game.

# Key Features

- Scene Systems - Splits games into modular scenes, like menus, levels, and cutscenes.
- Physics Engines - Uses built-in support more realistic and Arcade physics.

- Asset Management - Loads and manages images, audio, spritesheets, and more.
- Input Handling - Inputs all supported for keyboards, mouse, touch, and gamepad's.
- Animations - Used to easily create sprite animations.
- Tilemaps - Uses Tiled maps to design levels and maps for platformers, top-down games, and more.
- Camera & Viewport - Good for zooming in, panning, following the player, and applying effects.
- Sound - Has built-in audio sounds supported with Web Audio API.

## Compare and Contrast

Phaser is a gaming framework, not a language so you can't really compare it to other languages. But when using Phaser.js, which is basically using Phaser with JavaScript, the code can look a little different.

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <title>Phaser Starter</title>

    <!-- Make the game canvas fill the window -->
    <style>
      html,
      body {
        margin: 0;
        height: 100%;
      }
      canvas {
        display: block;
      }
    </style>

    <!-- Phaser 3 (latest stable) -->
    <script src="https://cdn.jsdelivr.net/npm/phaser@3/dist/phaser.js"></script>
  </head>

  <body>
    <!-- Main game code -->
    <script>
      /*=======================
        Basic Phaser config
      =======================*/
      const config = {
        type: Phaser.AUTO, // WebGL if available, else Canvas
        width: 800,
        height: 600,

        // Your first (and only) scene for now
        scene: {
          preload,
          create,
          update,
        },
      };

      /*=======================
        Launch the game
      =======================*/
      const game = new Phaser.Game(config);

      /*=======================
        Scene functions
      =======================*/
      function preload() {
        // Load a sample image from the Phaser Labs CDN
        this.load.image(
          "logo",
          "https://labs.phaser.io/assets/sprites/phaser3-logo.png"
        );
      }

      function create() {
        // Add it to the center of the canvas
        const img = this.add.image(config.width / 2, config.height / 2, "logo");

        // A tiny tween so you see movement
        this.tweens.add({
          targets: img,
          angle: 360,
          duration: 4000,
          repeat: -1,
        });
      }

      function update() {
        /* Game loop runs ~60 fps.
           Put per‑frame logic here */
      }
    </script>
  </body>
</html>
```

Above is starter code for Phaser. As you can see, this is written in HTML, but if you see the code it has words like game, preload, create, img, update, and many more, similar to what vocab would be used in a video game. This is because Phaser is used to make video games, so the vocab and code for it would be video game based.

## Summary

What we talked about

- About Phaser and how it's used
- How to get started
- Key features of Phaser
- Whats implemented into Phaser and some starter code

Phaser is a cool way to become a developer and start your own video game, and I hope this documentation helped you learn and understand it more. Thank you for reading!
