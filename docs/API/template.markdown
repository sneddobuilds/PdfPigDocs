---
layout: page
title: Template API
parent: API
nav_order: 3
---

# Template
Template allows you to manage your html templates for pdf generation

## Get Template

| Endpoint        |
|:-------------|
| <span class="label label-blue">Get</span>  /Template/Get/{templateId}          |

| Example        |
|:-------------|
| `https://api.pdfpig.xyz/Template/Get/573d536b-65fc-4e46-ace9-d77dd3ee9b32`          |


### Request
The request should post a json body to the server with the templateId passed in as a query parameter.

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

| Example Response        |
|:-------------|
| 
```
{
    "resultItem": {
        "name": "Joint Account Applications",
        "templateHtml": "<div style=\"font-family: 'Arial',sans-serif; margin-left: 50px; width: 700px;\">\r\n<h2 style=\"margin-bottom: 25px; color: black; font-size: 27px;\">JOINT ACCOUNT</h2>\r\n<p style=\"font-size: 1.2em;\"><strong>Account Purpose:</strong> {{accountpurpose}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Person 1 Full Name:</strong> {{name1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:</strong> {{email1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:</strong> {{phone1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Marital Status:</strong> {{maritalstatus1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>NIF:</strong> {{nif1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Employment Status:</strong> {{jobstatus1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Occupation (former if retired):</strong> {{job1}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Fiscal Number in Country of Residence:</strong> {{fiscalnumber1}}</p>\r\n<div style=\"text-align: center; margin: 40px 0;\">\r\n<p>=================================================================================</p>\r\n</div>\r\n<p style=\"font-size: 1.2em;\"><strong>Person 2 Full Name:</strong> {{name2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Email:</strong> {{email2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Mobile Number:</strong> {{phone2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Marital Status:</strong> {{maritalstatus2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>NIF:</strong> {{nif2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Employment Status:</strong> {{jobstatus2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Occupation (former if retired):</strong> {{job2}}</p>\r\n<p style=\"font-size: 1.2em;\"><strong>Fiscal Number in Country of Residence:</strong> {{fiscalnumber2}}</p>\r\n</div>",
        "id": "a9096bcb-cc5c-4060-980d-9f166c0cb3d2",
        "userId": "e3caf331-dfaa-441c-b5b8-b59463d43edd",
        "createdDate": "2021-07-09T14:45:11.095082",
        "updatedDate": "2021-07-09T14:45:11.094873"
    },
    "success": true,
    "errors": null
}
```          
|


| Response        |
|:-------------|
| ``` // ArrayBuffer ```|

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