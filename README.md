The goal of this coding exam is to quickly get you off the ground with **Authentication**.

### Refer to the image below:

<div style="text-align: center;">
    <img src="https://assets.ccbp.in/frontend/content/react-js/ebank-output-v2.gif" alt="ebank-output" style="max-width:70%;box-shadow:0 2.8px 2.2px rgba(0, 0, 0, 0.12)">
</div>

### Design Files

<details>
<summary>Login Route</summary>

- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Login](https://assets.ccbp.in/frontend/react-js/ebank-login-route-img.png)
- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Login Failure](https://assets.ccbp.in/frontend/react-js/ebank-login-failure-route-img.png)

</details>

<details>
<summary>Home Route</summary>

- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home](https://assets.ccbp.in/frontend/react-js/ebank-home-route-img.png)

</details>

<details>
<summary>Not Found Route</summary>

- [Medium (Size >= 768px), Large (Size >= 992px) and Extra Large (Size >= 1200px) - Home](https://assets.ccbp.in/frontend/react-js/ebank-not-found-route-img.png)

</details>

### Set Up Instructions

<details>
<summary>Click to view</summary>

- Download dependencies by running `npm install`
- Start up the app using `npm start`
</details>

### Completion Instructions

<details>
<summary>Functionality to be added</summary>
<br/>

The app must have the following functionalities

- **Login Route**

  - When invalid credentials are provided and the **Login** button is clicked, then the error message received from the response should be displayed
  - When valid credentials are provided and the **Login** button is clicked, then the page should be navigated to the Home Route
  - When an unauthenticated user tries to access the Home Route, then the page should be navigated to Login Route
  - When an authenticated user tries to access the Home Route, then the page should be navigated to the Home Route

- **Home Route**

  - When an _authenticated_ user tries to access the Login Route, then the page should be navigated to the Home Route
  - When the **Logout** button is clicked, then the page should be navigated to the Login Route

- **Not Found Route**
  - When a random path is provided in the URL, then the page should be navigated to the Not Found Route

</details>

<details>

<summary>API Requests & Responses</summary>
<br/>

**loginApiUrl**

#### API: `https://apis.ccbp.in/ebank/login`

#### Method: `POST`

#### Request:

```json
{
  "user_id": 142420,
  "pin": 231225
}
```

#### Description:

Returns a response based on the credentials provided

#### Sample Success Response:

```json
{
  "jwt_token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJ1c2VybmFtZSI6IjE0MjQyMCIsInJvbGUiOiJQUklNRV9VU0VSIiwiaWF0IjoxNjM0MDk4NzYyfQ.ZUCC2J2zBjRhLVa1EI_4EnkZ-M-7hoVZoZFAu8GTmEQ"
}
```

#### Sample Failure Response:

```json
{
  "status_code": 401,
  "error_msg": "Invalid user ID"
}
```

</details>

### Important Note

<details>
<summary>Click to view</summary>

<br/>

**The following instructions are required for the tests to pass**

- Home Route should consist of `/` in the URL path
- Login Route should consist of `/ebank/login` in the URL path
- No need to use the `BrowserRouter` in `App.js` as we have already included in `index.js`

- User credentials

  ```text
   User ID: 142420
   PIN: 231225

  ```

</details>

### Resources

<details>
<summary>Image URLs</summary>

- [https://assets.ccbp.in/frontend/react-js/ebank-login-img.png](https://assets.ccbp.in/frontend/react-js/ebank-login-img.png) alt should be **website login**

- [https://assets.ccbp.in/frontend/react-js/ebank-logo-img.png](https://assets.ccbp.in/frontend/react-js/ebank-logo-img.png) alt should be **website logo**

- [https://assets.ccbp.in/frontend/react-js/ebank-digital-card-img.png](https://assets.ccbp.in/frontend/react-js/ebank-digital-card-img.png) alt should be **digital card**

- [https://assets.ccbp.in/frontend/react-js/ebank-not-found-img.png](https://assets.ccbp.in/frontend/react-js/ebank-not-found-img.png) alt should be **not found**

</details>
<br/>
<details>
<summary>Colors</summary>

<br/>

<div style="background-color: #152850; width: 150px; padding: 10px; color: white">Hex: #152850</div>
<div style="background-color: #e0eefe; width: 150px; padding: 10px; color: black">Hex: #e0eefe</div>
<div style="background-color: #183b56; width: 150px; padding: 10px; color: white">Hex: #183b56</div>
<div style="background-color: #5a7184; width: 150px; padding: 10px; color: white">Hex: #5a7184</div>
<div style="background-color: #ffffff; width: 150px; padding: 10px; color: black">Hex: #ffffff</div>
<div style="background-color: #c3cad9; width: 150px; padding: 10px; color: black">Hex: #c3cad9</div>
<div style="background-color: #1565d8; width: 150px; padding: 10px; color: white">Hex: #1565d8</div>
<div style="background-color: #ff0b37; width: 150px; padding: 10px; color: white">Hex: #ff0b37</div>
<div style="background-color: #f8fafc; width: 150px; padding: 10px; color: black">Hex: #f8fafc</div>

</details>
<br/>
<details>

<summary>Font-families</summary>

- Roboto

</details>

> ### _Things to Keep in Mind_
>
> - All components you implement should go in the `src/components` directory
