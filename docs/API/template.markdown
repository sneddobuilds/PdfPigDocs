---
layout: page
title: Template API
parent: API
nav_order: 3
---

# Template
Template allows you to manage your html templates for pdf generation


| Endpoint        |
|:-------------|
| <span class="label label-blue">Get</span>  /Template/Get/{templateId}          |


## Request
The request should post a json body to the server with the templateId passed in as a query parameter.

### Options
<table>
<thead>
  <tr>
    <th>Option</th>
    <th>Description</th>
    <th>Required</th>
  </tr>
</thead>
<tbody>
  <tr>
    <td>Body</td>
    <td>{JSONDATA}</td>
    <td>True</td>
  </tr>
  <tr>
    <td>Query Param</td>
    <td>{templateId}</td>
    <td>True</td>
  </tr>
  <tr>
    <td>Header</td>
    <td>Content-Type: application/json</td>
    <td>True</td>
  </tr>
</tbody>
</table>


### Request Parameters

`{templateId}` is mandatory and can be obtained via the template endpoint

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