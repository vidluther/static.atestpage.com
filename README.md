# Earthbound Misfit Demo 

The demo for [Earthbound Misfit](https://github.com/vidluther/earthbound-misift) resides at https://atestpage.com. This is done by telling hugo to publish the demo site into the ./ebmisfit-public/ folder , and then publishing that folder by issuing the following command.

```
 hugo -d ~/work/atestpage.com/ebmisfit-public --minify
 cd ~/work/atestpage.com
 wrangler publish --env ebmisfit
```

# static.atestpage.com
Experiments with Cloudflare worker sites

This is the repo for the Cloudflare Worker of https://static.atestpage.com

This site was generated using the [worker-sites template](https://github.com/cloudflare/worker-sites-template) as [shown here](https://developers.cloudflare.com/workers/get-started/quickstarts)

```
wrangler generate my-app https://github.com/cloudflare/worker-sites-template
```

Since this is a site that's been created from scratch, I just used the Bootstrap [Starter Template](https://getbootstrap.com/docs/5.1/examples/starter-template/) and built this page. 

