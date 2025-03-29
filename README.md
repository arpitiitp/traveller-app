[![Project Logo](https://img.icons8.com/color/96/000000/airplane-take-off.png)](https://icons8.com/icon/68683/airplane-take-off)


## Overview

This project is a full-stack application that integrates a robust backend API with a modern React-based frontend. The backend provides secure authentication, user management, maps integration, and ride services, while the frontend delivers a dynamic UI using React, Google Maps API, and Tailwind CSS. Both parts of the application are designed for high performance and scalability.

## APP Video Link  
[Watch the video](https://drive.google.com/file/d/1NsvahJmhY2yZXGYFPuyNmN-xG_X4lZ6O/view?usp=sharing)

## Tech Stack

### Frontend
- **React**  
  ![React Icon](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)  
- **Google Maps API**  
  ![Google Maps Icon](https://img.shields.io/badge/Google%20Maps-4285F4?style=for-the-badge&logo=google-maps&logoColor=white)  
- **Tailwind CSS**  
  ![Tailwind CSS Icon](https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwind-css&logoColor=white)  
- **Vite** (for fast development and HMR)  
  ![Vite Icon](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)

### Backend
- **Node.js & Express**  
  ![Node.js Icon](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)  
  ![Express Icon](https://img.shields.io/badge/Express-000000?style=for-the-badge&logo=express&logoColor=white)
- **MongoDB**  
  ![MongoDB Icon](https://img.shields.io/badge/MongoDB-4EA94B?style=for-the-badge&logo=mongodb&logoColor=white)
- **JWT Web Tokens**  
  ![JWT Icon](https://img.shields.io/badge/JWT-000000?style=for-the-badge&logo=jsonwebtokens&logoColor=white)
- **bcrypt**  
  ![bcrypt Icon](https://img.shields.io/badge/bcrypt-4C4C4C?style=for-the-badge)
- **CORS**  
  ![CORS Icon](https://img.shields.io/badge/CORS-000000?style=for-the-badge)
- **Axios**  
  ![Axios Icon](https://img.shields.io/badge/Axios-5A29E4?style=for-the-badge&logo=axios&logoColor=white)

---

## Backend API Documentation

### User Endpoints
- **Register** (`POST /users/register`)  
  Registers a new user. The JSON payload must include:
  - `fullname`: Object with required `firstname` and optional `lastname`
  - `email`: Valid email address
  - `password`: Minimum 6 characters  
  Returns the user details along with a JWT token.

- **Login** (`POST /users/login`)  
  Authenticates a user with their email and password. Returns user data and a JWT token.

- **Profile** (`GET /users/profile`)  
  Retrieves the authenticated user’s profile. Requires a valid JWT token in the Authorization header.

- **Logout** (`GET /users/logout`)  
  Logs out the user by invalidating the JWT provided via headers or cookies.

### Captain Endpoints
- **Register** (`POST /captains/register`)  
  Registers a new captain. The JSON payload includes:
  - `fullname`: Object with required `firstname` and optional `lastname`
  - `email` and `password`
  - `vehicle`: Object with `color`, `plate`, `capacity`, and `vehicleType` (must be 'car', 'motorcycle', or 'auto')  
  Returns captain details and a JWT token.

- **Login** (`POST /captains/login`)  
  Authenticates a captain and returns their profile along with a JWT token.

- **Profile** (`GET /captains/profile`)  
  Retrieves the authenticated captain’s profile including vehicle details. Requires JWT authentication.

- **Logout** (`GET /captains/logout`)  
  Logs out the captain by invalidating the current JWT.

### Maps Endpoints
- **Get Coordinates** (`GET /maps/get-coordinates`)  
  Retrieves latitude and longitude for a given address.
  
- **Get Distance & Time** (`GET /maps/get-distance-time`)  
  Provides the distance and estimated travel time between an origin and destination.
  
- **Get Suggestions** (`GET /maps/get-suggestions`)  
  Returns autocomplete suggestions based on an input string.

### Rides Endpoints
- **Create Ride** (`POST /rides/create`)  
  Creates a new ride with the following required JSON fields:
  - `pickup`
  - `destination`
  - `vehicleType` (allowed values: 'auto', 'car', or 'moto')  
  Returns ride details such as fare, status, OTP, and more.

- **Get Fare** (`GET /rides/get-fare`)  
  Provides a fare estimate for a ride between specified pickup and destination addresses for various vehicle types. Requires JWT authentication.

---

## Frontend Setup

This frontend is built using React and Vite, providing a fast development environment with hot module replacement (HMR) and ESLint for maintaining code quality. It also integrates the Google Maps API for location-based services and utilizes Tailwind CSS for responsive and modern UI styling.

- **React + Vite**  
  Utilize [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react) or [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) for fast refresh and efficient bundling.

---

## Additional Resources

- **Backend Repository:** [Link to Backend Repo](#)
- **Frontend Repository:** [Link to Frontend Repo](#)
- **API Documentation:** Detailed API docs for users, captains, maps, and rides are available above.

---

*Customize the logos and resource links as needed to match your actual project assets and repository locations.*
