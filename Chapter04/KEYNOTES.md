# Chapter take away

1. The Spring Environment abstraction provides a unified interface for accessing properties and profiles
2. Properties are key/value pairs used to store configuration
3. Profiles are logical groups of beans registered only when a specific profile is active
4. Spring Boot collect properties from different sources according to precedence rules.
   5. Command-line arguments
   6. JVM system variables
   7. OS environment variables
   8. profile-specific property files
   9. generic property files
10. Spring beans can access properties from the Environment object by injecting the value with the @Value annotation, or from a bean mapped to a set of properties with the @ConfigurationProperties annotation
11. The @Profile annotation marks beans or configuration classes to be considered only when the specified profile is active
12. A configuration server handles aspects like secret encryption, configuration traceability, versioning, and context refreshing at runtime with no restart
13. The configuration itself can be stored according to different strategies, such as in a dedicated Git repository
14. @ConfigurationProperties beans are configured to listen to RefreshScopeRefreshedEvent events
15. RefreshScopeRefreshedEvent events can be triggered after a new change is pushed to the configuration repository, so that the client application reloads the context using the latest configuration data
16. Spring Boot Actuator defines an /actuator/refresh endpoint that you can use to trigger the event manually