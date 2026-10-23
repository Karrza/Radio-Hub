Radio Hub

**A minimal internet radio player built into Spotify using Spicetify.**

Radio Hub lets you listen to internet radio stations from around the world without needing a separate radio application. Its interface is designed to fit naturally into Spotify, keeping things simple and easy to use.

## Features

- **Discover radio stations** — find internet radio stations from around the world.
- **My Radio Stations** — keep your own collection of saved stations.
- **Custom stations** — add stations and their stream URLs.
- **Station artwork** — personalize stations with your own cover images.
- **Station management** — remove stations whenever you want.
- **Spotify volume synchronization** — radio volume follows Spotify's volume slider.
- **Playback integration** — radio playback can pause automatically when Spotify music starts playing.
- **Minimal interface** — a clean design intended to feel at home inside Spotify.

![Radio Hub preview](photo.png)
## Requirements

- Spotify for Windows
- [Spicetify CLI](https://spicetify.app/docs/getting-started/)

## Installation

1. Open the Spicetify configuration directory by running this command in PowerShell or Terminal:

   ```powershell
   spicetify config-dir
   ```

2. Open the directory displayed by the command and navigate to `CustomApps`. Create the folder if it doesn't exist.

3. Inside `CustomApps`, create a folder named `RadioHub`.

4. Download the Radio Hub files from this repository:
   - Open the [Radio-Hub repository](https://github.com/Karrza/Radio-Hub).
   - Click **Code → Download ZIP**.
   - Extract the downloaded ZIP.

5. Copy the contents of the app's folder into:

   ```text
   CustomApps/RadioHub/
   ```

   Make sure `index.js`, `manifest.json`, and any other required app files are directly inside the `RadioHub` folder, not inside an extra nested folder.

6. Register Radio Hub with Spicetify:

   ```powershell
   spicetify config custom_apps RadioHub
   ```

7. Apply the changes:

   ```powershell
   spicetify apply
   ```

8. Completely close and reopen Spotify. Radio Hub should appear in the sidebar.

To get the direct stream url do this:
1. Open the radio page in Chrome and press F12.
2. Go to Network → Media (or All).
3. Start the radio and look for the active audio request.
4. Right-click it → Copy → Copy URL.
   
## Uninstallation

1. Completely close Spotify.
2. Open PowerShell or Terminal and run:

   ```powershell
   spicetify config-dir
   ```

3. Navigate to the `CustomApps` directory inside the displayed folder.
4. Delete the `RadioHub` folder.
5. Remove Radio Hub from Spicetify's enabled custom apps:

   ```powershell
   spicetify config custom_apps RadioHub-
   ```

6. Re-apply Spicetify:

   ```powershell
   spicetify apply
   ```

7. Reopen Spotify. Radio Hub should no longer appear in the sidebar.

**Important:** Back up your saved stations and artwork before deleting the app folder if your version stores its data there.

## Troubleshooting

- **Radio Hub doesn't appear:** Verify that the files are in the correct `CustomApps/RadioHub` directory.
- **The app appears blank:** Check that all required files were copied correctly and inspect any errors reported by Spicetify.
- **Radio doesn't play:** Some internet radio streams may be offline or incompatible.
- **Spotify updates cause problems:** Check for Spicetify updates and reapply your customizations if necessary.

## Disclaimer

Radio Hub is an independent community project. It is not affiliated with, endorsed by, or officially supported by Spotify.

## License

No license has been specified yet.
