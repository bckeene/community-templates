# InfluxDB Open Source (OSS) Pricing Metrics Template

Provided by: InfluxData

This InfluxDB Template monitors usage trends from a local instance using the `/metrics` endpoint. This template is designed to aid in calculating pricing costs before migrating workloads to InfluxDB Cloud.

![InfluxDB 2 Dashboard Screenshot](influxdb2_oss_pricing_metrics_dashboard.png)

#### Template installation via InfluxDB UI
In the InfluxDB UI, go to Settings, Templates, and enter this URL: 
```
https://raw.githubusercontent.com/influxdata/community-templates/master/influxdb2_oss_pricing_metrics/usage_metrics_template.yml
```

#### Template installation via Influx CLI
If you have your InfluxDB credentials [configured in the CLI](https://v2.docs.influxdata.com/v2.0/reference/cli/influx/config/), you can also install this template with:

```
influx apply -u https://raw.githubusercontent.com/influxdata/community-templates/master/influxdb2_oss_pricing_metrics/usage_metrics_template.yml
```

## Included Resources

- 1 Bucket: `metrics` (default 3 day retention)
- 1 Labels: `OSS Monitoring`
- 1 Dashboard: `InfluxDB (open source usage metrics)`

## Setup Instructions

General instructions on using InfluxDB Templates can be found in the [use a template](../docs/use_a_template.md) document.

The data for the dashboard is populated by setting up the local `/metrics` scraper (see [InfluxDB OSS metrics scraper documentation](https://docs.influxdata.com/influxdb/v2.4/reference/internals/metrics/)). Note data collection will only begin once the scraper is setup and configured to send metrics to the `metrics` bucket

## Contact

- Author: Brian Keene
- Email: bkeene@influxdata.com
- Github: [@bckeene](https://github.com/bckeene)
