# sarva
Before we start a project, a developer ( or team ) has to make a lot of choices. Few of the choices are 
* Language to choose
* Configuration Management ( Config by environment / app type with ability to change it with GUI )
* Building a reliable, scalable and elastic application that can cater to changing demands of business ( Incl. Multi threaded and multiple nodes across data centers )
* Managing state of an application in a clustered environment
* Log management ( mine and alert on top of it )
* Insights into internal workings of an application in production ( it is beyond just logging e.g. monitoring memory patterns, heap size, threads etc. )
* Message Bus ( Kafka or Something Else )
* Data Processing ( Spark, Samza, Storm, Flink, Druid - what NOT )
* Alerting when things go south ( Email, Slack, Pager Duty, Netcool etc. )
* Web App ( with GUI and REST end points )
  * GUI ( It has whole lot of other implications like Bootstrap, ReactJS and what NOT )
  * REST APIs
    * Rate limiting and throttling
    * Discoverability
* Make onboarding of application seamless
* Continous Development
  * CI for Builds
  * Unit Test Cases ( Pre-Commit Hooks )
  * Nightly Builds 
  * Promotion Logic to various enviroments for testing
  * Ideal would be tear up and down environments ( to use resources optimally )

# Goal
* A skeleton that provides all of the above in one go. So that developer can focus on writing business logic and not spend time on learning or figuring out all of the above. 
* To accomplish above, skeleton would require multiple components. All of the them should get configured via GUI and have flexibility to make changes via configuration ( preferabally GUI )
 * Eventually, for each component we should have mutliple options and based upon the choice that user has selected at the time of setup, we should get that relevant components installed / added to the code base.
* All components will have scalaing at the core and this would be managed via GUI ( say Mesos or Kubernetes )

