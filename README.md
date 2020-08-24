# PagerDuty

This integration provides interoperability with
[PagerDuty](https://www.pagerduty.com/) for incident response and real-time
operations.

## Actions

The following are supported actions:

| Type    | Name                                             | Description                                                                |
|---------|--------------------------------------------------|----------------------------------------------------------------------------|
| Trigger | [incident-triggered](/triggers/incident-trigger) | When a new incident is created in PagerDuty                                |
| Step    | [event-send](/steps/event-send)                  | Send an event to PagerDuty to trigger, acknowledge, or resolve an incident |
| Step    | [change-event-send](/steps/change-event-send)    | Send a change event to PagerDuty                                           |

## Contributing

### Issues

Feel free to submit issues and enhancement requests.

### Contributing

In general, we follow the "fork-and-pull" Git workflow.

 1. **Fork** the repo on GitHub
 2. **Clone** the project to your own machine
 3. **Commit** changes to your own branch
 4. **Push** your work back up to your fork
 5. Submit a **Pull request** so that we can review your changes

NOTE: Be sure to merge the latest from "upstream" before making a pull request!

### License

As indicated by the repository, this project is licensed under Apache 2.0.
