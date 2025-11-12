# Restreamer-UI

The user interface of the Restreamer for the connection to the [datarhei Core](https://github.com/datarhei/core)application.

- React
- Material-UI (MUI)

## Development

### For the Restreamer interface:

```
$ git clone github.com/datarhei/restreamer-ui
$ cd restreamer-ui
$ yarn install
$ npm run start
```

Connect the UI with a [datarhei Core](https://github.com/datarhei/core):
http://localhost:3000?address=http://core-ip:core-port

### To add/fix translations:
Locales are located in `src/locals`
```
$ npm run i18n-extract:clean
$ npm run i18n-compile
```

## License
See the [LICENSE](./LICENSE) file for licensing information.

## Standalone Viewer

A lightweight, login-free viewer is available at `/viewer/index.html` once the UI is built/served. Pass the HLS manifest (and optional metadata) via query parameters:

```
https://your-ui.example.com/viewer/?src=https://your-core/hls/channel/index.m3u8&title=Commencement+Day&description=Auditorium+feed&poster=https://...
```

Supported parameters: `src` (required), `title`, `description`, `poster`, `autoplay=true`, `muted=false`, and `storage` (just for labeling). The page embeds Video.js directly, so it works with any public HLS URL and does not rely on the authenticated UI router.
