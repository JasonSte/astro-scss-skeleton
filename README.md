# Astro SCSS Skeleton with Dark Mode support

## Project Structure

Standard Astro structure, but SCSS files are split into sub folders. Uses typescript, which is setup to use path alias's for simplicity

### To use this skeleton:

- Clone the git. Delete the `.git` folder then run `git init` to create the git at initial state
- Edit `astro.config.mjs' to contain the correct site url for the project.
- Change the project name in package.json
- Run `pnpm install` or `npm install` to download the required modules

### Styles structure

```
├
├── styles/
│ ├── base/
│ │ └── \_colors.scss
| | └── \_fonts.scss
| | └── \_main.scss
| | └── \_variables.scss
| | └── global.scss
│ ├── components
│ │ └── \_header.scss
| | └── \_themeSwitch.scss
│ └── layout
|
```

\_main.scss contains the imports for the colors, fonts and variables files so to reference any of those, in a component/layout scss file, import \_main.scss. Global declarations are to be put in global.scss which is imported in the basehead.astro file, which should be fine to be used in any layout.

Contains a dark / light mode. This is powered via the \_colors.scss, along with script definitions in the ThemeInitial.astro and ThemeSwitch is a button to switch the theme. If not using the button remove the entries for localstorage in ThemeInitial

## 🧞 Commands

All commands are run from the root of the project, from a terminal. Use either `npm` or `pnpm`, advisable to use `pnpm`:

| Command                    | Action                                                    |
| :------------------------- | :-------------------------------------------------------- |
| `pnpm install`             | Installs dependencies                                     |
| `pnpm run dev`             | Starts local dev server at `localhost:3000`               |
| `pnpm run build`           | Build your production site to `./dist/`                   |
| `pnpm run preview`         | Preview your build locally, before deploying              |
| `pnpm run astro ...`       | Run CLI commands like `astro add`, `astro check`          |
| `pnpm run astro -- --help` | Get help using the Astro CLI                              |
| `pnpm run publish          | Publishes the built verion on Cloudflare Pages, if needed |
