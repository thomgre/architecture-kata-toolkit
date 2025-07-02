# Architecture Characteristics

>  Characteristics marked with `(implicit)` can become driving characteristics if they are critical concerns. 

## Abstraction
The level at which parts of the system are isolated from other parts of the system (both internal and external system interactions)

## Adaptability
The ease in which a system can adapt to changes in environment and functionality

## Availability
The amount of uptime of a system; usually measured in 9's (e.g., 99.9%)

## Concurrency
The ability of the system to process simultaneous requests, in most cases in the same order in which they were received; implied when scalability and elasticity are supported

## Configurability
The ability of the system to support multiple configurations, as well as support custom on-demand configurations and configuration updates

## Data Consistency
The data across the system is in sync and consistent across databases and tables

## Data Integrity
The data across the system is correct and there is no data loss in the system

## Deployability
The amount of ceremony involved with releasing the software, the frequency in which releases occur, and the overall risk of deployment

## Elasticity
The system can expand and respond quickly to unexpected or anticipated extreme loads (e.g., going from 20 to 250,000 users instantly)

## Extensibility
The ease in which a system can be extended with additional features and functionality

## Fault Tolerance
When fatal errors occur, other parts of the system continue to function

## Feasibility (implicit)
Considering timeframes, budgets, and developer skills when making architectural choices; tight timeframes and budgets make this a driving architectural characteristic

## Interoperability
The ability of the system to interface and interact with other systems to complete a business request

## Maintainability (implicit)
The level of effort required to locate and apply changes to the system

## Observability (implicit)
The ability of a system or a service to make available and stream metrics such as overall health, uptime, response times, performance, etc.

## Performance
The amount of time it takes for the system to process a business request

## Recoverability
The ability of the system to start where it left off in the event of a system crash

## Responsiveness
The amount of time it takes to get a response to the user

## Scalability
A function of system capacity and growth over time; as the number of users or requests increase in the system, responsiveness, performance, and error rates remain constant

## Security (implicit)
The ability of the system to restrict access to sensitive information or functionality

## Testability
The ease of and completeness of testing

## Workflow
The ability of the system to manage complex workflows that require multiple parts (services) of the system to complete a business request