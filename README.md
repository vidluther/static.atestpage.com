# static.atestpage.com

This is a simple demo of cloudflare worker sites. It can be viewed at https://static.atestpage.com/

The files for this were hand edited using VS Code, there aren't any fancy SSGs or anything here. 

## Steps to Publish
Keep in mind, this guide is to show you how to publish a static site in a "production environment" at Cloudflare, and to attach a domain to it.
I'm not going to get into how you get the domain configured in Cloudflare.. it's pretty simple.

### Create a new workspace
First create a new project/space that you want to build. 

```bash
wrangler generate static.atestpage.com https://github.com/cloudflare/worker-sites-template
```

### Make sure you've configured wrangler.toml 

```toml
account_id = "go.to.dash.cloudflare.com.to.get.this"
name = "static-dot-atestpage-com
type = "webpack"
zone_id = "this.is.also.on.dash.cloudflare.com"
workers_dev = false
compatibility_date = "2021-12-30"

## This is where you tell it what hostname to attach once you publish
route = "https://static.atestpage.com/*"
site = { bucket = "./public" }
```

### Edit the code etc.
You can edit the HTML in the public/ folder, this is a static site.. so basic html/css rules apply. 
You could use webpack..etc..just make sure that it publishes to the public/ folder. I just used bootstrap 5.1

```
 cd work/static.atestpage.com/
 code public
```

### Publish the code to Cloudflare Worker Sites

```
wrangler publish


<!-- ```

 hugo -d ~/work/atestpage.com/ebmisfit-public --minify
 cd ~/work/atestpage.com
 wrangler publish --env ebmisfit
``` -->


This is the repo for the Cloudflare Worker of https://static.atestpage.com

This site was generated using the [worker-sites template](https://github.com/cloudflare/worker-sites-template) as [shown here](https://developers.cloudflare.com/workers/get-started/quickstarts)