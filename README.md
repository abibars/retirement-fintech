# Full Stack Personal Finance Web App

This is a personal finance application that allows users to link their bank account via the Plaid API. Current functionality includes basic authentication via JSON Web Token, and the addition, deletion, and refreshing of a bank account. The application will display the user's account balances and transactions. Note that this project is a work in progress - more features are planned to be implemented in the future.

## PROBLEM STATEMENT
So, presently, do people plan their retirements considering all the factors ?

To plan your retirement corpus, large number of factors must be considered, for eg: your current salary, expenses, current savings, your assets, liabilities, investments, etc. Apart from this, global factors such as inflation rates, location based expenses (cheap vs expensive city), stock market conditions, etc, should also be considered to evaluate what should be your retirement corpus.

But currently, there is no solution to provide complete picture of your retirement corpus / savings, that would be sufficient for you to live a comfortable retired life.

## PROPOSED SOLUTION
Thus, my solution is to use technology (web, data analytics, etc) to create an application that takes into consideration user’s current financial status such as assets, liabilities, investments, etc, and global factors (inflation, location specific lifestyle, stock markets, etc) to model user’s future retirements needs and what, when, and how current savings can lead to future retirement corpus.

Data points are collected through API’s and modelled to create an output and displayed in chart for easy understanding.

## TECH STACK
MERN stack:
- MongoDB (Database)
- Express
- ReactJS (FrontEnd)
- NodeJS (BackEnd)

D3 JS (chart visualization)

Material UI

API’s (Plaid, Numbeo)

PPT is uploaded in the repo.

## Setup

1. `git clone https://github.com/jagodin/personal-finance-app`
2. `cd personal-finance-app`
3. `npm install`
4. `npm run dev` to run the development environment.

Obtain your Plaid API keys from [here](https://dashboard.plaid.com/signup) and set up a [MongoDB database](https://www.mongodb.com/download-center)

Configure `./config/default.json`

```
{
    "mongoURI": "YOUR_MONGO_URI",
    "jwtSecret": "YOUR_SECRET_TOKEN"
}
```

## Technologies

1. Node.js
2. React
3. Redux
4. MongoDB
5. Express.js
6. Material UI

## Packages

1. Axios
2. Express Validator
3. JSON Web Token
4. Redux Thunk
5. Bcrypt.js
6. Mongoose

## Screenshots

Login/Registration Page
![Login/Registration Page](https://user-images.githubusercontent.com/17988743/72691879-98e91780-3af6-11ea-8125-c8e25a172663.JPG)


Dashboard and Profile Menu
![Dashboard and Profile Menu](https://user-images.githubusercontent.com/17988743/72690028-09d40380-3ae6-11ea-8478-9d65f0d08dcb.JPG)


Linked Accounts and Balances
![Linked Accounts and Balances](https://user-images.githubusercontent.com/17988743/72690034-26703b80-3ae6-11ea-8d82-cd152aeba8f7.JPG)


Transactions
![Transactions](https://user-images.githubusercontent.com/17988743/72690047-3e47bf80-3ae6-11ea-920e-23ef0e32081e.JPG)


Plaid Link
![Plaid Link](https://user-images.githubusercontent.com/17988743/72690044-2e2fe000-3ae6-11ea-8592-563974a0230a.JPG)


Responsive Dashboard
![Responsive Dashboard](https://user-images.githubusercontent.com/17988743/72690045-3556ee00-3ae6-11ea-861d-b6ca09cffb90.JPG)


## Future Enhancements

1. Implement budgets and categorize transactions into appropriate budget.
2. Add user settings (i.e. UI preferances).
3. Give users the ability to report application issues via the Support page.
4. Implement FAQ.
5. Responsive UI enhancements.
6. Implement cache to prevent user's from overloading the backend and Plaid API.
7. Implement Google Firebase Authentication.

## Disclaimer

Note that the application exposes the user's `access_tokens` and `item_ids` to the client. For production releases, these must be securely persisted to your database and never exposed to the client.

From the Plaid API documentation:

> access_tokens and item_ids are the core identifiers that map your end-users to their financial institutions. You should persist these securely and associate them with users of your application. Make sure, however, that these identifiers are never exposed client-side. Keep in mind that one user can create multiple Items if they have accounts with multiple financial institutions.
