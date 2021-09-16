# static.atestpage.com
Experiments with Cloudflare worker sites

This is the repo for the Cloudflare Worker of https://static.atestpage.com

This site was generated using the [worker-sites template](https://github.com/cloudflare/worker-sites-template) as [shown here](https://developers.cloudflare.com/workers/get-started/quickstarts)

```
wrangler generate my-app https://github.com/cloudflare/worker-sites-template
```

Since this is a site that's been created from scratch, I just used the Bootstrap [Starter Template](https://getbootstrap.com/docs/5.1/examples/starter-template/) and built this page. 

# wrangler.toml 
I modified the wrangler.toml file doing the following.. 

1. added a ```route = "https://static.atestpage.com/" ```
1. Set my account_id and zone_id 
1. changed workers_dev to false, this prevents it from building my-app.atestpage.workers.dev


## Changes to wrangler.toml 


