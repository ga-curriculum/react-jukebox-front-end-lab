# ![React Jukebox Lab - Exercise](./assets/hero.png)

## Introduction

Welcome to the Reactville Jukebox! In this lab, you'll be creating the front end of a collaborative, community-driven jukebox application. You have the option to design the user interface either as a dynamic dashboard with conditional rendering or by using React Router to manage different views for each function. Additionally, you'll complete the jukebox vibe by implementing a feature to display the currently "playing" track.

This lab is designed to give you practical experience in building a Single Page Application (SPA) using React and fetch to interact with the RESTful API developed in the [Express API - Jukebox Lab](https://git.generalassemb.ly/modular-curriculum-all-courses/express-api-jukebox-lab). As you build out the functions for creating, reading, updating, and deleting (CRUD) tracks, you'll see how your frontend interacts seamlessly with the backend, bringing the digital jukebox to life.

## Minimum Requirements

Depending on your chosen UI structure, the requirements will slightly differ. Below are the functionalities your application must support, with notes for both UI approaches and the new requirement for tracking the current track:

| Feature                   | Dashboard Requirements                                                                                                                                | React Router Requirements                                                                                       |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------- |
| **Read all Tracks**       | - Display all tracks in the main view                                                                                                                 | - Display all tracks on a dedicated 'All Tracks' page                                                           |
| **Read a Single Track**   | - Add a link to view details of a track within the same layout<br>- Use a conditionally rendered component based on user selection or interaction     | - Link to a separate 'Track Details' page that shows the details of the track                                   |
| **Create a New Track**    | - Display a form in a conditionally rendered component based on user interaction<br>- Handle the form submission<br>- Display the new Track in the UI | - Provide a form on a separate 'Add Track' page<br>- Redirect to the track list after submission                |
| **Update a Track**        | - Edit track details in a conditionally rendered component based on user interaction                                                                  | - Use a 'Edit Track' page with a form, save changes and then redirect back to the details or list page          |
| **Delete a Track**        | - Include a delete button next to each track<br>- Remove the track from the view using a conditionally rendered component based on user interaction   | - Include a delete option on each track's detail or list page, with a confirmation prompt                       |
| **Current Track Playing** | - Maintain a state variable for the current track playing<br>- Display this track in a prominent area of the UI                                       | - Maintain a state variable for the current track playing<br>- Display this track in a prominent area of the UI |

> Please note that this lab does not involve actual audio playback capabilities. It is designed as a UI simulation of a jukebox, focusing on the interaction with a music track database. The features implemented will simulate managing a playlist, but will not play music.

## Component Hierarchy

You can choose between maintaining a single-page flow with components that appear and disappear based on user actions, or implementing routing to navigate between different components representing pages. Here is an example structure for each option:

### Dashboard Style

- **App**
  - **TrackList**
  - **TrackForm** (conditionally rendered based on user interaction)
  - **TrackDetail** (conditionally rendered based on user selection)

### React Router Style

- **App**
  - **NavBar** (optional for navigation)
  - **Home** (route '/')
  - **TrackList** (route '/tracks')
  - **TrackDetail** (route '/tracks/:id')
  - **CreateTrack** (route '/add-track')
  - **EditTrack** (route '/edit-track/:id')

This lab offers you a chance to practice making design decisions based on user experience and functionality requirements. Whichever approach you choose, the key is to ensure that the application remains user-friendly and performs full crud functionality paired with the Express API.
