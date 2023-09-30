# Weather API Documentation

This is a simple Weather API developed using the OpenWeather.org API and the Go programming language. This API allows you to fetch weather information for a specific location by making HTTP requests.

## Getting Started

To use this Weather API, you will need an API key from OpenWeather.org. You can obtain an API key by signing up on their [website](https://openweathermap.org/).

### Prerequisites

- Go programming language installed on your system.
- An OpenWeather.org API key.

### Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/yourusername/weather-api-golang.git
   ```

2. Change to the project directory:

   ```bash
   cd weather-api-golang
   ```

3. Create a `.env` file in the project directory and add your OpenWeather.org API key:

   ```bash
   OPENWEATHER_API_KEY=your_api_key_here
   ```

4. Build and run the application:

   ```bash
   go build
   ./weather-api-golang
   ```

The API server should now be running locally on port 8080.

## Usage

### Get Weather Information

To get weather information for a specific location, make a GET request to the following endpoint:

```
http://localhost:8080/weather?location={location}
```

Replace `{location}` with the name of the city or location for which you want weather information.

Example Request:

```
GET http://localhost:8080/weather?location=New+York
```

Example Response:

```json
{
  "location": "New York",
  "temperature": 72.5,
  "humidity": 65,
  "description": "Partly cloudy",
  "icon": "http://example.com/weather-icon.png"
}
```

## Error Handling

- If the API is unable to fetch weather data from OpenWeather.org, it will return a `500 Internal Server Error` response.
- If the location is not found or the API key is invalid, it will return a `404 Not Found` response.

## Deployment

To deploy this Weather API to a production environment, you can follow these steps:

1. Deploy the Go application to a web server or cloud platform of your choice.
2. Set up environment variables for the OpenWeather.org API key in your production environment.
3. Update the API endpoint in the documentation to point to your production server.

## Contributing

If you'd like to contribute to this project, please fork the repository and create a pull request with your changes.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Thanks to [OpenWeather.org](https://openweathermap.org/) for providing the weather data.
- This project was created as a learning exercise in Go programming.

Please feel free to reach out with any questions or feedback!
