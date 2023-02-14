
# SportSee project 



## Authors

- [ValentinMam](https://github.com/ValentinMam)


# Installation

Clone the project

```bash
  git clone https://github.com/ValentinMam/ValentinMamichel_12_20122022.git
```
## Environment Variables

To run this project, you will need to add the following environment variables to your .env file

`REACT_APP_ACTIVE_MOCK`

`PORT`

## Application


Go to the project directory

```bash
  cd sportsee-react-app
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```
Run on port 5500
## API


Go to the project directory

```bash
  cd sportsee-api
```

Install dependencies

```bash
  npm install
```

Start the server

```bash
  npm run start
```

Run on port 3000



# Mock to real API

sportsee-react-app/src/utils : 
- mockService.js : mock API
- service.js : real API
- models.js : models of data

You can switch between mock and real API by changing  sportsee-react-app/src/utils/models.js :


```javascript
const selectedService =
  process.env.REACT_APP_ACTIVE_MOCK === 'false' ? mockService : Service


// switch 'false' to 'true' or 'true' to 'false' to switch between mock and real API
```



## API Reference

#### Get all data of user 

```http
  GET http://localhost:3000/user/${userId}
```

| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `string` | **Required**. Id of users to fetch |


#### Get data of user activity

```http
  GET http://localhost:3000/user/${userId}/activity
```


| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `string` | **Required**. Id of users to fetch |



#### Get data of user average sessions

```http
  GET http://localhost:3000/user/${userId}/average-sessions
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `string` | **Required**. Id of users to fetch |


#### Get data of user performance

```http
  GET http://localhost:3000/user/${userId}/performance
```
| Parameter | Type     | Description                |
| :-------- | :------- | :------------------------- |
| `userId` | `string` | **Required**. Id of users to fetch |