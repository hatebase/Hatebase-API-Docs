# Get Analysis

~~~
https://api.hatebase.org/4-1/get_analysis
~~~

## Description

The /get_analysis endpoint retrieves the assessment initiated with a prior query to the /analyze endpoint. Analysis can take anywhere from a few minutes to a couple hours, depending on the complexity of the content and the volume of traffic at the time of request. Requests auto-expire within 48 hours.

## Input Parameters

<table>
  <tr>
    <td><b>Parameter</b></td>
    <td><b>Example</b></td>
    <td><b><b>Notes</b></b></td>
  </tr>
  <tr>
    <td>token</td>
    <td>ABC123</td>
    <td>Mandatory</td>
  </tr>
  <tr>
    <td>format</td>
    <td>json</td>
    <td>At this time only JSON format is available</td>
  </tr>
  <tr>
    <td>request_id</td>
    <td>aBc123</td>
    <td></td>
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
    <td>complete</td>
    <td>true</td>
    <td>"true" or "false" (if "false", more time is required to analyze)</td>
  </tr>
  <tr>
    <td>result</td>
    <td>true</td>
    <td>"true", "false" or "unknown"</td>
  </tr>
  <tr>
    <td>term</td>
    <td></td>
    <td>Term detected, if any</td>
  </tr>
  <tr>
    <td>hateful_meaning</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>nonhateful_meaning</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>average_offensiveness</td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>language</td>
    <td>ENG</td>
    <td>3-character ISO 639-3 code</td>
  </tr>
  <tr>
    <td>probability</td>
    <td>90</td>
    <td>Percentage likelihood of hate speech context</td>
  </tr>
  <tr>
    <td>explanation</td>
    <td></td>
    <td>Analysis truncated at 255 characters</td>
  </tr>
</table>
