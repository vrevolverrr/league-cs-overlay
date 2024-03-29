<h1 align="center">Creep Score Overlay</h1>

<p align="center">
  <b><small>✨ An overlay to show average creep score per minute in League of Legends ✨</small></b>
</p>

## Usage
Download the latest release [here](https://github.com/vrevolverrr/LeagueCSOverlay/releases/tag/v0.0.1) and run the executable! To change the font size, open notepad and type in your desired font size then save the file as "font.cfg" without double quotes in the same directory as the executable.

## Limitations
Currently only supports fullscreen borderless 1920x1080 resolution

## Explanation
A screnshot of the in game creep score counter is taken. The screenshot is cropped so that each frame only contains one digit exactly (10 px wide by 12 px tall).

<p align="center">
  <img src="https://raw.githubusercontent.com/vrevolverrr/LeagueCSOverlay/main/docs/example.png"></img>
</p>

The grayscale of the cropped frames are then compared to grayscale of target frames consisting of digits 0-9 and blank (no digit) to find the most similar digit. This is done by calculating the mean squared error (MSE) between the observed frame and each target frame.

The resulting number is then divided by the game time which is obtained through the game's [LiveClientAPI](https://developer.riotgames.com/docs/lol#game-client-api_live-client-data-api) to obtain the average creep score per minute.

The overlay is just a transparent Tkinter window. 

<p align="center">
  <sub><strong>Made with ❤️ Bryan Soong</strong></sub><br>
</p>