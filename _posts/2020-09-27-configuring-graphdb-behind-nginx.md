---
title: "Configuring GraphDB behind an Nginx proxy"
categories: [Programming]
layout: post
---

[GraphDB](http://graphdb.ontotext.com/) is a solid semantic graph database that includes both free and paid versions. The free version has a lot of capability and is easy to use.

In this post, we look at how to configure GraphDB behind an [nginx](https://www.nginx.com/) proxy so that it can live at a specific URL.

By default, GraphDB runs at:
```
http://localhost:7200
```

With the proxy settings, we'll set it run run at:
```
http://localhost:8080/graphdb/
```

## Configuring Nginx
First, install **nginx** for your platform, and run it. Test your **nginx** installation by visiting:
```
http://localhost:8080/
```

You should see a test page that says _**"Welcome to Nginx!"**_

Next, open the **`nginx.conf`** and modify the default config to include a **location** for GraphDB:
```
    server {
        listen       8080;
        server_name  localhost;

        #charset koi8-r;

        #access_log  logs/host.access.log  main;

        location / {
            root   html;
            index  index.html index.htm;
        }

        location /graphdb/ {
                proxy_pass http://127.0.0.1:7200/;
        }

        #error_page  404              /404.html;
```

**NOTE:** Be sure to add that trailing slash after the `proxy_pass` address. In my first attempt, I left this off and it did not work. After adding the trailing slash, I was in business.

Finally tell **nginx** to reload the config. On MacOS, you do this with:
```
nginx -s reload
```

## Configuring GraphDB
If you try to load GraphDB right away by visiting
```
http://localhost:8080/graphdb
```

Then you'll see the page partially load, but none of the assets will load. We need to tell GraphDB that it's available under a different URL than it expects, so that it will load the assets correctly.

Use the guide [Configuring GraphDB](http://graphdb.ontotext.com/documentation/free/quick-start-guide.html#configuring-graphdb) to learn how to bring up the settings window.

Once there, add an entry with:
* **property name**: `graphdb.workbench.external-url`
* **property value**: `http://localhost:8080/graphdb`

Then hit **Save and restart**.

Wait about a minute for everything to spin up again, and access your relocated GraphDB at its new home:
```
http://localhost:8080/graphdb/
```

# References
1. [nginx reverse proxy](https://docs.nginx.com/nginx/admin-guide/web-server/reverse-proxy/#pass): This tells us how to add a new `location` to the nginx config
2. [controlling nginx](https://docs.nginx.com/nginx/admin-guide/basic-functionality/runtime-control/#:~:text=To%20reload%20your%20configuration%2C%20you,)%20with%20the%20%2Ds%20argument.&text=where%20can%20be%20one,quit%20%E2%80%93%20Shut%20down%20gracefully): This tells us how to start, stop, and reload nginx
3. Stack Overflow [Run GraphDB behind Apache Proxy](https://stackoverflow.com/a/61651318): This breadcrumb led me to the right GraphDB configuration property to change
4. GraphDB [list of configuration properties](http://graphdb.ontotext.com/documentation/standard/configuring-graphdb.html#list-of-configuration-properties): The full list of configuration properties for GraphDB
5. [Configuring GraphDB](http://graphdb.ontotext.com/documentation/free/quick-start-guide.html#configuring-graphdb): Shows how to access the dialog box you can use to add properties.
