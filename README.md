
# HomeHub Mock Server

## Project Overview

The HomeHub Mock Server provides a backend simulation for the HomeHub real estate management application. This mock server is designed to help with frontend development and testing by providing mock data for property listings, agent details, and search/filter functionalities.

## Features

- **Property Listings:** View detailed information about various properties, including title, location, price, property type, number of bedrooms, bathrooms, square footage, status, and amenities.
- **Property Images:** Each property includes multiple images showcasing its features.
- **Agent Information:** Contact details and profile pictures of agents managing the properties.
- **Search and Filter:** Search and filter properties based on location, price range, and property type.

## Getting Started

### Prerequisites

- **Node.js:** Ensure Node.js is installed on your system. Download it from [nodejs.org](https://nodejs.org/).

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/ImeldaHope/homehub_data.git
   cd homehub_data
   ```

2. **Install Dependencies**

   Install the required dependencies using npm:

   ```bash
   npm install
   ```

### Configuration

By default, the mock server runs on port `3000`. You can change the port by setting the `PORT` environment variable.

### Running the Mock Server

To start the server, run:

```bash
npm start
```

The server will be available at `http://localhost:3000`.


### Hosting on Render.com

To deploy the mock server on Render.com, follow these steps:

1. **Create a New Web Service**: Log in to your Render.com account and create a new web service.
2. **Connect Your Repository**: Link your GitHub repository containing the mock server code.
3. **Configure Build and Start Commands**: Set the build command to `npm install` and the start command to `npm start`.
4. **Set Environment Variables**: Configure any necessary environment variables, including `PORT` if needed.
5. **Deploy**: Deploy your service and get the public URL for your mock server.

## API Endpoints

Once deployed, the JSON server will expose the following endpoints:

- **GET `/api/homehub`**  
  Returns a list of all properties with detailed information.

- **GET `/api/homehub/:id`**  
  Returns a specific property by its ID.

- **GET `/api/wishlist`**  
  Returns a list of properties in the wishlist.

- **POST `/api/wishlist`**  
  Adds a new property to the wishlist.

- **PATCH `/api/wishlist/:id`**  
  Updates the details of a specific property in the wishlist.

- **DELETE `/api/wishlist/:id`**  
  Deletes a specific property from the wishlist.

## Testing

To test the mock server endpoints, use tools like Postman or CURL. For example:

```bash
curl http://localhost:3000/api/homehub
```

