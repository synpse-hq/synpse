# Deploy personal uptime monitoring

![screenshot](uptime-kuma.png)

[Uptime-Kuma](https://github.com/louislam/uptime-kuma) is an Open-Source self-hosted uptime monitoring tool. It can periodically check your websites and alert you when services go down.

## Prerequisites

- Account in [Synpse](https://cloud.synpse.net)
- Ensure you have a project and namespace ready (we create them by default once you log-in)

## Deployment

This deployment sample will:
- Create a uptime-kuma container (data will be persisted on the host's `/data/uptime-kuma` path)

<a href="https://cloud.synpse.net/deploy?fileUrl=https://raw.githubusercontent.com/synpse-hq/synpse/main/samples/uptime-kuma/uptime-kuma.yaml" rel="noopener" target="_blank">
  <img src="https://storage.googleapis.com/synpse-misc/deploytosynpse.png"/>
</a>


## Next steps

Login by opening your http://[device IP]:3001 address. Then, create an account there and start adding your monitors:
