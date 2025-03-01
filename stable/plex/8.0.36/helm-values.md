# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.ALLOWED_NETWORKS | string | `"172.16.0.0/16"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/plex"` |  |
| image.tag | string | `"v1.25.3.5409@sha256:4bcec7172bffa2d847f07d6b86ea20a736e1cbf00ca51b2bf17c84ddd265c8b9"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| service.main.ports.main.port | int | `32400` |  |
| service.main.ports.main.targetPort | int | `32400` |  |

All Rights Reserved - The TrueCharts Project
