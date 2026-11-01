# Recreate a local training environment

This guide uses the current upstream DVWA project. It is a recreation path, not a claim that the historical Ubuntu VM or exact old container image has been restored. No vulnerable service was started during portfolio preparation.

## Prerequisites

Use an Ubuntu training VM with Git, Docker, and Docker Compose installed. Keep the training application on loopback and use only lab accounts. Follow the [official DVWA instructions](https://github.com/digininja/DVWA#docker) for current requirements.

## Start and record the environment

```bash
git clone https://github.com/digininja/DVWA.git
cd DVWA
git rev-parse HEAD
docker version
docker compose version
```

Record the commit and versions for reproducibility. Inspect `compose.yml` before starting: the upstream web binding should remain `127.0.0.1:4280:80`.

```bash
docker compose up -d
docker compose ps
```

Open `http://127.0.0.1:4280` inside the Ubuntu VM and follow the application's setup instructions. This port differs from the original report's port 8080. Stop the lab with `docker compose stop` when finished. The upstream [Compose configuration](https://github.com/digininja/DVWA/blob/master/compose.yml) was checked on 1 November 2026.

## Record a bounded assessment

Keep Burp's scope restricted to this local lab endpoint. Document the selected DVWA security level, test account, small test set, observed failure behavior, and confirmation of a successful training login. Preserve private session data locally. Use [PortSwigger's Intruder documentation](https://portswigger.net/burp/documentation/desktop/tools/intruder) for the tool's interface.

The current upstream image may behave differently from the older application shown in the report. Treat differences as new observations rather than claiming an exact historical replication.

The original report's startup screenshot shows the historical `vulnerables/web-dvwa` image. The recreation steps above deliberately use the current DVWA upstream project instead of presenting that older image as a maintained setup.
