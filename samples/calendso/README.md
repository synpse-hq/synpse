# Deploy personal calendar booking

Calendso (now known as [Cal.Com](https://cal.com/)) is an open source Calendly alternative. You are in charge of your own data, workflow and appearance. Synpse makes it easy to host on your own hardware.

## Prerequisites

- Account in [Synpse](https://cloud.synpse.net)
- Ensure you have a project and namespace ready (we create them by default once you log-in)
- DNS name (you will want to access it remotely)

## Deployment

This deployment sample will:
- Create a calendso container
- Create a Postgres instance (data will be persisted on the host's `/data/calendso-postgres` path)
- Create a [Prisma](https://www.prisma.io/studio) container through which you will be able to manage the data 

<a href="https://cloud.synpse.net/deploy?fileUrl=https://raw.githubusercontent.com/synpse-hq/synpse/main/samples/calendso/calendso-synpse-caddy.yaml" target="_blank">
  <img src="https://storage.googleapis.com/synpse-misc/deploytosynpse.png"/>
</a>


## Next steps

You will need to create a user through Prism and configure Google authentication to sync with your calendar. You can find a more detailed guide here: https://synpse.net/blog/self-hosting-calendso-caddy.