# Authenticate

~~~
https://api.hatebase.org/4-3/authenticate
~~~

## Description

The /authenticate endpoint is required to initiate an API session, and outputs a session token which is used for additional queries over the span of an hour. Once a session token has expired, a new one must be requested by using the /authenticate endpoint.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>api_key</td>
    <td>ABC123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>At this time only JSON format is available</td>
  </tr>
</table>

## Resultset

<table>
  <tr>
    <td><b>Field</b></td>
    <td><b>Value</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td></td>
  </tr>
  <tr>
    <td>requested_on</td>
    <td>2018-01-01 12:00:00</td>
    <td>GMT</td>
  </tr>
  <tr>
    <td>expires_on</td>
    <td>2018-01-01 13:00:00</td>
    <td>GMT</td>
  </tr>
</table>
