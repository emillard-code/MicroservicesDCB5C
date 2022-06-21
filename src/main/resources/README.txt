Purpose of each microservice application:

MicroserviceDCB1:
Provides a basic Department model class.
Also has basic controller, repository and service classes.

MicroserviceDCB2:
Provides a basic User model class (as well as an in-built Department class).
Also has basic controller, repository and service classes.
Has a ResponseTemplateVO class that enables application to interact with Department microservice.
(Application is able to return both Department and User objects at the same time)

MicroserviceDCB3:
Has the @EnableEurekaServer annotation that allows application to act as a service registry.

MicroserviceDCB4:
Has the @EnableEurekaClient annotation and application.yml settings that
allow the application to act as an API Gateway.
Has the @EnableHystrix annotation and application.yml settings that
allow the application to also dictate fallback methods to be called.

MicroserviceDCB5:
Has the @EnableEurekaClient and @EnableHystrixDashboard annotations
and application.yml settings that allow the application to act as a hystrix dashboard.

INSTRUCTIONS:
- "http://localhost:9003/" to access the service registry page.
- "http://localhost:9005/hystrix" to access the hystrix dashboard.
- Enter "http://localhost:9004/actuator/hystrix.stream" URL into hystrix dashboard to view microservice analytics.