# The Business Value of RHACM Observability as an Enterprise Solution

## Proven Scalable and Highly Available Monitoring Setup

Red Hat Advanced Cluster Management (RHACM) Observability provides a robust, scalable, and highly available monitoring infrastructure tailored for enterprise needs. Key benefits include:

* **Scalability for Large Workloads:** Supports customers managing over 150 million series of metrics, ensuring seamless performance across large-scale environments.
* **High Availability:** Built with resiliency in mind, featuring metric data replication between stores to prevent data loss and ensure uninterrupted operations.

## Simplified Configuration with T-Shirt Sizing

RHACM Observability simplifies setup by employing "T-Shirt sizing" for configurations. This approach ensures optimal tuning of the following components for scalability and efficiency:

* RBAC Query Proxy
* Grafana
* Alertmanager
* Observatorium API
* Thanos (Query Frontend, Query, Compact, Receive, Rule, Rule Reloader, Store, Store Memcached), shipped as an Operator for better configuration
* Memcached Exporter
* Observatorium Receive Controller

## Metric Resource Utilization

RHACM provides detailed insights into resource consumption, offering metrics like `TOTAL in MilliCPUs` and `TOTAL in CPUs`. This transparency helps customers plan and allocate resources effectively.

## Designed for Enterprise Resiliency

* **Built for Resilience:** The platform is designed with data replication, ensuring continuity in the face of failures.
* **Global Query View:** Enterprise users benefit from a unified query view across the entire fleet using PromQL.

## Comprehensive and Customizable Dashboards

* **Out-of-the-Box Dashboards:** Pre-configured dashboards for key enterprise needs, including:
    * ETCD performance
    * Network insights
    * Capacity management
    * Rightsizing recommendations
* **Custom Dashboards:** Supports tailored dashboards, a critical feature for enterprises requiring unique views or KPIs.

## Global Alerting and Rule Evaluation

* **Centralized Alerting:** A global alerting mechanism spans the entire fleet.
* **Secure Destination Support:** Configurations support secure destinations for Alertmanager, meeting compliance and security requirements.

## Extensibility Without Lock-In

* **Third-Party Export Support:** RHACM Observability integrates with external systems, avoiding vendor lock-in and ensuring flexibility.
* **Fine-Grained RBAC:** Offers customizable Role-Based Access Controls for metrics, enabling organizations to tailor access by role or need.

## Upstream Alignment and Future-Readiness

* **Always Up-to-Date:** Keeps pace with upstream projects such as the Thanos Operator and Observatorium, ensuring access to the latest features and improvements.
* **Integration Ready:** Seamlessly integrates with logging, tracing, and OpenTelemetry solutions through the `MultiClusterObservabilityAddon`.

## Virtually Unlimited Metric Storage

* **Extensive Storage:** Supports extensive metric storage, providing virtually unlimited capacity for enterprises managing massive data sets.
* **Separation of Metrics:** Distinct separation between platform and user workload metrics, with flexible configuration for custom metrics.

## Case Study: Business Impact at a Large Financial Institution

A large bank, like American Express, adopted RHACM Observability to meet its enterprise-scale requirements and saw significant benefits:

* **Scalability:** Successfully managed over 150 million metric series, ensuring seamless operation across their global infrastructure.
* **Resiliency:** Leveraged data replication to guarantee business continuity and high availability for critical services.
* **Custom Dashboards:** Developed tailored dashboards for unique operational needs, empowering teams with actionable insights.
* **Global Alerting:** Established centralized alerting to monitor fleet-wide health, improving response times and operational efficiency.

---

RHACM Observability stands as a comprehensive enterprise solution, blending scalability, resiliency, and customization with seamless extensibility. Its proven benefits highlight its value in transforming enterprise monitoring and observability.
