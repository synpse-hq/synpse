# Drone server Synpse

How to run [Drone](https://readme.drone.io/) on Synpse

See [webhookrelay sample](../webhookrelay/) for Webhook relay part of the deployment.

1. Create secret with github credentials configuration.
See [github docs](https://docs.github.com/en/developers/apps/getting-started-with-apps/differences-between-github-apps-and-oauth-apps) how to create one.

```
synpse secret create droneClientID -v DRONE_GITHUB_CLIENT_ID
synpse secret create droneSecret -v DRONE_GITHUB_CLIENT_SECRET
```
```

To expose your Drone you can use [Webhookrelay](https://webhookrelay.com/)

1. Register and login to WHR

1. Create bidirectional tunnel with custom domain. Set destination to `http://prometheus:9090`

1. Create token to configure your tunnel

1. Create secrets `relaySecret` and `relayKey`:

```
synpse secret create relaySecret -v RELAYSECRET
synpse secret create relayKey -v RELAYKEY
```

1. Change `drone-synpse.yaml` to point to your tunnel:
```
    - name: relayd
      image: webhookrelay/webhookrelayd-aarch64:1
      args:
        - --mode
        - tunnel
        - -t
        - <tunnel_name>
```

1. Deploy Drone to Synpse!

1. Create Drone deployments:
```
synpse deploy -f samples/drone/drone-synpse.yaml
synpse deploy -f samples/drone/drone-runner-synpse.yaml
```
