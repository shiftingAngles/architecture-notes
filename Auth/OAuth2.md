See e.g. Auth0 for guidance

# OAuth2 SSO Auth Code Flow with PKCE
User navigates to static SPA. Gets redirected to Auth provider /auth endpoint. At Auth provider, user consents to permission scope. User gets redirected to provided URL with authentication code in query parameter. SPA can then exchange the authentication code for a token at the /token endpoint. 

## attack surface:
* token in frontend can be extracted via xss attack.

## mitigation:
* token is written to js memory -> needs to be requested after every page refresh again
* BFF flow