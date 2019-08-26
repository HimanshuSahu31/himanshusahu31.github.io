



# GSoC Project 2019: Molr - Operational

## About the project
Molr is a modular distributed execution and debugging framework which provides a unified way to interact (locally or remotely) with executable code to run it and/or debug it. It is possible to provide input to it and retrieve output, return values, and exceptions from this. It is based on a command-response communication protocol.

In the view of LHC Run 3, we want to extend the functionalities of Molr so that it will be ready to use in production to control various operational systems.


## Summary

This project has evolved a lot over the past two years since its inception but there's still a lot more work to do for it to be ready to be used in production. I’ve worked on the issues and features that were in the roadmap for GSoC 2019. Below is the progress report. Please go through the links to learn in detail about the individual issues, discussions related to it and the code committed.

## Progress Report

### Completed
- [Switch REST streams to server-sent events](https://github.com/molr/molr/issues/22): Converting all existing streams to server-sent events.
    - [Pull Request #30](https://github.com/molr/molr/pull/30)  for the [molr project](https://github.com/molr/molr)
    - [Pull Request #3](https://github.com/molr/molr-pymole/pull/3) for the [molr-pymole Project]( https://github.com/molr/molr-pymole)
- [MissionStubs](https://github.com/molr/molr/issues/26): Support for typed missions up to two parameters.
- [MissionControlSupport](https://github.com/molr/molr/issues/33): Exposing some convenience methods to instantiate and control executing missions.
    - [Pull Request #35](https://github.com/molr/molr/pull/35): Both MissionStubs and MissionControlSupport have been implemented in this PR.

### Code Review
- [Provide a standard way to recuperate mission logs from moles](https://github.com/molr/molr/issues/20): Users instantiating a mission should be able to track the progress of the executing mission with the helps of logs. They will be able to subscribe to this exposed API using the Mission Instance Handle.
    - [Pull Request #37](https://github.com/molr/molr/pull/37): This solution uses log4j framework as a dependency for logging and appenders.
    - [Pull Request #38](https://github.com/molr/molr/pull/38): This solution uses logback framework and works in with slf4j. It's used for appenders only and logging is done as previously with slf4j.

### In-Progress
- [General purpose test suite for (remote) moles](https://github.com/molr/molr/issues/13): There can be multiple implementations of a mole in other programming languages. We should have a test suite in place to help developers test and validate their implementations of mole. 

### To Do
- [Register remote Mole at runtime](https://github.com/molr/molr/issues/28)
- [Return value of a mission](https://github.com/molr/molr/issues/27)
- [A Mission shall be able to call other Missions](https://github.com/molr/molr/issues/8)

## Future Work
- Work on open issues
- Suggest features to improve the project
- Provide support as and when required
## Conclusion

GSoC has provided me with an awesome summer and a great experience to work with [Andrea](https://github.com/andreacalia), [Kajetan](https://github.com/kaifox) and [Michi](https://github.com/michi42). This was my first open-source project and a project with such a large codebase that I've worked on. I've had problems initially to grasp the concepts of the project. After solving my second issue, I started to gain some confidence in the concepts and now I'm more confident than ever.

GSoC has been a great journey into the open-source world. This project has exposed me to various frameworks such as Project Reactor, Spring WebFlux, Log4j, Logback and other programming techniques test-driven development. Apart from this, I've written test suites,  code documentation, and used various design patterns to make my code modular and of quality.  I was new to almost all the things I worked on but I kept experimenting, failing, learning and then finally arriving at the solution. 

For me, I’ll continue to contribute to Molr and finish what I started. I am excited that my code will be used in LHC Run 3. 

PS: I thank my mentors for guiding me throughout the GSoC period. I hope to continue the collaboration in this project as well as other open-source projects with my mentors. :-)   Finally, I thank Google for this amazing opportunity.
