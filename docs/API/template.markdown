---
layout: page
title: Template API
parent: API
nav_order: 3
---

# Template
Template allows you to manage your html templates for pdf generation

## Template engine
The template engine is based on liquid, so you can make use of liquid functions within your templates - [see here](https://shopify.github.io/liquid/basics/introduction/).  

___

## Get Template

| Endpoint        |
|:-------------|
| <span class="label label-blue">Get</span>  /Template/Get/{templateId}          |

| Example        |
|:-------------|
| `https://api.pdfpig.xyz/Template/Get/573d536b-65fc-4e46-ace9-d77dd3ee9b32`          |


### Request
The required request options are as follows: 

#### Options
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


#### Request Parameters

`{templateId}` is mandatory and can be obtained via the template endpoint

### Response
Returns Json representing the result.


#### Example Response


```json
{
    "resultItem": {
        "name": "Template name",
        "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">My Document template<\/h2>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Name:<\/strong> {{name1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:<\/strong> {{email1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:<\/strong> {{phone1}}<\/p>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<h3>Orders:<\/h3>\r\n<table>\r\n{% for order in orders %}\r\n  <tr>\r\n<td>\r\n{{ order.id }}\r\n<\/td>\r\n<td>\r\n{{ order.cost }}\r\n<\/td>\r\n<\/tr>\r\n{% endfor %}\r\n<\/table>\r\n<\/div>",
        "id": "e3ctt331-dfaa-441t-b5b8-b59463d43etr",
        "userId": "e3ctt331-dfaa-441t-b5b8-b59463d43ett",
        "createdDate": "2021-07-09T14:45:11.095082",
        "updatedDate": "2021-07-09T14:45:11.094873"
    },
    "success": true,
    "errors": null
}
```

___

## Get Templates (Paged)

| Endpoint        |
|:-------------|
| <span class="label label-blue">Get</span>  /Template/GetPaged/{pageNumber}/pageSize          |

| Example        |
|:-------------|
| `https://api.pdfpig.xyz/Template/GetPaged/1/10`          |


### Request
The request options are as follows:

#### Options
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
    <td>Query Param</td>
    <td>{pageNumber}</td>
    <td>True</td>
  </tr>
  <tr>
    <td>Query Param</td>
    <td>{pageSize}</td>
    <td>True</td>
  </tr>
  <tr>
    <td>Header</td>
    <td>Content-Type: application/json</td>
    <td>True</td>
  </tr>
</tbody>
</table>

### Response
Returns Json representing the result.

<table>
<thead>
  <tr>
<th>Example Response</th>
</tr>
</thead>
<tbody>
<tr>
    <td>
```
{
    "resultItem": {
        "results": [
            {
                "name": "Template name",
                "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">My Document template<\/h2>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Name:<\/strong> {{name1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:<\/strong> {{email1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:<\/strong> {{phone1}}<\/p>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n  <h3>Orders:<\/h3>\r\n  <table>\r\n {% for order in orders %}\r\n  <tr>\r\n    <td>\r\n    {{ order.id }}\r\n    <\/td>\r\n    <td>\r\n      {{ order.cost }}\r\n    <\/td>\r\n    <\/tr>\r\n{% endfor %}\r\n<\/table>\r\n<\/div>",
                "id": "e3ctt331-dfaa-441t-b5b8-b59463d43etr",
                "userId": "e3ctt331-dfaa-441t-b5b8-b59463d43ett",
                "createdDate": "2021-07-09T14:45:11.095082",
                "updatedDate": "2021-07-09T14:45:11.094873"
            },
            {
                "name": "Another Template name",
                "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">My Document template<\/h2>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Name:<\/strong> {{name1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:<\/strong> {{email1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:<\/strong> {{phone1}}<\/p>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n  <h3>Orders:<\/h3>\r\n  <table>\r\n {% for order in orders %}\r\n  <tr>\r\n    <td>\r\n    {{ order.id }}\r\n    <\/td>\r\n    <td>\r\n      {{ order.cost }}\r\n    <\/td>\r\n    <\/tr>\r\n{% endfor %}\r\n<\/table>\r\n<\/div>",
                "id": "e3ctt331-dfaa-441t-b5b8-b59463d43etq",
                "userId": "e3ctt331-dfaa-441t-b5b8-b59463d43ett",
                "createdDate": "2021-07-08T14:45:11.095082",
                "updatedDate": "2021-07-08T14:45:11.094873"
            }
        ],
        "currentPage": 1,
        "pageCount": 1,
        "pageSize": 10,
        "rowCount": 2,
        "firstRowOnPage": 1,
        "lastRowOnPage": 2
    },
    "success": true,
    "errors": null
}
```          
</td>
</tr>
</table>

## Create Template

| Endpoint        |
|:-------------|
| <span class="label label-green">Post</span>  /Template/Create          |

| Example        |
|:-------------|
| `https://api.pdfpig.xyz/Template/Create`          |


### Request
The required request options are as follows: 

#### Options
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
    <td>Header</td>
    <td>Content-Type: application/json</td>
    <td>True</td>
  </tr>
</tbody>
</table>

<table>
<thead>
  <tr>
<th>Example Request Body</th>
</tr>
</thead>
<tbody>
<tr>
    <td>
```
{
    "name": "Template name",
    "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">My Document template<\/h2>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Name:<\/strong> {{name1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:<\/strong> {{email1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:<\/strong> {{phone1}}<\/p>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n  <h3>Orders:<\/h3>\r\n  <table>\r\n {% for order in orders %}\r\n  <tr>\r\n    <td>\r\n    {{ order.id }}\r\n    <\/td>\r\n    <td>\r\n      {{ order.cost }}\r\n    <\/td>\r\n    <\/tr>\r\n{% endfor %}\r\n<\/table>\r\n<\/div>"
}
```          
</td>
</tr>
</table>


### Response
Returns Json representing the result.

<table>
<thead>
  <tr>
<th>Example Response</th>
</tr>
</thead>
<tbody>
<tr>
    <td>
```
{
    "resultItem": {
        "name": "Template name",
        "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">My Document template<\/h2>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Name:<\/strong> {{name1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:<\/strong> {{email1}}<\/p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:<\/strong> {{phone1}}<\/p>\r\n<p style=\"font-size: 1.2em;\">&nbsp;<\/p>\r\n  <h3>Orders:<\/h3>\r\n  <table>\r\n {% for order in orders %}\r\n  <tr>\r\n    <td>\r\n    {{ order.id }}\r\n    <\/td>\r\n    <td>\r\n      {{ order.cost }}\r\n    <\/td>\r\n    <\/tr>\r\n{% endfor %}\r\n<\/table>\r\n<\/div>",
        "id": "e3ctt331-dfaa-441t-b5b8-b59463d43etr",
        "userId": "e3ctt331-dfaa-441t-b5b8-b59463d43ett",
        "createdDate": "2021-07-09T14:45:11.095082",
        "updatedDate": "2021-07-09T14:45:11.094873"
    },
    "success": true,
    "errors": null
}
```          
</td>
</tr>
</table>


___


## Errors

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