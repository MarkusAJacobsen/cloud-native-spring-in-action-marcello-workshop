# Chapter take away

1. In an OIDC/OAuth2 setup, the Client (Edge Service) is granted access to a Resource Server (Catalog Service and Order Service) on behalf of the user through an Access Token
2. Spring Cloud Gateway provides a TokenRelay filter to add the Access Token to any request routed downstream automatically
3. Following the JWT format, ID Tokens and Access Tokens can propagate relevant information as claims about the authenticated user. For example, you can add a roles claim and configure Spring Security with authorization policies depending on the user role
4. Spring Boot applications can be configured as OAuth2 Resource Servers using Spring Security
5. In an OAuth2 Resource Server, the strategy for authenticating users is entirely based on a valid Access Token provided in the Authorization header for each request. We call it JWT authentication
6. In an OAuth2 Resource Server, security policies are still enforced through a SecurityFilterChain (imperative) or SecurityWebFilterChain (reactive) bean
7. Spring Security represents permissions, roles, and scopes as GrantedAuthority objects
8. You can provide a custom JwtAuthenticationConverter bean to define how to extract granted authorities from a JWT, for example using the roles claim
9. Granted authorities can be used to adopt an RBAC strategy and protect endpoints, depending on the user role
10. The Spring Data libraries support auditing to track who created an entity and who updated it last. You can enable this feature in both Spring Data JDBC and Spring Data R2DBC by configuring an AuditorAware (or ReactiveAuditAware) bean to return the username of the currently authenticated user
11. When data auditing is enabled, you can use the @CreatedBy and @LastModifiedBy annotations to automatically inject the right values when a create or update operation occurs
12. Testing security is challenging, but Spring Security provides convenient utilities to make that easier, including expressions that mutate HTTP requests to include a JWT Access Token (.with(jwt()) or .mutateWith(mockJWT())) or to run a test case in a specific security context for a given user (@WithMockUser)
13. Testcontainers can help write full integration tests by using an actual Keycloak container to verify the interactions with Spring Security