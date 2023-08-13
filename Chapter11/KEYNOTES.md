# Chapter take away

1. Access control systems require identification (who are you?), authentication (can you prove it's really you?), and authorization (what are you allowed to do?)
2. A common strategy for implementing authentication and authorization in cloud native application is based on JWT as the data format, OAuth2 as the authorization framework, and OpenID Connect as the authentication protocol
3. When using OIDC authentication, a Client application initiates the flow and delegates an Authorization Server for the actual authentication. Then the Authorization Server issues an ID Token to the client
4. The ID Token includes information about the user authentication
5. Keycloak is an identity and access management solution that supports OAuth2 and OpenID Connect and can be used as an Authorization Server
6. Spring Security provides native support for OAuth2 and OpenID Connect and you can use it to turn Spring Boot applications into OAuth2 clients
7. In Spring Security, you can configure both authentication and authorization in a SecurityWebFilterChain bean. To enable the OIDC authentication flow, you can use the oauth2Login() DSL
8. By default, Spring Security exposes a /logout endpoint for logging a user out
9. In an OIDC/OAuth2 context we also need to propagate the logout request to the Authorization Server (such as Keycloak) to log the user out of there. We can do that via the RP-Initiated Logout flow supported by Spring Security via the OidcClientInitiatedServerLogoutSuccessHandler class
10. When a secure Spring Boot application is the backend for an SPA, we need to configure CSRF protection through cookies and implement an authentication entry point that returns an HTTP 401 response when a request is not authenticated (as opposed to the default HTTP 302 response redirecting to the Authorization Server Automatically)
11. The Spring Security Test dependency supplies several convenient utilities for testing security
12. The WebTestClient bean can be enhanced by mutating its requests context through a particular configuration for OIDC login and CSRF protection