# Grafana Synpse

How to run Grafana on Synpse

1. Create secret with Grafana configuration:
```
synpse secret create grafana-config -f samples/grafana/grafana.ini
```

! Important to know about grafana Config is that once started it will not accept changes.

1. Create Grafana deployment:
```
synpse deploy -f samples/grafana/grafana-synpse.yaml
```

# Expose with domain

To expose your Grafana you can use
[Webhookrelay](https://webhookrelay.com/)

1. Register and login to WHR

1. Create bidirectional tunnel with custom domain. Set destination to `http://grafana:3000`

1. Create token to configure your tunnel

1. Create secrets `relaySecret` and `relayKey`:

```
synpse secret create relaySecret -v RELAYSECRET
synpse secret create relayKey -v RELAYKEY
```

1. Change `grafana-synpse-webhookrelay.yaml` to point to your tunnel:
```
    - name: relayd
      image: webhookrelay/webhookrelayd-aarch64:1
      args:
        - --mode
        - tunnel
        - -t
        - <tunnel_name>
```

1. Deploy `grafana-synpse-webhookrelay.yaml` to Synpse!