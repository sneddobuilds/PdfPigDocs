---
layout: page
title: Generate API
parent: API
nav_order: 3
---

# Generate
Generate allows you to post json data to a html template and have it generate a PDF.


| Endpoint        |
|:-------------|
| <span class="label label-green">Post</span>  /Generate/Create/{templateId}          |


## Request
The request should post a json body to the server with the templateId passed in as a query parameter.

Ensure that you set the content-type header as follows:

```
Content-Type: multipart/form-data
```

## Response
Returns a pdf file.

| Response        |
|:-------------|
| ``` // ArrayBuffer ```|

### Errors

|  Response code |  Description |
|:--|:--|
|  400 |  Bad Request -- Your request is invalid. |
|:--|:--|
|  401 |  Unauthorized -- Your API key is wrong. |
|:--|:--|
|  404 |  Not Found -- The specified request could not be found. |
|:--|:--|
|  500 |  Internal Server Error -- We had a problem with our server. Try again later. |
|:--|:--|
|  503 |  Service Unavailable -- We're temporarily offline for maintenance. Please try again later. |