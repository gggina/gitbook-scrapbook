# How to set up traces

This how-to describes the steps to set up traces that can be viewed in the StackState Traces perspective.

For traces to be available in StackState, you will need to install the [StackState Agent V2 StackPack](/stackpacks/integrations/agent) and configure one of the tracing integrations.

## Install the StackState Agent StackPack

The StackState Agent V2 StackPack enables integration with external systems to receive trace data. You can check if it is installed on the StackPacks page in StackState. If it is not installed, follow the installation instructions on [StackState Agent V2 StackPack](/stackpacks/integrations/agent).

## Configure StackState Agent V2 integrations to receive trace data

Once the StackState Agent V2 StackPack is installed, you can configure the associated integrations with external systems. The following integrations are used by StackState to populate the Traces perspective:

- **Java APM** - provides tracing support for Java JVM based systems.
- **DotNet APM** - runs in-process to instrument your applications and send traces to StackState.
- **Traefik** - adds topology and telemetry information from Traefik.
- **AWS X-ray** - collects tracing information from the AWS built in distributed tracing system.

Full configuration details for each available StackState Agent V2 integration are included in StackState. These can be accessed from the StackPacks page.

1. Go to the StackPacks page in the StackState GUI
2. Click **Tracing** from the tags listed at the top of the page. This will filter the listed StackPacks to show only those used for traces.
3. Click on the integration you want to configure and follow the instructions provided to set up traces.

## Still not able to see traces?
