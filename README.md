# SEO Indexing Tools

This repository contains SEO indexing tools, easing indexing of my websites on search engines. They're written in Bash, Node.js and Ruby but can be directly executed on any Unix-like system if the required runtime is installed.

## URL from sitemap

This Ruby script takes a sitemap URL as input and outputs a list of URLs found in it.

### Usage

```bash
./url_from_sitemap https://example.com/sitemap.xml > Bing/urls.txt
```

## Bing IndexNow

To get indexed on Bing, you can use the IndexNow API. You'll find two Bash scripts to send a URL or a batch of them from a `urls.txt` file. You'll need to [get an API key](https://www.bing.com/indexnow/getstarted#implementation) and host a key file at the root of your website.

### Usage

```bash
export BING_INDEXNOW_KEY=YOUR_API_KEY
./indexnow.sh https://example.com/page.html

export INDEXNOW_DOMAIN=example.com
./indexnow_batch.sh urls.txt
```

## Google Indexing API

To get indexed on Google, you can use the [Indexing API](https://developers.google.com/search/apis/indexing-api/v3/quickstart). To use it you'll need a Google Cloud Service account declared as proprietary of your domain property in [Search Console](https://search.google.com/search-console/index) and to store its corresponding key in `service_account.json` file. This Node.JS script allows you to send a URL to the Indexing API.

### Usage

```bash
./gindex https://example.com/page.html
```

## License

This repository is under the [MIT License](LICENSE).
