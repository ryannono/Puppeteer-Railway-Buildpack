# puppeteer-railway-buildpack

(Note: This is a Railway adapted version of [Jon Tewksbury's heroku build pack](https://github.com/jontewks/puppeteer-heroku-buildpack/blob/main/README.md))

Installs dependencies needed in order to run [puppeteer](https://github.com/puppeteer/puppeteer) on [railway](https://railway.app). Be sure to include `{ args: ['--no-sandbox', '--disable-setuid-sandbox'] }` and `ignoreDefaultArgs: ['--disable-extensions']` in your call to `puppeteer.launch`.

Puppeteer defaults to `headless: true` in `puppeteer.launch` and this shouldn't be changed. Railway doesn't have a GUI to show you chrome when running `headless: false` and will throw an error.

## Usage

To use add the `nixpacks.toml` file to your root directory before deploying.

This will make the railway nixpacks builder instal the needed chrome dependencies listed here:

| Package | Size (mb) |
| ------- | ---- |
| `fonts-liberation` | 2.1 |
| `libappindicator3-1` | 55.2 |
| `libasound2` | 2.4 |
| `libatk-bridge2.0-0` | 3.9 |
| `libatk1.0-0` | 0.2 |
| `libgbm1` | 0.4 |
| `libgtk-3-0` | 54.8 |
| `libnspr4` | 0.3 |
| `libnss3` | 4.2 |
| `libx11-xcb1` | 0.1 |
| `libxcomposite1` | 0.03 |
| `libxcursor1` | 0.1 |
| `libxdamage1` | 0.03 |
| `libxfixes3` | 0.05 |
| `libxi6` | 0.1 |
| `libxrandr2` | 0.07 |
| `libxss1` | 0.03 |
| `libxtst6` | 0.05 |
| `xdg-utils` | 344 😱 |
