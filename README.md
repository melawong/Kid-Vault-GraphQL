# Welcome To Kid Vault

This **StepZen GraphQL API** serves as the middle layer for the **Kid Vault** app, which was built as part of the StepZen Challenge 2022.

The frontend and backend code repositories can be viewed here:
- [React Frontend](https://github.com/melawong/mom-api-frontend)
- [Flask Backend](https://github.com/anita-lee/mom_api2)

The deployed version of the Flask backend with a mock Postgres database is viewable here:
- [Heroku Backend with Postgres data](https://test-mom-api.herokuapp.com/)

`NOTE:` *Heroku often takes some time to wake up! Don't forget to give it a minute.*

The deployed version of our app is viewable here:
- [Kid Vault](https://kidvault.surge.sh/)

---
To install this repository on your computer, please follow these instructions:

### Installing StepZen

If you haven't already, be sure to sign up for and install StepZen.

[Detailed StepZen installation instructions are available here.](https://stepzen.com/docs/quick-start/install-and-setup)


### Running this STEPZEN API

1. [Register for COVID Act Now](https://apidocs.covidactnow.org/) to get your API key.

2. Setup your [Flask Backend](https://github.com/anita-lee/mom_api2) with your Postgres database.
    - *You can choose to seed with our mock data .csv file or add your own, but you'll need our schemas/tables for this API to function properly!*

3. Run stepzen:

```
$ stepzen start
```

4. Create .env file with:
```
STEPZEN_COVID_API_KEY=[YOUR_API_KEY_HERE]
```

Create config.yaml file with:
```
configurationset:
  - configuration:
      name: postgresql_config
      uri: [YOUR_POSTGRES_DB_URI_INFO_HERE]
  - configuration:
      name: covid_api_config
      apiKey: STEPZEN_COVID_API_KEY
```
`NOTE:` *Don't forget to add the config.yaml and .env to a .gitignore file!*

