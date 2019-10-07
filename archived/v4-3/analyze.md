# Analyze

~~~
https://api.hatebase.org/4-3/analyze
~~~

## Description

The /analyze endpoint allows users to submit a custom piece of content for analysis by HateBrain, the natural language parsing engine at the heard of Hatebase. Submitting content through this endpoint returns a request_id which can then be used with the /get_analysis endpoint to see the results of HateBrain's assessment. Analysis can take anywhere from a few minutes to a couple hours, depending on the complexity of the content and the volume of traffic at the time of request. Requests auto-expire within 48 hours.

Note that the /analyze endpoint is intended for use with short user posts, as in a chat session. Posts of greater than 3,000 characters will be truncated. A minimum length of 50 characters is also recommended (although posts as short as 25 characters will be accepted), because language detection is unreliable with extremely short pieces of content.

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
    <td>content</td>
    <td></td>
    <td>Must be between 25 and 3,000 characters</td>
  </tr>
  <tr>
    <td>language</td>
    <td>ENG</td>
    <td>3-character ISO 639-3 code. Please provide if known, since this increases the accuracy of the analysis.</td>
  </tr>
  <tr>
    <td>country</td>
    <td>CA</td>
    <td>2-character ISO 3166-2 code. Please provide if known, since this increases the accuracy of the analysis.</td>
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
    <td>request_id</td>
    <td>ABC123</td>
    <td>Can be used when querying /get_analysis</td>
  </tr>
  <tr>
    <td>expires_on</td>
    <td>2018-01-01 13:00:00</td>
    <td>GMT</td>
  </tr>
</table>
