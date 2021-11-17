# mc.yohane.su

![](https://img.shields.io/uptimerobot/status/m787979705-dedee70ce3309167bafdd585?label=Port%20Status)
![mc.yohane.su](https://img.shields.io/endpoint?url=https%3A%2F%2Fminecraft-server-status-badge.vercel.app%2Fapi%2Fserver%2Fmc.yohane.su%3Fport%3D25565)

my minecraft server

## status

- [Uptime Robot](https://stats.uptimerobot.com/QLk7XC6Kxv/787979705)
- [Grafana Dashboard](https://grafana.sksat.net/goto/aq1Idnknk?orgId=1)

![JVM memory](https://grafana.sksat.net/render/d-solo/BIXBinz7z/minecraft?orgId=1&refresh=30s&from=1624651161148&to=1624652961148&panelId=5&width=400&height=200&tz=Asia%2FTokyo)
![Players](https://grafana.sksat.net/render/d-solo/BIXBinz7z/minecraft?orgId=1&refresh=30s&from=1624651161148&to=1624652961148&panelId=1&width=400&height=200&tz=Asia%2FTokyo)

![Loaded Chunks](https://grafana.sksat.net/render/d-solo/BIXBinz7z/minecraft?orgId=1&refresh=30s&from=1624651161148&to=1624652961148&panelId=3&width=260&height=300&tz=Asia%2FTokyo)
![Entities](https://grafana.sksat.net/render/d-solo/BIXBinz7z/minecraft?orgId=1&refresh=30s&from=1624651161148&to=1624652961148&panelId=4&width=260&height=300&tz=Asia%2FTokyo)
![Villagers](https://grafana.sksat.net/render/d-solo/BIXBinz7z/minecraft?orgId=1&refresh=30s&from=1624651161148&to=1624652961148&panelId=11&width=260&height=300&tz=Asia%2FTokyo)


## setup & start

Deploy Machine
```sh
### deps: docker, docker-compose
### deps(backup service): systemd, rclone
$ ./setup.sh
$ docker-compose up -d
```

:bulb: It is highly recommended to use [compose-cd](https://github.com/sksat/compose-cd) for continuous deployment.

Expose Machine
```sh
### deps: systemd, cloudflared
$ cp ./minecraft-expose.service ~/.config/systemd/user/
$ systemctl --user enable --now minecraft-expose
```

## maintenance

```sh
$ ./cmd.sh say hello
```

or use [mcrcon](https://github.com/Tiiffi/mcrcon)

## how to join

Edit [whitelist.json](https://github.com/sksat/mc.yohane.su/blob/main/data/whitelist.json) and send a pull request

## links

- container image: [papermc-docker](https://github.com/sksat/papermc-docker)
- deploy automation script: [compose-cd](https://github.com/sksat/compose-cd)
- whitelist.json check Action: [minecraft-whitelist-validator](https://github.com/sksat/minecraft-whitelist-validator)
- blog: [マイクラサーバをGitHubで運用する](https://sksat.hatenablog.com/entry/2021/08/26/015620)
