This fork currently fixes the following issues in Gran Turismo 6 version 1.22:

- Black spots of reflections in cars (see https://github.com/RPCS3/rpcs3/issues/18607)

WIP:

- Currently trying to come up with a patch to disable MLAA/TAA without side issues. The already available patch by Illusion disables the AA and also fixes the tearing, but introduces big vertex explosions around the map which ruins the experience.

The MLAA/TAA disable patch and motion blur fix patch (fixes black replays) are located here: https://github.com/rleonever/rpcs3-GT6-1.22-fixes/blob/master/imported_patch.yml

- Currently trying to disable MLAA/TAA directly in the emulator pipeline without needing patches via a hack, to check if the vertex explosions still occur.

- (Optional) On version 1.22, if you don't disable MLAA/TAA via patch, the game has an annoying tearing effect which i also couldn't fix, if we could fix this, the game in theory could be playable without any major issues, besides the garbage anti aliasing implementation. I abandoned trying to fix this but if anyone manages to, god bless you.

Best scenario possible to run the game on 1.22: Enable Write and Read Color Buffers, set the resolution to 1080p (not your render resolution, the graphics mode). In 1080p mode, the AA is a lot less agressive compared to 720p, so the image, specially your car, will become more crisp, but the game will have some minor graphics downgrades. Tearing seems to happen a bit less when the game resolution is around 1080p and not higher (like 2K or 4K)


Any changes are welcome!








RPCS3
=====

[![GitHub Actions](https://img.shields.io/github/actions/workflow/status/RPCS3/rpcs3/rpcs3.yml?branch=master&logo=github&label=Actions)](https://github.com/RPCS3/rpcs3/actions/workflows/rpcs3.yml)
[![RPCS3 Discord Server](https://img.shields.io/discord/272035812277878785?color=5865F2&label=RPCS3%20Discord&logo=discord&logoColor=white)](https://discord.gg/rpcs3)

The world's first free and open-source PlayStation 3 emulator/debugger, written in C++ for Windows, Linux, macOS and FreeBSD.

You can find some basic information on our [**website**](https://rpcs3.net/). Game info is being populated on the [**Wiki**](https://wiki.rpcs3.net/).
For discussion about this emulator, PS3 emulation, and game compatibility reports, please visit our [**forums**](https://forums.rpcs3.net) and our [**Discord server**](https://discord.gg/RPCS3).

[**Support the Lead Developers on Patreon**](https://rpcs3.net/patreon)

## Contributing

If you want to help the project but do not code, the best way to help out is to test games and make bug reports. See:
* [Quickstart](https://rpcs3.net/quickstart)

If you want to contribute as a developer, please take a look at the following pages:

* [Coding Style](https://github.com/RPCS3/rpcs3/wiki/Coding-Style)
* [Developer Information](https://github.com/RPCS3/rpcs3/wiki/Developer-Information)

You should also contact any of the developers in the forums or in the Discord server to learn more about the current state of the emulator.

### AI Use

Use of AI tools for research and reverse engineering purposes is permitted. However, contributors are expected to fully own and understand all code they submit. Any communication with the team — including code, code comments, and GitHub comments — must come from the human contributor, not an AI agent acting autonomously.

We have unfortunately seen a rise in untested and unverified AI-generated slop being submitted to this project. This wastes maintainer time and, in worse cases, such changes get merged and break functionality for all users. Repeated violations will result in a ban from the repository. Please be respectful of everyone's time.

**Pull requests opened by AI agents or automated tools must include a disclosure in the PR description** stating the scope of AI involvement — which parts were AI-generated and what human testing or review was performed prior to submission. PRs that omit this disclosure may be closed without review.

If you are unsure about your work, open a discussion issue to talk it through with the team, or reach out to a maintainer on [Discord](https://discord.gg/RPCS3).

## Building

See [BUILDING.md](BUILDING.md) for more information about how to setup an environment to build RPCS3.

## Running

Check our friendly [quickstart](https://rpcs3.net/quickstart) guide to make sure your computer meets the minimum system requirements to run RPCS3.

Don't forget to have your graphics driver up to date and to install the [Visual C++ Redistributable Packages for Visual Studio 2022](https://aka.ms/vs/17/release/VC_redist.x64.exe) if you are a Windows user.

## License

Most files are licensed under the terms of GNU GPL-2.0-only License; see LICENSE file for details. Some files may be licensed differently; check appropriate file headers for details.
