<center><a href='https://hatebase.org'><img src="logo.png" width="300" ></a></center><br />

Please review this README for a general understanding of the API before proceeding into the version-specific documentation. Although this README is intended to be a high-level overview of the API's usage and terms, any specific comments on implementation will always reference the latest version.

# Versions

- [v4.0](current/v4-0/overview.md) **Current**
- [v3.0](archived/v3-0/overview.md) Deprecated
- [v2.0](archived/v2-0/overview.md) Deprecated
- v1.0 Retired

# How It Works

The Hatebase API accepts queries using a two-phase approach: the authentication handshake and then the actual query itself. In either scenario, the system is queried with a version number, an endpoint (which defines the type of information requested) and a payload containing input parameters (sent by POST), and then returns a resultset.

The URL structure for querying the API is as follows:

```
https://api.hatebase.org/1-0/authenticate
```

"1-0" represents the version number, and "authenticate" represents the endpoint. All versions and endpoints will be documented here.

# Authentication Phase

The API is queried with a key which is obtained from your Hatebase account:

```
{
  api_key: ABC123
}
```

The returned data provides the input parameters which were queried, plus a resultset (in this case a session token), plus any warnings and/or errors:


```
{
  datetime: gmt_time,
  key: ABC123,
  format: json,
  result: [
    token: DEF456,
    expires_on: "2018-01-01 12:00:00"
  ]
  errors: [
    [789, "Incorrect key"]
  ]
  warnings:[
    [012, "Unspecified format"]
  ]
}
```

Note that this result set is solely illustrative; a token would never be provided if there were errors, only warnings.

Tokens will expire within one hour of issue.

# Query Phase

The token provided in the authentication phase is used as an input parameter to authenticate phase two: the actual data query. The result set will look something like this:


```
{
  datetime: gmt_time,
  token: DEF456,
  expires_on: "2018-01-01 12:00:00",
  format: json,
  page: 1,
  total_pages: 14,
  result: [
  ]
  errors: [
  ]
  warnings:[
  ]
}
```

Again, this simple result set is solely illustrative; there is no need for empty key-value pairs.

# Daily Rate Limiting

Access to the API is limited by your plan's maximum daily query limit. It is strongly recommended that systems which connect with the API do not do so in user real-time. A safer architecture is to download data asynchronously and store locally for better real-time performance and no redundant data retrieval.

# Error Messages

<table>
  <tr>
  <td><b>Code</b></td>
  <td><b>Message</b></td>
  </tr>
  <tr>
  <td>4347</td>
  <td>Invalid endpoint</td>
  </tr>
  <tr>
  <td>4830</td>
  <td>Invalid key</td>
  </tr>
  <tr>
  <td>2546</td>
  <td>Invalid token</td>
  </tr>
  <tr>
  <td>8344</td>
  <td>Invalid ID</td>
  </tr>
  <tr>
  <td>3765</td>
  <td>You must assign a plan to your account to access the API</td>
  </tr>
  <tr>
  <td>5783</td>
  <td>Expired token; please reauthenticate using your API key</td>
  </tr>
  <tr>
  <td>8752</td>
  <td>The version of the API is now retired; please update your queries to resume accessing the API.</td>
  </tr>
  <tr>
  <td>5074</td>
  <td>Daily query cap exceeded; please review documentation on connecting asynchronously to avoid exceeding limits.</td>
  </tr>
  <tr>
  <td>6859</td>
  <td>It's not you, it's us; something apparently went wrong on our end.</td>
  </tr>
</table>

# Warning Messages

<table>
  <tr>
  <td><b>Code</b></td>
  <td><b>Message</b></td>
  </tr>
  <tr>
  <td>6445</td>
  <td>API version deprecated and approaching retirement; please upgrade to the latest version</td>
  </tr>
  <tr>
  <td>6577</td>
  <td>Daily query cap imminent; please review documentation on connecting asynchronously to avoid exceeding limits.</td>
  </tr>
  <tr>
  <td>9011</td>
  <td>No output format specified, so defaulted to JSON</td>
  </tr>
  <tr>
  <td>3841</td>
  <td>No page number specified, so defaulted to 1</td>
  </tr>
  <tr>
  <td>2201</td>
  <td>An input parameter is invalid, and was therefore ignored</td>
  </tr>
</table>

# Please Contact Us

Although every effort has been made to ensure that this documentation accurately reflects the operation of the API, please advise us if you discover any discrepancies.
