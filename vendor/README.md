# vendor/

`identity-kit-embed.js` is `dist/embed.global.js` from `@thurinlabs/identity-kit`, copied in so
the page loads no third-party script (the live card at thurinlabs.id).

| file | from | sha256 |
|---|---|---|
| identity-kit-embed.js | `@thurinlabs/identity-kit@1.3.5` (npm), `dist/embed.global.js` | `0bd2522188eddd51d6b7f7ca1a59c98d296dbe664bf5304c37b20913851710cd` |

To update after a kit release, take the file from the published npm tarball and check it:

```bash
npm pack @thurinlabs/identity-kit@<version> && tar -xzf thurinlabs-identity-kit-<version>.tgz
cp package/dist/embed.global.js vendor/identity-kit-embed.js && sha256sum vendor/identity-kit-embed.js
rm -rf package thurinlabs-identity-kit-<version>.tgz
```

Then update the row above (version + sha256).
