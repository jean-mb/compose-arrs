# Setup Ecossitema *arr + QBitTorrent + Plex Media Server
Setup do ecossistema *arr (Sonarr, Radarr Prowlarr, Overseerr) junto com Plex e QBitTorrent

## Features:
Contém:
- [QBitTorrent](https://www.qbittorrent.org/), como cliente de download torrent.
- [Prowlarr](https://github.com/Prowlarr/Prowlarr), como navegador/centralizador de indexadores torrent.
- [Radarr](https://radarr.video/), como monitor de filmes.
- [Sonarr](https://sonarr.tv/), como monitor de séries.
- [Plex](https://www.plex.tv/), como servidor de streaming de mídias.
- [Overseerr](https://overseerr.dev/), como interface para requisitar mídias.
  
## Importante: 
- Os caminhos de diretórios foram pensados para execução em ambiente / sistema de arquivos Linux. Caso o uso seja em Windows, ajustar os mapemeamentos em todos os ```volumes``` para caminhos do Windows
- Ao alterar qualquer mapeamento de volume de qualquer serviço, verificar os demais serviços, pois a inter-comunicação dos serviços acontece via esses diretórios:
 - Radarr e Sonarr monitoram os diretórios de downloads e filmes e séries do QBitTorrent

   ```/DATA/Media/SeriesDownloads```
   
   ```/DATA/Media/FilmesDownloads```
   
 - Plex faz streaming dos arquivos dos dirétorios de filmes e séries do Radarr e Sonarr

   ```/DATA/Media/Filmes```

   ```/DATA/Media/Series```
   
## Setup
Documentação do Docker Compose: [Documentação](https://docs.docker.com/compose/)

Baixe o arquivo e execute no diretório:
```docker-compose up -d```
