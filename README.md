Adaptiv.MuleDotNetSamples.MuleEsb
=================================
The following Mule AnyPoint project is an APIKit based sample that demonstrates MuleESB dotNet & MSMQ connector features.

The project references classes from https://github.com/nikolaiblackie/Adaptiv.MuleDotNetSamples.DotNet which are precompiled and stored in / src / main / resources /

Samples part of Auckland Code Camp 2014 presentation demonstrations  http://www.slideshare.net/nikolaiadaptiv/mule-anypoint-platform-dot-net-alice-in-a-java-integration-wonderland

References used to build samples:
* Dotnet Connector
  * http://www.mulesoft.org/documentation/display/current/DotNet+Connector 
* MSMQ Connector
 * http://www.mulesoft.org/documentation/display/current/MSMQ+Connector 
* Mule Blogs
 * http://blogs.mulesoft.org/solutions-for-microsoft/ 
 * http://blogs.mulesoft.org/integrating-mule-esb-net-based-rules-engines/ 


Highlights of sample:

* \src\main\api\ComplexSample.raml - sample RAML that outlines resources and verbs for exposing sample functions
* \src\main\app\ComplexSample.xml - APIKit Generated flows
  * post:/SampleSimple - demonstrates primative method call
  * post:/SampleComplex - demonstrates message parameter based method call
  * post:/SampleMSMQComplex - demonstrates routing a message to MSMQ
    *Pre-requisites
  * post:/SampleBREComplex - demonstrates calling a .NET method exposing BizTalk rules engine
  
Pre-requisites for samples:
* Sample only runs on Windows based environments, must have .NET4.5 installed
* post:/SampleMSMQComplex
  * Must install Anypoint Gateway for Windows, see http://www.mulesoft.org/documentation/display/current/MSMQ+Connector
  * Must create a queue for configuration queueName=".\private$\msmq-demo"
  * Must replace accessToken="jXwF7YJGVm6D0/MbUbPHat483iM=" in msmq:config with token generated on install
* post:/SampleBREComplex
  * Must have install BizTalk Server business rules engine and deployed BRE policies referenced in https://github.com/nikolaiblackie/Adaptiv.MuleDotNetSamples.DotNet
