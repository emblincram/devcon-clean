# devcon-clean

Minimales Ubuntu-Basisimage fuer einen sauberen Start ohne vorinstalliertes Entwicklungs-Tooling.

## Zweck

- Testen mit moeglichst wenig vorgegebenen Abhaengigkeiten.
- Ausgangsbasis fuer eigene, schlanke Container.

## Inhalt

- Basis: `ubuntu:22.04`
- Kaum zusaetzliche Konfiguration im Dockerfile
- Build/Push per GitHub Action nach GHCR

## Lokal bauen

Aus dem Repo-Root:

```bash
docker build -t devcon-clean:local -f .devcontainer/Dockerfile .
```

## GHCR Push (lokal)

Das Hilfsskript liegt in `.devcontainer/rebuild-image.sh` und erwartet `GITHUB_TOKEN`:

```bash
export GITHUB_TOKEN=<token_mit_packages_write>
bash .devcontainer/rebuild-image.sh
```

## Hinweis

Dieses Repo ist ein Docker-Image-Repo. Ein `devcontainer.json` ist nicht vorhanden.
