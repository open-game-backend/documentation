# Service Checklist

1. Create Spring Boot application.
    1. Add Spring Boot Starter Web.
    1. Add Spring Boot Starter Data JPA.
    1. Add Spring Cloud Starter Netflix Eureka Client.
    1. Add `net`, `util` and `test` library dependencies and repositories.
1. Setup Spring Boot application.
    1. Replace `application.properties` with `application.yml`.
    1. Set application port.
    1. Set application name.
    1. Add resource filtering to `pom.xml`.
    1. Set application version.
    1. Configure Eureka client and H2 console for local development.
1. Setup GitHub CI.
    1. Add `<distributionManagement>` to `pom.xml`.
    1. Create workflow YML file.
1. Setup logging.
    1. Add `@EnableOpenGameBackendUtils` and `@ConfigurationPropertiesScan`.
    1. Add Elastic dependency.
    1. Add `logback-spring.xml`.
    1. Add Zalando Logbook dependency.
    1. Set Zalando Logbook log level to `TRACE`.
1. Setup API documentation.
    1. Add `springdoc-openapi-ui` dependency.
    1. Add `OpenAPI` bean.
    1. Verify documentation at `http://localhost:<PORT>/swagger-ui/index.html?configUrl=/v3/api-docs/swagger-config#/`
1. Create persistence layer.
    1. Add H2 and MariaDB database dependencies.
    1. Add Flyway dependency.
    1. Add JPA entities.
    1. Add repositories and tests.
    1. Add database migrations.
    1. Seed database.
1. Create service layer.
    1. Add services and tests, with request and response DTOs in `net` library.
1. Create endpoint layer.
    1. Add controllers and integration tests.
    1. Add `GlobalControllerExceptionHandler`.
1. Verify security.
    1. Secure endpoints in `WebSecurityConfig` of gateway if necessary.
1. Setup Ansible deployment.
    1. Add host to `hosts` and `hosts.example`.
    1. Add service playbook.
    1. Add service playbook to `site.yml`.
    1. Add service configuration file.
    1. Add credentials to `vars`, `vault` and `vault.example`.
