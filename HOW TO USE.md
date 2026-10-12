# RB4DX Song Creator - How to use

Turns an MP3 into a playable Rock Band 4 (RB4DX) custom song for a jailbroken PS4.
MP3 -> auto-made chart -> Rock Band 3 CON -> PS4 `.pkg` -> (optional) sent to your PS4.

## Before you start
- Windows PC and a PS4 on the same network (only needed for sending).
- PS4 jailbroken (GoldHEN) with Rock Band 4 (CUSA02084) installed and an FTP server running (port 2121).
- No Python or other installs needed - everything is bundled. Keep the whole folder together.

## Make a song
1. Open `SongTool.exe`.
2. Drag one or more MP3s (or a whole folder of MP3s) onto the window, or click the drop area / **BROWSE...** (Ctrl+O).
3. A **Check song details** window appears for each song:
   - Edit **artist** and **title**. **LOOK UP** fills artist, title, year and genre from iTunes.
   - **ART...** lets you pick your own cover image (otherwise iTunes art is used if found).
   - Set **genre**, **year** and **preview start** (seconds into the song for the menu preview). **PLAY / STOP** lets you listen to find the spot.
   - **Chart**: Easier, Normal or Busier for that song.
   - An orange warning means a very short or low-quality MP3. You can still continue.
4. Press **CONVERT** (or Enter). Progress shows in the list and bar. Takes about 20-30 seconds per song.
5. Your package is in the `PS4 Packages` folder.
   Songs already built with identical settings are skipped, so re-running is instant.

## Send to the PS4
- Tick **Send to PS4 after building** and enter your PS4 IP, or use **SEND PKG TO PS4...** to send any existing `.pkg`.
- Use **TEST PS4** first: it checks the FTP connection and that Rock Band 4 is installed.
- On the PS4, install the pkg from **Debug Settings > Game > Package Installer** (files are uploaded to `/data/pkg`).
- **PS4 SONGS** lists and deletes the `.pkg` files in `/data/pkg`.
- **EU PS4**: tick if your Rock Band 4 is the European version.

## Other features
- **BUNDLE all songs into ONE package**: combines everything you add into one pkg with the pack name you type.
- **WEB SEARCH**: finds free / Creative Commons music (Internet Archive, Jamendo) and converts it. Jamendo needs a free client id in `jamendo_key.txt`. Only use music you have the right to use.
- **CANCEL** stops a running conversion.
- **COPY LOG**: copies the log to paste in a bug report.
- **CLEAN UP**: deletes the temporary `build` folder.
- **HELP / REPORT BUG**: opens the Discord (link in `discord.txt`).
- Settings (IP, send, bundle, chart level, EU) are remembered in `settings.ini`.

## Troubleshooting
- **Build failed on a very short song**: songs under about 30 seconds don't build. Use a full-length track.
- **Can't reach the PS4**: check the IP, that the FTP server is running (port 2121), and use TEST PS4. You can still convert and copy the pkg manually.
- **Song doesn't show in game**: make sure the pkg is installed, then restart Rock Band 4.
- **Anything else**: press **COPY LOG** and post it with HELP / REPORT BUG.

Made by CoronaSend.
