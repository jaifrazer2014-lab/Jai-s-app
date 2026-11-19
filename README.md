# JAI Pocket Lab — AltStore Classic build

This project is designed to create an **unsigned iOS IPA** using a GitHub-hosted Mac runner, then let AltServer sign and install it. You do not need a Mac. You do need a Windows PC, a GitHub account, and AltStore Classic already installed on your iPhone.

## Part 1 — Upload the project to GitHub

1. Extract this ZIP on your Windows PC.
2. Open https://github.com and sign in (or create an account).
3. Create a new repository. Give it a name such as `jai-pocket-lab`. Keep it private if you prefer.
4. On the new repository page, choose **uploading an existing file**.
5. Upload the contents of this extracted folder, including the hidden `.github` folder. The `.github/workflows/build-ios.yml` file is important.
6. Commit the files to the repository.

If GitHub's browser uploader hides `.github`, create the folder and workflow using GitHub's **Add file → Create new file** option and name it exactly `.github/workflows/build-ios.yml`, then paste the workflow contents from this ZIP.

## Part 2 — Build the IPA

1. In your GitHub repository, open the **Actions** tab.
2. Select **Build unsigned iOS IPA** on the left.
3. Press **Run workflow**, then the green **Run workflow** button.
4. Wait for the workflow to finish. It may take several minutes.
5. Open the completed workflow run. At the bottom, find **Artifacts**.
6. Download `JAI-Pocket-Lab-unsigned-IPA`. Extract the downloaded artifact ZIP to get `JAI-Pocket-Lab-unsigned.ipa`.

## Part 3 — Install using AltStore Classic

1. On your Windows PC, make sure AltServer is installed and running. Use the official AltStore Windows guide: https://faq.altstore.io/altstore-classic/how-to-install-altstore-windows
2. Keep the PC and iPhone on the same Wi-Fi network, or connect the iPhone to the PC by USB.
3. Open AltStore on the iPhone.
4. Tap the **+** button in My Apps and select `JAI-Pocket-Lab-unsigned.ipa` from the Files app.
5. Follow the prompts. AltServer will sign the app with the Apple account configured in AltServer.

Keep AltServer available so AltStore can refresh the app. With a free Apple account, sideloaded apps generally need refreshing every 7 days. See the official AltServer guide: https://faq.altstore.io/altstore-classic/altserver

## Important notes

- Never share your Apple ID password, verification codes, or signing files with anyone. Enter account details only in the official AltServer/AltStore flow.
- If GitHub Actions reports a build error, open the failed run and copy the first red error section. Do not post any passwords or tokens.
- This project is a native app shell. Live maps and external lookups require internet.
- This version does not connect to your Raspberry Pi, Arduino, Windows PC, or printer.
- Some tiles are starter tools and some device-specific features are placeholders, not fully implemented hardware integrations.
