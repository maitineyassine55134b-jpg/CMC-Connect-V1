# CMC Connect – Application Android

Application Android (WebView) qui affiche le prototype **CMC Connect** du CMC Tamesna.

## Structure

- `app/src/main/assets/index.html` : le prototype web (à remplacer, voir ci-dessous)
- `app/src/main/java/ma/cmc/connect/MainActivity.kt` : activité principale
- `.github/workflows/android.yml` : compilation automatique de l'APK

## 1. Mettre le prototype dans l'application

Copiez votre fichier `cmc-connect.html` dans `app/src/main/assets/` et renommez-le `index.html` (en remplaçant le fichier existant).

## 2. Publier sur GitHub

```bash
git init
git add .
git commit -m "CMC Connect – version initiale"
git branch -M main
git remote add origin https://github.com/VOTRE-COMPTE/CMC-Connect.git
git push -u origin main
```

## 3. Récupérer l'APK

Sur GitHub : onglet **Actions** → workflow **Build APK** → cliquez sur la dernière exécution → section **Artifacts** → téléchargez `CMC-Connect-debug` (contient `app-debug.apk`).

Vous pouvez aussi lancer la compilation manuellement via **Actions → Build APK → Run workflow**.

## 4. Installer sur Android

Transférez `app-debug.apk` sur le téléphone, autorisez l'installation depuis une source inconnue, puis installez-le.

## Compiler en local (optionnel)

Avec Android Studio : **File → Open** puis sélectionnez le dossier du projet, et cliquez sur **Run**.

## Notes

- La connexion Gmail du prototype est simulée. Une vraie connexion Google nécessitera un backend et un identifiant OAuth.
- Pour publier sur le Play Store, il faudra générer un APK/AAB signé (`assembleRelease` avec un keystore).
