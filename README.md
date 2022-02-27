# TCR (Test && Commit || Revert) utility for TypeScript

Before we start, all the credits goes to [Murex](https://github.com/murex).
This utility is based on [their implementation](https://github.com/murex/Kata-BowlingGame).
I'd like to thank them for their incredible work.
Feel free to check theirs repos and I'd recommend you attend one of their workshops.

All I did was focusing on the TypeScript language and make it easy to be integrated in a solution.

So I won't be explaining how the utility works as I didn't modify the internals.
If you'd like to know how to use it, feel free to check [their documentation](https://github.com/murex/Kata-BowlingGame/blob/master/tcr/TCR.md).
I will focused on what makes this one specific and how to integrate it in a solution.

## Licence

[Here](LICENSE.md)'s the licence file, from [Murex](https://github.com/murex).

## Toolchain selection

The script can support multiple toolchains.
I mainly focused on being compatible with main test frameworks.

| Toolchain | Default |
| --------- | ------- |
| npm       | &check; |
| yarn      |         |

You do not have to install anything in order to use them. They are just triggering the `build` and `test` scripts from within your `package.json` file.

In order to select a specific toolchain, you will have to use the toolchain option `-t` with the name of the toolchain.
For example, running the utility using the default toolchain (npm) requires this command: `./tcrw`, while using a specific toolchain (yarn) requires this one: `./tcrw -t yarn`.

## Integration

This is the easy part!

Please keep in mind you have to follow a strict folder structure.

Knowing that, just copy both [tcr folder](tcr) and [watcher script](tcrw) at the root of your solution, at the same level than both `src` and `tests` folders.

This is it. Then run the script and have fun!
