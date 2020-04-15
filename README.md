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
Prometheus is a popular open-source metrics and alerting solution that features hundreds of community-built exporters which enable a wide range of systems to be monitored. It is commonly paired with a visualisation system like Grafana.

However there are some challenges that arise from using Prometheus. These can be summarised as Scaling, Silos and Context-switching.

* Scaling
As more and more metrics are generated and alerts configured, teams need to find a way to scale Prometheus to cope with the demand. This can involve complex sharding or running multiple Prometheus instances per team. This costs in terms of infrastructure resources and human resources to implement. Some companies turn to hosted solutions to allow them to reduce this complexity, at the cost of paying a vendor.

* Silos
In a typical company, you tend to see many Prometheus instances in use, perhaps by team or by department. The problem with this is that in an incident that cuts across teams or departments, SRE's lack the ability to query across these data silos to pinpoint the issue. Furthermore it makes it much harder to Business Intelligence (BI), long-term reporting and cross company dashboards.

* Context-switching
Metrics are just one of the [three](https://www.oreilly.com/library/view/distributed-systems-observability/9781492033431/ch04.html) ([some say four(https://newrelic.com/platform/telemetry-data-101/)]) pillars of Observability.

At New Relic we believe there is considerable benefit to having all of Observability data (Metrics, Events, Logs and Traces) in a single platform. You can benefit from economies of scale, build skills in a single platform, break down data silos and fix issues faster by preventing context-switching between different tools to diagnose a single issue. This problem is not unique to Prometheus, but if you are using a different tool to store and query each of the different telemetry types, you are wasting precious time when you could be focussing on restoring service to your customers.

New Relic provides a [Prometheus integration](https://docs.newrelic.com/docs/integrations/prometheus-integrations) which enables you to ingest OpenMetrics from an endpoint, all without needing to run the Prometheus server. This means you can benefit from the rich ecosystem of exporters and client libraries without having to run Prometheus itself. It can be run on [Kubernetes](https://docs.newrelic.com/docs/integrations/prometheus-integrations/get-started/new-relic-prometheus-openmetrics-integration-kubernetes) or as a [stand-alone Docker container](https://docs.newrelic.com/docs/integrations/prometheus-integrations/get-started/new-relic-prometheus-openmetrics-integration-kubernetes).

Once deployed, you can [view or query your OpenMetrics data](https://docs.newrelic.com/docs/integrations/prometheus-integrations/view-query-data/view-query-your-prometheus-openmetrics-data).

### Micrometer

### Kamon.io - Monitoring Scala apps

### Dropwizard

### StatsD / DogStatsD / GoStatsD

