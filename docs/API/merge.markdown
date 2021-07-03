---
layout: page
title: Merge API
parent: API
nav_order: 1
---

# Merge
Merge allows you to post a zip of pdfs and images to be merged together and compressed.


| Endpoint        |
|:-------------|
| <span class="label label-green">Post</span>  /Combine/Process          |


## Request
The request should post a form to the server, the form should consist of the following fields:

<table>
<thead>
  <tr>
    <th>Name</th>
    <th>Type</th>
    <th>Required</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>zip</td>
    <td>File</td>
    <td>True</td>
  </tr>
  <tr>
    <td colspan="3">The zip file to be processed</td>
  </tr>
</tbody>
</table>

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