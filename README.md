This **StepZen GraphQL API** serves as the middle layer for the **Kid Vault** app, which was built as part of the StepZen Challenge 2022.

The frontend and backend code repositories can be viewed here:
- [React Frontend](https://github.com/melawong/mom-api-frontend)
- [Flask Backend](https://github.com/anita-lee/mom_api2)

The deployed version of the Flask backend with a mock Postgres database is viewable here:
- [Deployed Backend with Postgres data](https://test-mom-api.herokuapp.com/)


To install this repository on your computer, please follow these instructions:

1. Flask API Back-End => mom_api2

### Installing Dependencies

```
python3 -m venv venv
```
```
source venv/bin/activate
```
```
pip3 install -r requirements.txt
```

### Running the FLASK API

Create .env file with:
```
DATABASE_URL=postgresql:///mom_api2
SECRET_KEY=*************
```
******** = Provide your own.

Create the database in the command line:
```
$ psql
# CREATE DATABASE mom_api2;
```

To seed the database, first run the `seed.py` file directly to create the database tables:
```
$ python3 seed.py
```
You only need to do this once, unless you change your model definitions.

Fix the database: (Data was entered explicitly using .csv files, need to set max student_id value)
```
# SELECT setval('students_id_seq', (SELECT MAX(id) from "students"));
```

Use Insomnia to add Mom & School profile:
```
{ "username":"Mom",
"password":"password",
"first_name":"Laura",
"last_name":"Andooli",
"email":"l@andooli.com",
"phone":"3425435"}

{ "username":"school",
"password":"school",
"first_name":"school",
"last_name":"school",
"email":"school@school.com",
"phone":"3425435"}
```

Use Insomnia to add Guardian/Children Relationships for Andooli Family:
```
{ "guardian_username":"Mom",
"child_id":"4" }

{ "guardian_username":"Mom",
"child_id":"6" }

{ "guardian_username":"Mom",
"child_id":"7" }
```

Then run the app itself:

```
$ flask run -p 5001
```

Visit [http://localhost:5001/](http://localhost:5001/) in your browser to see the results.

2. StepZen => test_stepzen

### Running the StepZen Files

Create .env file with:
```

```
******** = Provide your own.

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
