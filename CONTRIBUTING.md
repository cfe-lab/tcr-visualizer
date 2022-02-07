This is a Django app deployed on the server with some other Django apps.

## Deploying a Release
You need to connect to the server from inside the lab network. You can find the
internal IP address in the `servers.md` file in the `dev-docs` repository. If
you don't already have an account on the server, ask the lab director for
access.

The source code is deployed with a Git clone at
`/alldata/bblab_site/tools/tcr_visualization`. To deploy an update, change to that
directory, and then run `sudo git pull`. 

Note that the contents of `static/` should go in `/alldata/bblab_site/static/`. 
This includes `tcr_vis_style.css` and `tcr_vis.js`.

Then restart the Apache server with
`sudo systemctl restart httpd`

## Note: D3.js
This tools uses [`D3.js v5.16.0`]. 

`D3.js` is now `>v7.0` which includes some breaking changes.

[`D3.js v5.16.0`]: https://d3js.org/d3.v5.min.js