# Modernization Strategies
A model for choosing the optimal modernization strategy for each subsystem. Feel free to adapt this to your organization's specific needs, and share any links here to content you have publicly shared on this topic.

This model is used in my book [Architecture Modernization](https://www.manning.com/books/architecture-modernization). 

![modernization-strategies](https://user-images.githubusercontent.com/692094/230796861-c8d2cd3b-aa75-4f02-a3ff-ba29e592b2f0.jpg)

## Platform Modernization

The Y-axis represents the level of modernization applied to the technologies used to build the subsystem. It includes:

- Infrastructure: e.g. from on-prem to the cloud or from VMs to Serverless
- Programming language and runtime: e.g. from C# .NET to Kotlin on the JVM
- Data storage and integration: e.g. from Oracle SQL to a document DB and message bus
- Libraries and frameworks: e.g. adopting new web frameworks, persistence frameworks, and testing frameworks

A simple option for producing an overall score is to choose high (3 points), medium (2 points) or low (1 point) for each criteria above.

## Product, Domain, and Code Modernization

The X-axis represents the level of modernization applied to changing the behavior and design of the software so that it provides more value or is easier to work with. This is more of a range:

- Expose: Making existing functionality from the legacy subsystem available to other subsystems (e.g. by creating an API or publishing an event), with the least amount of effort and invasive changes possible
- Polish: Cleaning up some of the low hanging technical debt without addressing more fundamental issues
- Rewrite: Rewrite the subsystem maintaining the existing functionality but cleaning up all the technical debt 
- Remodel: Retaining the existing functionality but redesigning the domain model so that it is easier to maintain and evolve the code 
- Rethink: The functionality and domain model is totally recreated from a blank canvas, typically involving large amounts of user research and domain modeling

## Example Strategies

- ???
