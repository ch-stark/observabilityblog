# The Business Value of RHACM Observability as an Enterprise Solution

## Proven Scalable and Highly Available Monitoring Setup

Red Hat Advanced Cluster Management (RHACM) Observability provides a robust, scalable, and highly available monitoring infrastructure tailored for enterprise needs. Key benefits include:

* **Scalability for Large Workloads:** RHACM Observability is built to handle massive data sets, supporting customers managing **over 150 million series of metrics**. This ensures seamless performance across your largest environments, overcoming the inherent retention limits of OpenShift alone.
* **High Availability:** Designed with resilience in mind, RHACM Observability features metric data replication between stores to prevent data loss and ensure uninterrupted operations, critical for business continuity.

## Simplified Configuration with T-Shirt Sizing

RHACM Observability simplifies setup by employing "T-Shirt sizing" for configurations. This approach ensures optimal tuning of the following components for scalability and efficiency:

* RBAC Query Proxy
* Grafana (Perses in the future)
* Alertmanager
* Observatorium API
* Thanos (Query Frontend, Query, Compact, Receive, Rule, Rule Reloader, Store, Store Memcached) – soon shipped as an Operator for better configuration
* Memcached Exporter
* Observatorium Receive Controller

## Comprehensive Metric Resource Utilization and Planning

RHACM provides detailed insights into resource consumption, offering metrics like `TOTAL in MilliCPUs` and `TOTAL in CPUs`. This transparency helps customers plan and allocate resources effectively. Furthermore, our **rightsizing dashboards** provide recommendations to optimize your resource utilization, leading to cost savings and improved performance.


## Designed for Enterprise Resiliency

* **Built for Resilience:** The platform is designed with data replication, ensuring continuity in the face of failures and meeting enterprise retention requirements.
* **Global Query View:** Enterprise users benefit from a unified query view across the entire fleet using PromQL, simplifying complex monitoring tasks.

## Comprehensive and Customizable Dashboards

* **Out-of-the-Box Dashboards:** RHACM Observability includes pre-configured dashboards for key enterprise needs, including:
    * ETCD performance
    * Network insights
    * Capacity management
    * **Rightsizing recommendations**
* **Custom Dashboards:** Beyond the out-of-the-box options, RHACM Observability supports tailored dashboards, a critical feature for enterprises requiring unique views or Key Performance Indicators (KPIs). For advanced customization and modern visualization, RHACM is aligning with **Perses**, a Cloud Native Computing Foundation (CNCF) project.

## Global Alerting and Rule Evaluation

* **Centralized Alerting:** A global alerting mechanism spans the entire fleet, enabling consistent and efficient incident response.
* **Secure Destination Support:** Configurations support secure destinations for Alertmanager, meeting stringent compliance and security requirements.

## Extensibility Without Lock-In

* **Third-Party Export Support:** RHACM Observability integrates seamlessly with external systems, avoiding vendor lock-in and ensuring flexibility within your existing ecosystem.
* **Fine-Grained RBAC:** Offers customizable Role-Based Access Controls for metrics, enabling organizations to tailor access by role or need, enhancing security and operational control.


## Upstream Alignment and Future-Readiness

* **Always Up-to-Date:** RHACM Observability keeps pace with upstream projects such as the Thanos Operator and Observatorium, ensuring access to the latest features and improvements.
* **Integration Ready:** Seamlessly integrates with logging, tracing, and OpenTelemetry solutions through the `MultiClusterObservabilityAddon`, providing a holistic view of your infrastructure.


## Virtually Unlimited Metric Storage

* **Extensive Storage:** Supports extensive metric storage, providing virtually unlimited capacity for enterprises managing massive data sets and addressing long-term retention requirements.
* **Separation of Metrics:** Distinct separation between platform and user workload metrics, with flexible configuration for custom metrics, giving you granular control over your observability data.


## Case Study: Business Impact at a Large Financial Institution

A large bank adopted RHACM Observability to meet its enterprise-scale requirements and saw significant benefits:

* **Scalability:** Successfully managed over 150 million metric series, ensuring seamless operation across their global infrastructure and meeting their retention needs.
* **Resiliency:** Leveraged data replication to guarantee business continuity and high availability for critical services.
* **Custom Dashboards:** Developed tailored dashboards for unique operational needs, empowering teams with actionable insights and leveraging rightsizing recommendations.
* **Global Alerting:** Established centralized alerting to monitor fleet-wide health, improving response times and operational efficiency.


RHACM Observability stands as a comprehensive enterprise solution, blending scalability, resiliency, and customization with seamless extensibility. Its proven benefits highlight its value in transforming enterprise monitoring and observability, enabling organizations to gain deeper insights, ensure business continuity, and optimize resource utilization.
