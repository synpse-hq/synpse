# Drone server Synpse

How to run [Drone](https://readme.drone.io/) on Synpse

1. Create secret with github credentials configuration:
```
synpse secret create drone-gh-secret -f samples/prometheus/prometheus-config.yaml
```

1. Create Prometheus deployment:
```
synpse deploy -f samples/prometheus/prometheus-synpse.yaml
```

# Expose with domain

To expose your Prometheus you can use [Webhookrelay](https://webhookrelay.com/)

1. Register and login to WHR

1. Create bidirectional tunnel with custom domain. Set destination to `http://prometheus:9090`

1. Create token to configure your tunnel

1. Create secrets `relaySecret` and `relayKey`:

```
synpse secret create relaySecret -v RELAYSECRET
synpse secret create relayKey -v RELAYKEY
```

1. Change `prometheus-synpse-webhookrelay.yaml` to point to your tunnel:
```
    - name: relayd
      image: webhookrelay/webhookrelayd-aarch64:1
      args:
        - --mode
        - tunnel
        - -t
        - <tunnel_name>
```

1. Deploy `prometheus-synpse-webhookrelay.yaml` to Synpse!