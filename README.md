AppDynamics Agents for OpenShift using Source-To-Image
======
# Dockerfile
The Docerfile was enhanced by Configuration Properties to configure the Application to be monitored by the AppDynamics Java Agent.

These are as follows:
```
ENV APPDYNAMICS_CONTROLLER_HOST_NAME
ENV APPDYNAMICS_CONTROLLER_PORT
ENV APPDYNAMICS_CONTROLLER_SSL_ENABLED
ENV APPDYNAMICS_AGENT_APPLICATION_NAME
ENV APPDYNAMICS_AGENT_TIER_NAME
ENV APPDYNAMICS_AGENT_ACCOUNT_NAME
ENV APPDYNAMICS_AGENT_ACCOUNT_ACCESS_KEY
ENV APPDYNAMICS_AGENT_VERSION

RUN yum install -y unzip curl && yum clean all -y
```
Please change the ENV properties to suite your needs.
# Assemble
The assemble Script was enhanced to Download the AppDynamics Java Agent.
# Run
The run Script was enhanced to export the ```JAVA_OPTS``` environment variable to include the reference to the AppDynamics Java Agent.
