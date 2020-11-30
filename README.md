# Large System Development, Fall 2020

## **Team B**

## Project CI status

![Frontend CI](https://github.com/TEAM-B-SOFT2020/LSDFrontEnd/workflows/FRONTEND%20CI/badge.svg) ![Backend CI](https://github.com/TEAM-B-SOFT2020/LSDBackEnd/workflows/Backend%20CI/badge.svg)

[Case 2](https://datsoftlyngby.github.io/soft2020fall/resources/aa00a079-case-2.pdf)

## Assignments

1. [Logical Data Model](assignments/logical-data-model.md)
2. [Use Case Model](assignments/use-case-model.md)
3. [System Operations Contract](assignments/system-operations-contract.md)

## Contract

[Contract repository](https://github.com/TEAM-B-SOFT2020/LSDContract)

## Backend Application

[Backend repository](https://github.com/TEAM-B-SOFT2020/LSDBackEnd)

### Setup

#### Installation

```bash
npm install
```

#### MongoDB

1. Log in to your mongodb account on [atlas](https://account.mongodb.com/account/login)
2. Create a database named something like **lsdbackend** or whatever you prefer.
3. Create a `.env` file in the root of the project and insert your connection string like this:

```bash
CONNECTION_STRING=your production connection string with credentials
TEST_CONNECTION_STRING=your development connection string with credentials
# Remember not to use space separation
# - and that the connection strings cannot be identical.
```

4. Populate the production database by running:

```bash
npm run populate
```

### Test

```bash
npm run test
```

### Execute the application

The application uses Remote Procedure Call (RPC) to connect with the frontend application.  
It listens on `localhost:3000`  
When the application is running the monitor is reachable on `localhost:3000/status`
Logs is located at `logs/error.log` and `logs/info.log` in the root folder.

```bash
npm run start
```

### Service Level Agreement and Brancing Strategy

The Service Level Agreement can be found [here](https://github.com/TEAM-B-SOFT2020/LSDBackEnd/wiki/Service-Level-Agreement)  
A figure of our brancing strategy can be found [here](https://github.com/TEAM-B-SOFT2020/LSDBackEnd/wiki)

## Frontend Application

[FrontEnd repository](https://github.com/TEAM-B-SOFT2020/LSDFrontEnd)

### Setup

1. Download the repository.
2. In terminal 

```bash
yarn install
```

3. In terminal

```bash
yarn add TEAM-B-SOFT2020/LSDContract
```

### Tests

```bash
yarn test
```

### Execute the application

Run application

If you have docker installed, you can run everything using the command

```bash
yarn monitor
```
The prometheus.yml file is configured to install a docker-image of the application and run grafana service.



```bash
yarn dev
```

Links

```bash
http://localhost:4000 - for application 
```

```bash
http://localhost:4000/api - for API
```

### Logging and Monotoring.
When the application is running. We log both errors and information about data retrival and input.
In the logger.ts file we specify two text files to store logs. The text files are saved in './logs/errors.log' and './logs/info.logs'
The loggers are defined by levels 'level: 'error'' for erros and 'level: 'info'' for general info.




```bash 
http://localhost:3000 - for montoring 
```

....
