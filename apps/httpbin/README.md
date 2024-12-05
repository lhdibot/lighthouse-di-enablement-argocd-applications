# config.json Parameters

> This file will set parameters within this project's ArgoCD applications. 

The name and path will be set for all applications, but all parameters underneath the environments will only apply to their respective environment.

All parameters labeled in the following table must be included in your configuration. If any of the parameters are not included, an error will appear on the ApplicationSet that created the applications: 

The ApplicationSet can be found by searching `{PROJECT_NAME}-tenant-applications` in ArgoCD. 

## Parameters

| Key | Description |
|-----|-------------|
| name | Name of the application |
| path | Path to the application's helm chart configuration |
| target_revision | Desired branch/tag for the application to target (see [ArgoCD Documentation on tracking strategies](https://argo-cd.readthedocs.io/en/stable/user-guide/tracking_strategies/#git)) |
| auto_sync | Stringified boolean to turn auto sync on or off (i.e. "true" or "false") |
| sync_options | Allows for [advanced sync options](https://argo-cd.readthedocs.io/en/stable/user-guide/sync-options/) to be set |
| on_created_slack | Semicolon separated list of Slack channel names to send alerts to when the application is created |
| on_deployed_slack | Semicolon separated list of Slack channel names to send alerts to when the application is deployed |
| on_deleted_slack | Semicolon separated list of Slack channel names to send alerts to when the application is deleted |
| on_health_degraded_slack | Semicolon separated list of Slack channel names to send alerts to when the application is degraded |
| on_sync_failed_slack | Semicolon separated list of Slack channel names to send alerts to when the application undergoes a sync failure |
