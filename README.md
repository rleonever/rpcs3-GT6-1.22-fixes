This fork currently fixes the following issues in Gran Turismo 6 version 1.22:

- Black spots of reflections in cars (see https://github.com/RPCS3/rpcs3/issues/18607)

WIP:

- Currently trying to come up with a patch to disable MLAA without side issues. The patch disables the AA and also fixes the tearing, but introduces big vertex explosions around the map which ruins the experience.

The MLAA disable patch and motion blur fix patch (fixes black replays) are the following:

"Version: 1.2

# Gran Turismo 6 (v1.22) - Illusion Baseline (Safe Working State)

PPU-42367707f4caac2668f10cb46498f64bde9db440:
  "GT6 Disable Anti Aliasing (Exact Illusion Original)":
    Games:
      "Gran Turismo 6":
        BCUS99247: [ All ]
    Author: "illusion"
    Notes: "Original Illusion AA disable patch at 0xED2E88."
    Patch Version: 1.0
    Patch:
      - [ be32, 0x00ED2E88, 0x39E00001 ]

  "GT6 Disable Motion Blur (Exact Illusion Original)":
    Games:
      "Gran Turismo 6":
        BCUS99247: [ All ]
    Author: "illusion"
    Notes: "Original Illusion Motion Blur disable patch at 0x8C2B4C. Fixes black replay screen."
    Patch Version: 1.0
    Patch:
      - [ be32, 0x008C2B4C, 0x38600000 ]
"

- Currently trying to disable MLAA directly in the emulator pipeline without needing patches via a hack, to check if the vertex explosions still occur.

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
