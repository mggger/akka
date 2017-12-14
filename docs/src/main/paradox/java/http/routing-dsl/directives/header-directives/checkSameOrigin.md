# checkSameOrigin

## Description

Checks that request comes from the same origin. Extracts the @unidoc[Origin] header value and verifies that allowed range
contains the obtained value. In the case of absent of the @unidoc[Origin] header rejects with a @unidoc[MissingHeaderRejection].
If the origin value is not in the allowed range rejects with an `InvalidOriginHeaderRejection`
and `StatusCodes.FORBIDDEN` status.

## Example

Checking the @unidoc[Origin] header:

@@snip [HeaderDirectivesExamplesTest.java]($test$/java/docs/http/javadsl/server/directives/HeaderDirectivesExamplesTest.java) { #checkSameOrigin }