---
title: "Register a new reserved content coding value"

category: std

docname: draft-deng-register-a-reserved-content-coding-value-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
# area: AREA
# workgroup: WG Working Group
keyword:
 - - content coding
 - - unknown
venue:
#  group: WG
#  type: Working Group
#  mail: WG@example.com
#  arch: https://example.com/WG
  github: "guohuideng2024/register_unknown_cc"
  latest: "https://guohuideng2024.github.io/register_unknown_cc/draft-deng-register-a-reserved-content-coding-value.html"

author:
 -
    fullname: "Guohui Deng"
    organization: Microsoft
    email: "guohuideng@microsoft.com"

normative:

--- abstract

This document proposes a new reserved value `unknown` for the HTTP protocol parameter
`content coding`. With this value reserved, when the UA(user agent) doesn't recognize
or suppoprt a `content encoding` value from a http response, it exposes
`content encoding` value in `PerformanceResourceTiming` API as `unknown`.

--- middle

# Introduction

A new field `contentEncoding` is [proposed](https://github.com/whatwg/fetch/pull/1796)
to be added to [PerformanceResourceTiming](https://www.w3.org/TR/resource-timing/).
This field explicitly exposes the `content encoding` value in the http response that
delivered the resource.  This value is beneficial to web sites' and CDNs' content
delivery optimization, analytics and debugging.

To ensure that the `contentEncoding` in `PerformanceResourceTiming` doesn't become a side
channel, all arbitary values that are not recognized or supported are converted to
`unknown` before exposed in `PerformanceResourceTiming`. This conversion requires that the
original value cannot be `unknown`.

# Proposal

Register a new reserved value `unknown` for the HPPT parameter `content coding`.
A `content coding` value cannot be `unknown`.

# Conventions and Definitions

{::boilerplate bcp14-tagged}


# Security Considerations

No security concerns.

# IANA Considerations

IANA maintains a [HTTP Content Coding Registry](https://www.iana.org/assignments/http-parameters/http-parameters.xhtml).
If this proposal becomes a standard, a new reserved value `unknown` will be added to the registry.

--- back

# Acknowledgments
{:numbered="false"}

Many thanks to Noam Rosenthal, Anne van Kesteren, Yoav Weiss, Patrick Meenan, Nic Jansma,
and Lucas Pardue for the discussion and guidance.
