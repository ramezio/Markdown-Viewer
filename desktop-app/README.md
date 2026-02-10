# Markdown Viewer Desktop App Port

This is a desktop app port of [Markdown Viewer](https://github.com/ThisIs-Developer/Markdown-Viewer), see [README](../README.md). It is built using [Neutralinojs](https://github.com/neutralinojs/neutralinojs).

## Development

### Requirements

- [Node.js](https://nodejs.org/)
- [npm](https://www.npmjs.com/)

### Running the app

```bash
npx @neutralinojs/neu@11.7.0 run
```

Hot-reload is enabled by default. You can enable the browser inspector by setting `"enableInspector": true` in `neutralino.config.json`.

For more information, see the [Neutralinojs documentation](https://neutralino.js.org/docs/cli/neu-cli#installation).

### Building the app

Single file executable (embeds everything from the `resources` folder):

```bash
npx @neutralinojs/neu@11.7.0 build --embed-resources
```

Portable ZIP file with application bundle:

```bash
npx @neutralinojs/neu@11.7.0 build --release
```

For more information, see the [Neutralinojs documentation](https://neutralino.js.org/docs/cli/neu-cli#neu-build).

## License

**MIT**.

The desktop version uses [Neutralinojs](https://github.com/neutralinojs/neutralinojs), which is also licensed under the MIT License.

- [Neutralinojs](https://github.com/neutralinojs/neutralinojs): [LICENSE (MIT)](LICENSE)
- [Markdown Viewer & Desktop Port](https://github.com/ThisIs-Developer/Markdown-Viewer): [LICENSE (MIT)](../LICENSE)

## Contributors

[![Contributors](https://contrib.rocks/image?repo=ThisIs-Developer/Markdown-Viewer)](https://github.com/ThisIs-Developer/Markdown-Viewer/graphs/contributors)
