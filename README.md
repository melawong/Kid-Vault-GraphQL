# Welcome To Kid Vault

This **StepZen GraphQL API** serves as the middle layer for the **Kid Vault** app, which was built as part of the StepZen Challenge 2022.

The frontend and backend code repositories can be viewed here:
- [React Frontend](https://github.com/melawong/mom-api-frontend)
- [Flask Backend](https://github.com/anita-lee/mom_api2)

The deployed version of the Flask backend with a mock Postgres database is viewable here:
- [Heroku Backend with Postgres data](https://test-mom-api.herokuapp.com/)

*Note: Heroku often takes some time to wake up! Don't forget to give it a minute.*


To install this repository on your computer, please follow these instructions:

### Installing StepZen

If you haven't already, be sure to sign up for and install StepZen.

[Detailed StepZen installation instructions are available here.](https://stepzen.com/docs/quick-start/install-and-setup)


### Running the STEPZEN API

1. [Register for COVID Act Now](https://apidocs.covidactnow.org/) to get your API key.

Create .env file with:
```
STEPZEN_COVID_API_KEY=[YOUR_API_KEY_HERE]
```

Then run stepzen:

```
$ stepzen start -p 5002
```

3. React Front-End => mom-api-frontend

### Installing Dependencies

```
npm install
```

### Running the Front End

Create .env file with:
```
REACT_APP_API_KEY=*******
REACT_APP_BASE_URL=*******
```
******** = Provide your own.

Then run React:

```
$ npm start
```
