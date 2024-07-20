# data.scratchaddons.com

This is the data configuration repository for Scratch Addons extension clients.

Configuration files are supported by the extension since Scratch Addons v1.39.0 (August 2024).

The `data.scratchaddons.com` subdomain is hosted by GitHub Pages, and is not proxied through Cloudflare.

## Files

### `version.json`

This file is fetched regularly by the extension. It contains a version number that should be incremented each time `data.json` is modified.

If the extension discovers this number was incremented, `data.json` will be fetched.

```json
{"v":4}
```

### `data.json`

This file contains the main configuration data.

### Supported fields

#### `minVersion` string
Specifies the minimum extension version that can be used. If the client detects that its version is below this minimum version, it will automatically disable itself.

#### `disabledVersions` string[]
A list of extension versions that are manually disabled, even if they are newer than the `minVersion`.

## Updating configuration

To update the configuration:

1. Modify the `data.json` file as needed.
2. Increment the version number in `version.json` by one.
3. The updated files will be automatically deployed to the `data.scratchaddons.com` subdomain.
