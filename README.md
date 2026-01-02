# Hollow Knight: Silksong Modding Docs

This repository contains the source code for all parts of https://docs.silksong-modding.org/ that
are not related to a specific core library. It is intended to contain conceptual content about
modding basics and helpful topics related to the Silksong-specific development flow.

## Contributing guidelines

- It's strongly recommended discuss potential additions to the docs in the
  [#silksong-org-discussion](https://discord.com/channels/879125729936298015/1413054490621378610)
  channel in the Hollow Knight Modding Discord server before spending any effort writing. This will
  help ensure that the content you plan to add is (1) on-topic and (2) organized in line with the
  rest of the content.
- Remember that it not our responsibility to reproduce the entire body of literature about modding
  or development in general. Assume some basic knowledge from the reader and link to additional
  resources when appropriate. In general, we assume the following of readers:
  - The reader should have basic C# knowledge (or the ability read MSDN documentation)
  - The reader can read BepInEx and Harmony documentation to understand advanced use cases in depth
  - The reader may have modded Hollow Knight before, but it's not guaranteed (draw comparisons where
    applicable, but sparingly)

## Local development

### Prerequisites

- .NET SDK - to run docfx
  - Version 10.x recommended
- Node.js - for formatting and JS dev tooling
  - Latest LTS (currently 24.x) recommended
  - Using a version manager like [mise](https://mise.jdx.dev/) is strongly recommended

After setting up SDKs, run `dotnet tool restore` and `npm install` to install dependencies.

### Writing docs

The modding docs are built using [docfx](https://dotnet.github.io/docfx). To build the site, run
`docfx`. To host the local site, run `docfx serve _site`. You can also use the shorthand
`docfx --serve` to build and run the site.

### Formatting

The modding docs use [Prettier](https://prettier.io/) for formatting. There are extensions to
integrate various IDEs, or you can manually run `npm run format`.
[Husky](https://typicode.github.io/husky/) is also configured to automatically format the project as
a pre-commit hook.
