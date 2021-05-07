# TestNearU-DeltaHacks 

## Goal

The goal of the application is the location all the COVID-19 testing locations in Ontario. I have noticed that is was quite difficult trying to find the testing locations from the government website since enough information was not provided for users. In order to resolve this issue I created an application that is easy to use so users can easily locate the location and book an appointment for a covid test through phone. This is project is part of the Delta Hacks hackathon. Since the theme of the hackathon is meant to be related to health it would be a great idea to connect the project to something health related. 

## How

There were multiple Technologies that were involved in the making of this project. One of the key requirements for Delta Hacks was to enforce security on the project and one of the best ways to do this was to use Firebase Authentication. After setting up authentication I had to store the testing locations data that I retrieved from the Ontario website as a JSON file. I knew that I would need a database of some sort however I didn’t have experience with MongoDB or other types of database. The easiest and fastest way to setup a database is using Firebase real-time database, so I ended up uploading the JSON file and firebase organized it automatically. After completing all the setups it was finally time to begin coding the website using React for the client-side and invoking the Google Maps Javascript API to display the testing locations on a map. Then I utilized an open source library react-google-maps to display the markers along with the information as an infowindow. 

## Learning

There was lots to learn from this project because I was working with some of these technologies for the first time. I have not worked with firebase before this so I learned how to setup authentication to secure an application. I have always felt the need to use databases in my projects but since I didn’t know MySQL, MongoDB or any other type of database. So it was great to gets my hand on firebase database and play around with the data and use it to my advantage which gives your project such an advantage. 

## Challenges

This project may seem quite easy to do however there are many challenging aspects to it that I have faced on the making of the project.

The first challenging obstacle is that it was quite difficult  getting the data( longitude, latitude) from the firebase to place the markers because there was no possible way to map over index values on the data that was on firebase. In order to resolve this issue I had to bring the latitude and longitude section as a JSON file and store it on the project as a local file which made it much easier to just map over and display all the markers. 

Another major challenge I faced was that when a user clicks on a marker the information should show up about the testing location however for some reason it wouldn’t work with the library that I choose. Initially I choose to work with Google Maps React library but the infowindow feature on it was broken which I realized after doing some in-depth research. The only solution for this was for me to switch to another Library called React Google Maps. This took a long time because I had to switch up the code I already wrote and do it again. Finally after switching libraries I was able to have a well functioning application.   

## Tools and Technologies

- React
- Node.js
- Firebase Authentication
- Firebase Realtime Database
- Google Maps JavaScript API
- React Google Maps Library
- Vercel


## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.
