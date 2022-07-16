# Welcome To Kid Vault 

## ABOUT

This **StepZen GraphQL API** serves as the middle layer for the **Kid Vault** app, which was built as part of the StepZen GraphQL Challenge 2022.

The front-end and back-end code repositories can be viewed here:

- [Kid Vault Front-end](https://github.com/melawong/Kid-Vault-Frontend)
- [Kid Vault Back-end](https://github.com/anita-lee/mom_api2)

The deployed version of the Flask back-end with a mock Postgres database is viewable here:

- [Heroku Back-end with Postgres data](https://test-mom-api.herokuapp.com/)

`NOTE:` _Heroku often takes some time to wake up! Don't forget to give it a minute._

The deployed version of our app is viewable here:

- [Kid Vault](https://kidvault.surge.sh/)

---

## INSTALLATION

To install this repository on your computer, please follow these instructions:

### Installing StepZen

If you haven't already, be sure to sign up for and install StepZen.

[Detailed StepZen installation instructions are available here.](https://stepzen.com/docs/quick-start/install-and-setup)

### Running this STEPZEN API

1. [Register for COVID Act Now](https://apidocs.covidactnow.org/) to get your API key.

2. Setup your [Flask Back-end](https://github.com/anita-lee/mom_api2) with your Postgres database.

   - _You can choose to seed with our mock data .csv file or add your own, but you'll need our schemas/tables for this API to function properly!_

3. Create .env file with:

```
STEPZEN_COVID_API_KEY=[YOUR_API_KEY_HERE]
```

4. Create config.yaml file with:

```
configurationset:
  - configuration:
      name: postgresql_config
      uri: [YOUR_POSTGRES_DB_URI_INFO_HERE]
  - configuration:
      name: covid_api_config
      apiKey: STEPZEN_COVID_API_KEY
```

`NOTE:` _Don't forget to add the config.yaml and .env to a .gitignore file!_

5. Run stepzen:

```
$ stepzen start
```

6. Check your terminal for the `localhost:5001` address to enter the playground for the API!

---

## WOOHOO!

You Made It! Enjoy and please contact @melawong and @anita-lee with any issues or questions.
