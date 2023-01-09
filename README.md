<div align="center">

  <img src="https://github.com/synpse-hq/synpse/blob/main/assets/logo.png" width="200px">
  <br>

  **The easiest way to bootstrap your devices and deploy applications.
  Synpse manages OTA deployment & updates, provides SSH and network access.**

  ---

  <p align="center">
    <a href="https://synpse.net">Website</a> •
    <a href="#samples">Samples</a> •
    <a href="https://github.com/synpse-hq/synpse/discussions">Discussions</a> •
    <a href="https://docs.synpse.net">Docs</a> •
    <a href="https://discord.gg/dkgN4vVNdm">Discord</a> •
    <a href="https://cloud.synpse.net/">Cloud</a> •
    <a href="https://buymeacoffee.com/synpse">Buy us a COFFEE</a>
  </p>

</div>


## Synpse.NET - device orchestration for the rest of us

Synpse provides your device fleet management, application deployment and their configuration. Whole process is simple with very low learning curve.

## Key features

- Device inventory management: each of your device will register as an entry in our database and will be visible via UI/CLI/Dashboard.
- SSH/TCP connections to your devices via tunnels: you don't need to have a public IP on your device to have access to it.
- Declarative application deployment: store your manifests in GitHub, Gitlab or any other SCM repository, deploy applications via UI or CLI.
- Device filtering for grouping and application scheduling: use labels and selectors to deploy applications to a subset of your devices for A/B testing.
- Secret management: Synpse provides encrypted secret store to provide sensitive configuration to your applications.
- Namespaces: separate your applications and secrets using namespaces on the same device.

## Supported platforms

Synpse currently supports all Linux based distributions. It's possible to run it on Darwin (MacOS) systems too, but you will need to install the agent as a daemon yourself.

Windows support is planned, using binary executable drivers, however it's not a prioritized feature yet. If you would like to see Windows support implemented sooner, please contact us.

<table>
  <thead>
    <tr>
      <th>Platform</th>
      <th>Architecture</th>
      <th>Status</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td rowspan="3">Linux</td>
      <td><code>amd64</code></td>
      <td>✅</td>
    </tr>
    <tr>
      <td><code>aarch64</code></td>
      <td>✅</td>
    </tr>
     <tr>
      <td><code>arm32</code></td>
      <td>✅</td>
    </tr>
    <tr>
      <td rowspan="2">Darwin</td>
      <td><code>amd64</code></td>
      <td>⏳</td>
    </tr>
    <tr>
      <td><code>aarch64</code></td>
      <td>⏳</td>
    </tr>
    <tr>
      <td>Windows</td>
      <td><code>amd64</code></td>
      <td>⏳</td>
    </tr>
  </tbody>
</table>

## Samples

You can view samples of applications deployed on Synpse in the [samples/](https://github.com/synpse-hq/synpse/tree/main/samples) directory. Feel free to submit a pull request with your favorite app!

- [Cal.com](samples/calendso) - easy meeting scheduling
- [Grafana](samples/grafana) - monitoring/metrics stack
- [Clickhouse] (samples/clickhouse) - column-oriented database management system (DBMS)
- [Prometheus](samples/prometheus) - metrics collector, database and query engine
- [Home Assistant](samples/home-assistant) - self-hosted home automation hub that supports thousands of integrations
- [Gladys Home Assistant](samples/gladys-assistant) - a lightweight and privacy focused home assistant
- [Node-RED](samples/node-red) - no-code automation solution for anything from home automation to industrial applications
- [ownCloud](samples/owncloud) - privacy focused essential business tool
- [Firefox](samples/firefox) - web browser
- [Drone CI/CD](samples/drone) - self-hosted CI/CD solution
- [Jupyter Labs](samples/jupyterlab/) - web-based interactive development environment for Jupyter notebooks
- [piHole](samples/pihole) - network wide ad blocking
- [uptime-kuma](samples/uptime-kuma) - self-hosted monitoring solution for your websites (uptimerobot/pingdom alternative)
- [webhookrelay](samples/webhookrelay) - integration with webhookrelay

## Community

Synpse is a young project and our community is constantly growing. Join our [Discord channel](https://discord.gg/dkgN4vVNdm) or participate in [GitHub Discussions](https://github.com/synpse-hq/synpse/discussions).

## Bug reporting/getting help

If you get stuck or not sure how to achieve something or just want to request a new feature, you can try:

1. Read the docs: https://docs.synpse.net
2. Submit an issue here: https://github.com/synpse-hq/synpse/issues
