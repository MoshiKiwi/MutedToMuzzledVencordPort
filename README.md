# MutedToMuzzled (PupCord)

A Vencord **QuickCSS stylesheet**, not a standalone Vencord plugin. It replaces Discord voice-control and participant-status icons with puppy-themed images.

## Icon mapping

| Discord state | PupCord icon |
| --- | --- |
| Microphone enabled | `bark.png` (Bark) |
| User-muted microphone | `dog.png` (Muzz) |
| Server-muted / channel permission blocks speaking | `dog.png` (Muzz) |
| Listening enabled | `cage2.png` (Cage) |
| Sound disabled / deafen active | `cage.png` (Caged) |

The same microphone/deafen mapping is applied to local controls and participant status icons. Local controls are selected by accessible action labels, including English and Russian microphone, mute, sound, and deafen wording, rather than by button position. This avoids treating an extra webcam control as the microphone or deafen button.

The stylesheet also changes voice-control tooltips to `Bark!!`, `Muzzled`, `Cage`, and `Caged`, and changes typing indicators to barking-themed text.

## Install

1. Open **Discord Settings → Vencord → Themes → Edit QuickCSS**.
2. Add this line at the very top of QuickCSS:

   ```css
   @import url("https://raw.githubusercontent.com/djdenicore/MutedToMuzzledVencordPort-Fix/master/MutedToMuzzled.css");
   ```

3. Save the file and reload Discord if the changes are not visible.

## Compatibility

- Uses modern CSS features including `:has()`, `:is()`, and CSS nesting.
- Discord may change generated class names, accessible labels, or SVG paths in client updates. The relevant selectors may then need updating.
- Puppy assets are hosted in [zoez22/muzzlemute](https://github.com/zoez22/muzzlemute).

## Credits

Based on the MutedToMuzzled BetterDiscord plugin by 1xzozz.
