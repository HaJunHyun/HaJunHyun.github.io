# HaJunHyun.github.io

Personal academic website built from the official [al-folio](https://github.com/alshedivat/al-folio) starter.

The original al-folio design, theme runtime, and pinned dependencies are preserved. Only personal configuration and content have been changed.

- Target URL: <https://hajunhyun.github.io/>
- Target repository: `HaJunHyun/HaJunHyun.github.io`
- Upstream commit: `40c06007dab344970b681ba63b2241b1a8209ec1`
- Setup and editing guide (Korean): [docs/HAJUN_SETUP.md](docs/HAJUN_SETUP.md)
- Official installation guide: [docs/QUICKSTART.md](docs/QUICKSTART.md)

## Content

- `_pages/about.md`: introduction and profile
- `_data/socials.yml`: verified contact links
- `_projects/`: public GitHub projects
- `_bibliography/papers.bib`: publications, currently empty
- `_drafts/research-note.md`: an unpublished Distill-style writing template
- `_posts/`: create this folder when publishing the first post

No affiliation, email address, CV, or publications have been invented. The profile image is the public GitHub avatar.

## Build

```sh
bundle install
npm ci
bundle exec jekyll build
bundle exec jekyll serve
```

Use the empty `baseurl` already set in `_config.yml` for this personal site. The official GitHub Actions deployment workflow builds the site and publishes the output to the `gh-pages` branch.

## License

al-folio is distributed under the MIT License. See [LICENSE](LICENSE).
