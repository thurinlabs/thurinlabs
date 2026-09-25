# thurinlabs.id

The company site for [Thurin Labs](https://thurinlabs.id): what we build, what we believe, and how to reach us. Also served from ENS at `thurinlabs.eth`.

The product lives at [thurin.id](https://thurin.id) ([thurin-id](https://github.com/thurinlabs/thurin-id)).

## What's here

```
index.html            the page (single file: styles, markup, light/dark switch, ENS-aware links)
privacy/index.html    privacy policy
images/               favicon, share image, background tile
fonts/                the fonts, served from here
.github/workflows/    mirror to Codeberg
```

No build step, no framework, no dependencies, and no third-party scripts. The card on the page is
thurinlabs.eth's card image, drawn by thurin.id's share-card service; showing it asks no one else.

## Run it locally

```bash
python3 -m http.server 8000
# or: npx serve .
```

Then open http://localhost:8000.

## Deploy

Deployed as a static IPFS site. The operator's `deploy.sh` (kept outside this repo) pins the
files of the tagged commit ([Verify a deploy](https://docs.thurin.id/#/guides/verify-deploy)), points nginx at the new CID, and writes the `thurinlabs.eth` contenthash. The
page detects when it is served from ENS (`thurinlabs.eth`, or a gateway such as
`thurinlabs.eth.limo`) and rewrites its Thurin.id links to `id.thurinlabs.eth` with the same
suffix, so a visitor who arrived without DNS is never handed back to it.

## Links

- [Thurin.id](https://thurin.id) — the product
- [Docs](https://docs.thurin.id) · [Roadmap](https://docs.thurin.id/#/roadmap)
- [GitHub](https://github.com/thurinlabs) · [Codeberg](https://codeberg.org/thurinlabs) (mirror)

## License

MIT
