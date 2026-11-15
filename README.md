# Canal OTA Console AD

Canal de mise a jour sans fil pour la Switch d'Adrien.
- `manifest.json` : build courant, version, lien du zip, sha256.
- Les payloads sont des *releases* GitHub (assets `payload.zip`).

L'homebrew **Console AD - Mise a jour** sur la console lit le `manifest.json` brut,
compare le `build`, telecharge le zip, verifie le sha256, extrait a la racine de la SD, reboote.

Publier une MAJ depuis le Mac :
```
python3 tools/make_update.py <dossier_payload> --notes "ce que ca change"
```
