# ![React Jukebox Lab Front-End - Level Up](./assets/hero.png)

## Level Up: Enhance Your Jukebox

Ready to take your Reactville Jukebox to the next level? As you've built a solid foundation for managing and displaying tracks, now you can enhance the user experience by integrating more interactive and visual elements. Consider adding the following features to your front-end application:

### Display Cover Art

Show cover art for each track in the UI.

- **Update the Track Model**: Ensure your back-end model includes a `coverArtUrl` attribute.
- **Modify the Track Form**: Update the form used to add or update tracks to include an input field for the cover art URL.
- **Display in UI**: Modify the `TrackList` and `TrackDetail` components to display the cover art `img` associated with each track.

### Play Audio Clips

This is an ***advanced level up*** that requires the help of an outside API for music or sound clips.

Allow users to preview tracks by playing audio clips directly in the browser.

- **Update the Track Model**: Include a `soundClipUrl` attribute in your back-end model if not already present.
- **Modify the Track Form**: Ensure there is an input field in the form for users to add or update the URL of the audio clip.
- **Audio Playback in UI**: Implement an audio player in the `TrackDetail` component that uses the HTML `<audio>` element to play the sound clip. 

Here's an example of how to integrate a basic audio player component in React:

```jsx
<audio controls src={currentTrack.soundClipUrl}>
  Your browser does not support the audio element.
</audio>
```
