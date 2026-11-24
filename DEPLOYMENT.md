# GitHub Pages deployment

The production URL is [RafiurRahman](https://ratul1918.github.io/RafiurRahman/). The [Pages workflow](.github/workflows/pages.yml) builds the site and publishes it on pushes to `main`. It can also be run from the Actions tab.

In repository **Settings → Pages**, the publishing source is **GitHub Actions**. The workflow builds with the `/RafiurRahman/` base path. The CV and bundled assets resolve within that path.

To test a production build locally:

```sh
npm ci
npm run typecheck
npm run build -- --base=/RafiurRahman/
npm run preview
```

Open `/RafiurRahman/` on the preview server and check the homepage, navigation, and CV download.

The homepage specifies its canonical URL and includes profile metadata. The [sitemap](https://ratul1918.github.io/RafiurRahman/sitemap.xml) can be submitted in Google Search Console after verifying the property. Google controls when it indexes the site and how it ranks for a name search.
