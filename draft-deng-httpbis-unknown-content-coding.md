---
title: "Register a new reserved content coding value"

category: std

docname: draft-deng-httpbis-unknown-content-coding-latest
submissiontype: IETF  # also: "independent", "editorial", "IAB", or "IRTF"
number:
date:
consensus: true
v: 3
# area: AREA
# workgroup: WG Working Group
keyword:
 - content coding
 - unknown

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
`content coding`.

--- middle

# Rationale and proposal

There is a need to [convert](https://github.com/whatwg/fetch/pull/1796) an arbitary
`content encoding` value from a http response to `unknown`,  if the UA(user agent)
doesn't recognize or support the original `content encoding` value. This conversion
requires that the original value cannot be `unknown`.

Therefore, this document proposes a new reserved value `unknown` for the HTTP protocol
parameter. A `content coding` value cannot be `unknown`.

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
