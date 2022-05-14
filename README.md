# pa11y-nuxt

_Work in progress_ 👨‍🔧

Integrate [pa11y](https://pa11y.org/) as [serverMiddleware](https://nuxtjs.org/docs/configuration-glossary/configuration-servermiddleware/#custom-api-endpoint) in NuxtJS.

Demo: https://pa11y-nuxt.onrender.com/
_(Runs on free plan on [render](https://render.com), can be offline if my account limit is reached)_

Checkout https://github.com/mandrasch/pa11y-express as well.

## Host on render.com

Just create a new WebService on [render.com](https://render.com) and configure the project as seen here:

![Screenshot render.com Select a Github Repository](/_gh_screenshots/screenshot_render_001.png)
![Screenshot render.com Configure build and start command](/_gh_screenshots/screenshot_render_002.png)
![Screenshot render.com Dashboard of project with public url](/_gh_screenshots/screenshot_render_003.png)

## Build Setup

```bash
# install dependencies
$ npm install

# serve with hot reload at localhost:3000
$ npm run dev

# build for production and launch server
$ npm run build
$ npm run start
```

For detailed explanation on how things work, check out the [NuxtJS documentation](https://nuxtjs.org).
