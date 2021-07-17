# Home Assistant on Synpse

[Home Assistant](https://www.home-assistant.io/) is a popular open-source home automation tool. 

It can either be installed as a "Home Assistant Operating System" that strictly limits what else you can do with your device or you can choose to install it as a [container](https://www.home-assistant.io/installation/linux#install-home-assistant-container) through Docker.

## Deployment

Use `ha-synpse.yaml` to deploy a containerized version of Home Assistant. Once deployed, you can access it using `http://<device IP>:8123`. Next steps can be found in [Home Assistant official docs](https://www.home-assistant.io/getting-started/onboarding/).


## Expose with domain

To expose your [Home Assistant](https://www.home-assistant.io/) you can use
[Webhookrelay](https://webhookrelay.com/)

1. Register and login to WHR

1. Create bidirectional tunnel with custom domain. Set destination to `http://homeassistant:8123`

1. Create token to configure your tunnel

1. Create secrets `relaySecret` and `relayKey`:

```
synpse secret create relaySecret -v RELAYSECRET
synpse secret create relayKey -v RELAYKEY
```

1. Change `ha-synpse-webhookrelay.yaml` to point to your tunnel:
```
    - name: relayd
      image: webhookrelay/webhookrelayd-aarch64:1
      args:
        - --mode
        - tunnel
        - -t
        - <tunnel_name>
```

1. Deploy `ha-synpse-webhookrelay.yaml` to Synpse!