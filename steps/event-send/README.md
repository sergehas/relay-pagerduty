# event-send

This step can be used to send events to [PagerDuty](http://pagerduty.com/). Events are the means by which incidents are [triggered](https://support.pagerduty.com/docs/incidents), acknowledged, or resolved.

## Specification

This step expects the following fields in the `spec` section of a workflow step definition that uses it:

| Setting      | Data type        | Description                                                                                                                                                                    | Default | Required                |
|--------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------|-------------------------|
| `connection` | Relay connection | A pagerduty connection containing the token                                                                                                                                    | None    | Yes                     |
| `type`       | String           | One of `trigger`, `acknowledge`, or `resolve`                                                                                                                                  | None    | Yes                     |
| `summary`    | String           | The [summary](https://developer.pagerduty.com/docs/events-api-v2/overview/#pagerduty-common-event-format-pd-cef) of the event triggered                                        | None    | For trigger type events |
| `source`     | String           | The [source](https://developer.pagerduty.com/docs/events-api-v2/overview/#pagerduty-common-event-format-pd-cef) of the event                                                   | None    | For trigger type events |
| `severity`   | String           | The [severity](https://developer.pagerduty.com/docs/events-api-v2/overview/#pagerduty-common-event-format-pd-cef) of the event. One of: `info`, `warning`, `error`, `critical` | None    | No                      |
| `dedup_key`  | String           | The [deduplication key](https://support.pagerduty.com/docs/event-management) to group all events relating to an incident                                                       | None    | Yes                     |

## Outputs

| Name        | Data type | Description                                     |
|-------------|-----------|-------------------------------------------------|
| `dedup_key` | String    | The de-duplication key for the referenced event |
