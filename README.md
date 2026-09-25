# osps-plugins

Builds of the Orion plugin pack. **The source is not here** — this repository
exists so the launcher has somewhere to fetch from.

## For players

Download **`Runelite.jar`** from Discord, put it wherever you like, and run
it. It downloads the current plugin pack and starts the Orion client with the
plugins loaded.

You only do that once. Every release after that arrives on its own the next
time you start the game.

### If double-clicking does nothing

You have no Java installed. Orion ships its own copy but does not register it,
so there is nothing on the machine that knows how to open a `.jar`. Install any
Java and it will work from then on.

Note that `orion-plugins.jar` — the file on the releases below — is **not** the
one you run. That is the pack, and the launcher downloads it for you. Running it
yourself does nothing at all.

### What it does

It checks this page for a newer pack each time you start it. If it cannot reach
GitHub, it starts the game with the plugins you already have.

Nothing is installed into or changed in your Orion folder. The downloaded pack
lives in `%LOCALAPPDATA%\OrionPlugins`.

## Something went wrong

Run it from a command prompt:

```
java -jar Runelite.jar --dry-run
```

That prints which Java it found, which client jar, and which pack version it
has, without starting anything. The client's own output is in
`%LOCALAPPDATA%\OrionPlugins\launcher.log`.
