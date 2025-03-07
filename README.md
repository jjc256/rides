# Theme Park Ride Order Optimizer

This project is a web application designed to optimize the order of rides at a theme park given user ride preferences and wait time data.

## Features

- **Pre-Park Planning Mode**: Plan your day in advance using average wait times adjusted according to time of day. In order to use pre-park planning mode for a park other than Magic Kingdom, upload a `park_averages.txt`.
- **In-Park Planning Mode**: Get real-time ride recommendations based on current wait times.
- **Customizable Layout**: Configure the layout of lands and rides visually.
- **User Ratings**: Rate rides to personalize your experience.

## Setup

### Prerequisites

- A web server to host the application (e.g., Apache, Nginx, or a simple HTTP server).
- A Cloudflare Worker or similar service to bypass CORS restrictions for the API.

### Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/yourusername/rides.git
    cd rides
    ```

2. Place the `magic_kingdom_averages.txt` or other theme park file in the root directory of the project.

3. Serve the `index.html` file using your preferred web server.

### Configuration

- **API Endpoint**: The application fetches live wait times from `https://rides.jjchen256.workers.dev/`, which uses a Cloudfare worker to fetch from `https://queue-times.com/parks/6/queue_times.json`. You can change this to another API endpoint if needed.
- **Average Wait Times**: For pre-park planning, provide average wait times in a `.txt` file. The format should be:
    ```
    Ride Name, Average Wait Time
    ```

## Usage

1. Open the application in your web browser.
2. Select the mode (Pre-Park Planning or In-Park Planning).
3. Configure the layout by selecting the center land and peripheral lands.
4. Rate each ride from 1 to 10.
5. Set the start and end times for your visit.
6. Click "Plan My Day" to get your recommended ride order.

## Acknowledgements

- Live wait time data and ride/land names are powered by [Queue-Times.com](https://queue-times.com/en-US).
