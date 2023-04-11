# Modernization Strategies
A model for choosing the optimal modernization strategy for each subsystem. This allows a portfolio-based approach to modernization where the optimal ROI can be determined on a granular basis to achieve the optimal overall ROI of your modernization investment. It's crucial to avoid over-investing in areas that add unnecessary costs and slow down modernization in your critical strategic domains.

Feel free to adapt this to your organization's specific needs. Pull requests accepted if you'd like to contribute improvements or share links to your content on this topic.

This model is used in my book [Architecture Modernization](https://www.manning.com/books/architecture-modernization). 

![modernization-strategies](https://user-images.githubusercontent.com/692094/230796861-c8d2cd3b-aa75-4f02-a3ff-ba29e592b2f0.jpg)

## Platform Modernization

The Y-axis represents the level of modernization applied to the technologies used to build the subsystem. It includes:

- **Infrastructure**: e.g. from on-prem to the cloud or from VMs to Serverless
- **Programming language and runtime**: e.g. from C# .NET to Kotlin on the JVM
- **Data storage and integration**: e.g. from Oracle SQL to a Mongo DB and Rabbit MQ
- **Libraries and frameworks**: e.g. adopting new web frameworks, persistence frameworks, and testing frameworks

A simple option for producing an overall score is to choose high (3 points), medium (2 points) or low (1 point) for each criteria above.

## Product, Domain, and Software Modernization

The X-axis represents the level of modernization applied to changing the behavior and design of the code so that it provides more value or is easier to work with. This is more of a range:

- **Expose**: Making existing functionality from the legacy subsystem available to other subsystems (e.g. by creating an API or publishing an event), with the least amount of effort and invasive changes possible
- **Polish**: Cleaning up some of the low hanging technical debt without addressing more fundamental issues
- **Rewrite**: Rewrite the subsystem maintaining the existing functionality but cleaning up all the technical debt 
- **Remodel**: Retaining the existing functionality but redesigning the domain model so that it is easier to maintain and evolve the code 
- **Rethink**: The functionality and domain model is totally recreated from a blank canvas, typically involving large amounts of user research and domain modeling

## Example Strategies

The following are some example strategies. This isn't an exhaustive list so don't feel a need to try and fit what you are doing exactly into one of these

- **Sunset**: The subsystem will be discontinued and shutdown (there is no modernization but this could still involve a large amount of effort and risk)
- **Maintain**: Try to keep the current subsystem running for the least cost. There will still be some effort involved keeping the technologies upto date with the latest security patches etc
- **Legacy Encapsulate**: As above but expose the legacy capabilities to other subsystems
- **Legacy Polish**: Similar to the above but also addressing small amounts of technical debt
- **Extract and Remodel**: Pulling a subsystem out of the legacy system and rebuilding with a brand new domain model (existing functionality and tech stack remains largely the same)
- **Lift and Shift**: Move the current code onto new infrastructure with minimal or no changes to application code
- **Lift and Reshape**: As above but cleaning up some parts of the code so that new features can be added more easily or it runs more reliably in production
- **Rehost and Remodel**: Rebuild the system with a fresh domain model and deploy to more modern infrastructure, using largely the same programming languages and frameworks
- Total Modernization: Every aspect of the technology, functionality, and domain model is completely modernized to the highest degree possible. Likely to be a very expensive option but justifiable for subsystems that are a major source of competitive advantage or innovation.
