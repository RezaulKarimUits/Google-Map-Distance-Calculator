# Google Map Distance Calculator

## Introduction

Google Map Distance Calculator is an ASP.NET Core MVC web application for calculating travel distance and time from a selected map location to a list of origins. It uses Google Maps and the Google Distance Matrix service to compare several travel options, including driving, walking, bicycling, and transit modes such as bus, rail, subway, train, and tram.

The app is useful when you need to evaluate many locations against one destination, review distance and duration results in a grid, summarize travel statistics, and export the results to Excel for further analysis.

## Features

- Select a destination directly on the Google map.
- Enter multiple origin addresses in a text area.
- Calculate distance and travel time across multiple travel modes.
- View detailed origin-to-destination results in sortable grids.
- Review summary statistics such as minimum, maximum, and median distance/time.
- Export distance results and statistics to Excel.

## Getting Started

### Prerequisites

Install the following before running the project:

- [.NET SDK 10.0](https://dotnet.microsoft.com/download) or the SDK version required by `MapApp/MapApp.csproj`
- A Google Maps API key with the Maps JavaScript API and Distance Matrix API enabled
- Visual Studio 2022 or later, Visual Studio Code, or another editor that supports ASP.NET Core

### Installation

Clone the repository:

```bash
git clone <your-repository-url>
cd Google-Map-Distance-Calculator
```

Restore the .NET dependencies:

```bash
dotnet restore
```

### Configure Google Maps

Open `MapApp/Views/Home/Index.cshtml` and replace the Google Maps script key with your own API key:

```html
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_GOOGLE_MAPS_API_KEY"></script>
```

For production use, restrict the API key in Google Cloud Console by HTTP referrer and enable only the APIs required by this app.

### Run the Application

From the repository root, run:

```bash
dotnet run --project MapApp
```

Then open the local URL shown in the terminal, usually:

```text
https://localhost:5001
```

or:

```text
http://localhost:5000
```

You can also open `MapApp.sln` in Visual Studio and start the `MapApp` project.

## How to Use

1. Choose a departure time.
2. Enter one origin address per line in the Origins text area.
3. Click a destination point on the map.
4. Click Calculate.
5. Review the detailed distance table and summary statistics.
6. Use the Excel export buttons to download the results.

## Build

Build the project with:

```bash
dotnet build
```

## Project Structure

```text
Google-Map-Distance-Calculator/
|-- MapApp.sln
|-- README.md
`-- MapApp/
    |-- Controllers/
    |-- Models/
    |-- Views/
    |-- wwwroot/
    |-- Program.cs
    |-- Startup.cs
    `-- MapApp.csproj
```

## Notes

- Distance and time results come from Google Maps services, so API quotas, billing, and service availability depend on your Google Cloud configuration.
- The app uses client-side libraries including Vue, jQuery, Bootstrap, Syncfusion EJ2, Moment.js, and supporting plugins.
- Keep API keys out of public commits when possible, and rotate any key that has already been exposed publicly.

## Contributing

Contributions are welcome. To contribute:

1. Fork the repository.
2. Create a feature branch.
3. Make your changes.
4. Test the app locally.
5. Submit a pull request with a short description of your changes.
