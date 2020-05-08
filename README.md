# Findr Cordova App

- FINDR: Cordova iOS or Android App
- Using Cordova, Geolocation, and Google Maps JS API

```
package name:  com.algonquin.[your username].findr
github repo:  https://www.github.com/[your username]/findr
App name: Findr-[your username]
```

## References

[Cordova Reference for CSP and Android from MAD9022](https://prof3ssorst3v3.github.io/mad9022/modules/week2/#cordova-file-handling)

[Cordova Reference for iOS from MAD9022](https://prof3ssorst3v3.github.io/mad9022/modules/week4/#ios)

[Cordova Official Documentation](https://cordova.apache.org/docs/en/latest/)

[Geolocation Reference from MAD9014](https://prof3ssorst3v3.github.io/mad9014/modules/week10/geolocation.html)

[Google Maps Playlist](https://www.youtube.com/watch?v=EwZUQuPjakg&list=PLyuRouwmQCjkT4oMPGc1_4yggaFTLyZNh)

## App Description

This app will only have one screen. The whole screen will be filled with an interactive Google Map.

Use CSS to make the Map fill the whole width and height of the screen. See the example below.

```css
#map {
  width: 100vw;
  height: 100vh;
}
```

Next, use Geolocation and center the map on the user's current location.

Add a marker at the user's current location.

The map should let the user use the pinch gesture for zooming. Double tapping will be used for something else.

Double tapping on the map will add new markers to the map. The new markers should be a different colour than the current location marker.

Let the user enter a label for that marker. The coordinates for the tap and the label need to be saved in localStorage. This way, every time the app loads it can add the markers to the map that were saved previously.

The data in localStorage should be a single array of objects saved under a single unique key. Here is an example of what the data could look like.

```json
[
  {
    "id": 1570111234780,
    "label": "place name",
    "latlng": "45.3853206,-75.7003327"
  },
  {
    "id": 1570111299555,
    "label": "not the same place",
    "latlng": "46.3853206,-75.5004445"
  },
  {
    "id": 1570444444780,
    "label": "further west",
    "latlng": "43.3853206,-77.70011111"
  }
]
```

You should use the Cordova `dialog` plugin and its `prompt()` method to collect the label OR a modal window with a form input.

[Reference for the Dialog plugin](https://prof3ssorst3v3.github.io/mad9022/modules/week5/#cordova-dialog-plugin)

Each marker needs to have an InfoWindow which will appear when the marker is tapped. Inside the InfoWindow you should display the label that was entered and a button or link that can be tapped to remove the marker from the map and localStorage.

## Getting Started

Start on paper. Plan the app, the components, the interface, the functions, and any global variables.

- Clone this repo to your computer.
- Delete the `.git` folder.
- Create your own private repo on GitHub and copy the url.
- Run the following commands after creating your private repo.

```
git init
git remote add origin <the url for your private repo>
git add .
git commit -m 'create starter files'
git push origin master
cordova platform add <platform of your choice>
cordova plugin add cordova-plugin-dialogs
cordova plugin add cordova-plugin-geolocation
```

- Now you should be ready to start your coding.
- Remember to frequently update your repo.

```
git status
git add .
git commit -m 'message about what feature you just updated'
git push origin master
```

## Submission

Invite Steve to your private repo.

Send Steve an email when you are done.
