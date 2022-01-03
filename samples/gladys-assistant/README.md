# Deploy Gladys Home Assistant

[Gladys](https://gladysassistant.com/)) is a privacy-first, open-source home assistant.

## Prerequisites

- Account in [Synpse](https://cloud.synpse.net)
- Ensure you have a project and namespace ready (we create them by default once you log-in)

## Deployment

This deployment sample will:
- Create a Gladys container
- Data will be stored in `/data/gladysassistant` directory on the device

<a href="https://cloud.synpse.net/deploy?fileUrl=https://raw.githubusercontent.com/synpse-hq/synpse/main/samples/gladys-assistant/gladys.yaml" rel="noopener" target="_blank">
  <img src="https://storage.googleapis.com/synpse-misc/deploytosynpse.png"/>
</a>


## Next steps

Login using the device IP and port 8080 (http://device-ip:8080), create your initial user. Once that's created, you can use device tunnel to expose it to the internet so you can access to it remotely.

Useful links:
- Documentation on deploying Gladys via Synpse: https://docs.synpse.net/examples/home-automation/gladys-assistant
- Gladys docs: https://gladysassistant.com/docs/