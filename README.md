# osps-plugins

Builds of the Orion plugin pack. **The source is not here** — this repository
exists so the launcher has somewhere to fetch from.

## For players

Download `OrionPlugins.jar` from Discord, put it wherever you like, and run it.
It downloads the current pack and starts the Orion client with the plugins
loaded.

You only ever do that once. Every release after that arrives on its own the
next time you start the game.

If double-clicking it does nothing at all, you have no Java installed. Orion
ships its own copy but does not register it, so nothing is there to open a
`.jar`. Install any Java, and it will work from then on.

It checks this page for a newer pack each time you start it. If it cannot
reach GitHub, it starts the game with the plugins you already have.

## Releases

Each release carries three files:

| file | what it is |
| --- | --- |
| `orion-plugins.jar` | the plugin pack |
| `orion-plugins.jar.sha256` | checked before it replaces anything |
| `version.txt` | how the launcher decides whether to download |

## Something went wrong

Run it from a command prompt:

```
java -jar OrionPlugins.jar --dry-run
```

That prints which Java it found, which client jar, and which pack it has,
without starting anything. The client's own output is in
`%LOCALAPPDATA%\OrionPlugins\launcher.log`.
