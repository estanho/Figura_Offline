# Figura Offline

By default, Figura blocks offline accounts for security reasons. Without Mojang authentication there is no way to verify who is actually connecting, which could allow malicious or spoofed uploads. This makes total sense and is expected behavior.

After finding [Sculptor](https://github.com/shiroyashik/sculptor), a project that allows you to run your own Figura backend with custom authentication, I removed those checks from the mod. On top of that I implemented a simple username-based whitelist to control who can connect to the backend, similar to Minecraft's default whitelist but without depending on whether the account is genuine or not.

The changes to the mod itself are minimal. Most of the work is on the setup side.

**This is a personal setup built for a specific server and it does not work by just downloading this fork.** There is a whole configuration side involving Sculptor and a custom authentication service that needs to be in place for this to work.

## What I use

- This Figura fork (client-side)
- [Sculptor](https://github.com/shiroyashik/sculptor) as the backend
- A custom authentication service with whitelist running alongside Sculptor on the same VM

## Credits

All credit for the original mod goes to the [Figura team](https://github.com/FiguraMC/Figura). This is an incredible project and this fork wouldn't exist without it. Big thanks to [shiroyashik](https://github.com/shiroyashik/sculptor) for Sculptor, which made this whole setup possible.

> This is a personal setup. A proper tutorial with full configuration details will be added in the future.


### 👉 [Return](https://github.com/estanho/Figura_Offline)