# Use Cases for New Relic Metrics

A list of use cases for New Relic Metrics.

# What is New Relic Metrics?

New Relic Metrics is an API, along with software libraries such as SDK's and exporters that you can use to easily ingest dimensional metrics to New Relic. Once ingested, you can query, visualise and alert on those metrics to give you an in-depth view into how your systems and software are performing.

In the monitoring industry, "dimensional" metrics refer to metric data that has a variety of attributes (dimensions) attached, such as duration-related attributes (start time, end time), entity ID, region, host, etc. This amount of detail allows for in-depth analysis and querying.

The Metric API is how metrics are ingested from some of our [integrations](https://newrelic.com/integrations), including our [open source exporters](https://docs.newrelic.com/docs/data-ingest-apis/get-data-new-relic/new-relic-sdks/telemetry-sdks-send-custom-telemetry-data-new-relic#external-data) (like DropWizard, OpenCensus, and Prometheus). The Metric API is also used by our [Telemetry SDKs](https://docs.newrelic.com/docs/data-ingest-apis/get-data-new-relic/new-relic-sdks/telemetry-sdks-send-custom-telemetry-data-new-relic), which are language-specific tools that make it easier to use our data-ingest APIs.

## Application Monitoring

## Infrastructure Monitoring

## Business Metrics

## Internet of Things (IoT)

## Kubernetes

## Integrating with other sources of Metric data

### Prometheus

### Micrometer

### Kamon.io - Monitoring Scala apps

### Dropwizard

### StatsD / DogStatsD / GoStatsD

