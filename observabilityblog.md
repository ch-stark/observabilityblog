# The Business Value of RHACM Observability as an Enterprise Solution

Red Hat Advanced Cluster Management (RHACM) Observability delivers a technically robust, scalable, and highly available monitoring infrastructure specifically engineered for demanding enterprise environments. This solution extends comprehensive observability across your entire fleet, including **any CNCF-Certified Kubernetes Cluster**.

---

## Proven Scalable and Highly Available Monitoring Setup

RHACM Observability is architected to manage vast metric datasets, demonstrated by its capability to support customers with **over 150 million series of metrics**. This capacity ensures consistent performance across the largest deployments, effectively overcoming the inherent retention limitations of standalone OpenShift monitoring. Its high-availability design incorporates metric data replication between stores, preventing data loss and ensuring continuous operational insights—a critical factor for business continuity in enterprise settings.

---

## Simplified Configuration with T-Shirt Sizing and Thanos Optimization

RHACM Observability streamlines deployment and configuration through a "T-Shirt sizing" methodology, which pre-tunes core components for optimal scalability and efficiency. A pivotal element within this architecture is **Thanos**, an open-source, highly scalable observability platform for storing, querying, and visualizing Prometheus metrics across distributed environments. Thanos is crucial for achieving long-term data retention, global querying capabilities, and high availability in large-scale setups.

The components optimized include:

* RBAC Query Proxy
* Grafana (with future alignment to Perses)
* Alertmanager
* Observatorium API
* **Thanos**: This suite of components (Query Frontend, Query, Compact, Receive, Rule, Rule Reloader, Store, Store Memcached) is the backbone of RHACM Observability's scalability and long-term retention. Its role is paramount for handling the immense volume of metrics and enabling efficient querying across disparate Prometheus instances. RHACM's future plans include shipping Thanos as a dedicated Operator for enhanced, simplified configuration and management.
    * **Thanos Tuning for Scale**: For large-scale deployments, optimizing Thanos components is crucial. Key considerations for performance and efficiency include:
        * **Thanos Compactor**: This component is responsible for data compaction and downsampling, which drastically reduces storage costs and improves query performance for historical data. Careful configuration of retention policies (e.g., raw data for 90 days, 5-minute resolution for 180 days, 1-hour resolution for 1 year) is essential. Ensuring the Compactor is actively processing blocks is critical, and alerts should be configured to detect any stoppage.
        * **Thanos Query Frontend**: Acts as a caching layer and query splitter, significantly improving the performance of complex and long-range PromQL queries by breaking them into smaller, more manageable parts. Effective caching, often via Memcached, is vital.
        * **Thanos Store Gateway**: Provides a read-only interface to the object storage where metrics are stored. For very large datasets, sharding the Store Gateway based on time ranges can distribute the query load and improve retrieval times.
        * **Thanos Receive**: When used for remote write, proper tuning of `batch_send_deadline` and backoff settings helps manage ingestion load and prevent overloading the receiver, especially during restarts or high churn. Choosing between `hashmod` and `ketama` for hashring distribution impacts churn during scaling operations.
        * **Metric Cardinality and Retention**: Aggressively pruning unnecessary metrics and managing high-cardinality labels directly impacts Thanos's performance and storage footprint. Only essential metrics should be retained for long periods, with appropriate downsampling applied to older data.
* Memcached Exporter
* Observatorium Receive Controller

---

## Comprehensive Metric Resource Utilization and Planning

RHACM provides granular insights into resource consumption, offering metrics such as `TOTAL in MilliCPUs` and `TOTAL in CPUs`. This transparency is critical for effective resource planning and allocation. Furthermore, our **rightsizing dashboards** provide data-driven recommendations to optimize resource utilization, leading to demonstrable cost savings and enhanced performance.

---

## Designed for Enterprise Resiliency

The platform is engineered for inherent resilience, leveraging data replication to ensure continuity in the face of failures and to meet stringent enterprise data retention requirements. Enterprise users gain a unified global query view across their entire cluster fleet using PromQL, significantly simplifying complex monitoring and troubleshooting tasks. This unified view spans all managed clusters, including **any CNCF-Certified Kubernetes Cluster**.

---

## Comprehensive and Customizable Dashboards

RHACM Observability includes a suite of pre-configured, **out-of-the-box dashboards** tailored for essential enterprise monitoring requirements, covering:

* ETCD performance
* Network insights
* Capacity management
* **Rightsizing recommendations**

Beyond these standard offerings, RHACM Observability supports the creation of custom dashboards, a crucial capability for enterprises requiring bespoke views or specific Key Performance Indicators (KPIs). For advanced customization and modern visualization, RHACM is strategically aligning with **Perses**, a Cloud Native Computing Foundation (CNCF) project, ensuring future-readiness and adherence to open standards.

---

## Global Alerting and Rule Evaluation

A global alerting mechanism provides centralized, consistent, and efficient incident response across the entire fleet. Furthermore, configurations support secure destinations for Alertmanager, ensuring compliance with stringent enterprise security and regulatory requirements.

---

## Extensibility Without Lock-In

RHACM Observability promotes extensibility and avoids vendor lock-in through:

* **Third-Party Export Support**: Seamless integration with external systems ensures flexibility within your existing operational ecosystem.
* **Fine-Grained RBAC**: Customizable Role-Based Access Controls for metrics allow organizations to precisely tailor access permissions by role or need, significantly enhancing security and operational control.

---

## Upstream Alignment and Future-Readiness

RHACM Observability maintains pace with critical upstream projects, including the Thanos Operator and Observatorium, guaranteeing access to the latest features, performance enhancements, and community innovations. It seamlessly integrates with logging, tracing, and OpenTelemetry solutions via the `MultiClusterObservabilityAddon`, providing a holistic view of your distributed infrastructure.

---

## Virtually Unlimited Metric Storage

The solution supports extensive metric storage, offering virtually unlimited capacity for enterprises managing massive data sets and addressing long-term retention requirements without compromise.

---

## Case Study: Business Impact at a Large Financial Institution

A prominent financial institution adopted RHACM Observability to address its enterprise-scale requirements and realized substantial benefits:

* **Scalability**: Successfully managed over 150 million metric series, ensuring seamless operation across their global infrastructure and meeting their long-term retention needs.
* **Resiliency**: Leveraged robust data replication mechanisms to guarantee business continuity and high availability for critical services.
* **Custom Dashboards**: Developed tailored dashboards for unique operational needs, empowering teams with actionable insights and leveraging rightsizing recommendations to optimize resource expenditure.
* **Global Alerting**: Established centralized alerting to monitor fleet-wide health across **all CNCF-Certified Kubernetes Clusters**, significantly improving response times and overall operational efficiency.

RHACM Observability stands as a comprehensive enterprise-grade solution, harmonizing scalability, resiliency, and customization with seamless extensibility. Its demonstrated benefits underscore its value in transforming enterprise monitoring and observability, empowering organizations to gain deeper operational insights, ensure continuous business operations, and optimize resource utilization across their diverse Kubernetes environments.
