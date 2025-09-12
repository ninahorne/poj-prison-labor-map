# Prison Labor Map - Promise of Justice Project

An interactive web application mapping prison labor locations, historical sites, and janitorial services using forced prison labor across Louisiana parishes. This project is part of the Equal Justice Initiative's Promise of Justice Project.

## Overview

This application visualizes three types of locations:

- **Jails and Prisons Using Forced Labor** - Correctional facilities with forced labor programs
- **Places Using Janitorial Services** - Buildings that utilize Prison Enterprises janitorial services performed by incarcerated individuals
- **Historical Locations** - Sites of historical significance related to criminal justice

## Features

- Interactive Google Maps visualization centered on Louisiana
- Toggle-able map layers for different data types
- Detailed information windows with demographics, facility details, and historical context
- Parish boundary overlays that highlight when markers are clicked
- Responsive design with custom styling
- Real-time data integration via Airtable API

## Tech Stack

- **Frontend**: Vanilla JavaScript, HTML5, CSS3
- **Maps**: Google Maps JavaScript API
- **Backend**: Node.js with Express
- **Data Source**: Airtable API
- **Deployment**: Vercel
- **Styling**: Bootstrap 5, custom CSS

## Installation

1. Clone the repository:

```bash
git clone <repository-url>
cd poj-prison-labor-map
```

2. Install dependencies:

```bash
npm install
# or
yarn install
```

3. Set up environment variables:
   Create a `.env` file in the root directory:

```
AIRTABLE_API_KEY=your_airtable_api_key
```

4. Run locally:

```bash
npm run serve
# or for production
npm start
```

The application will be available at `http://localhost:3000`

## Environment Variables

- `AIRTABLE_API_KEY` - API key for accessing Airtable data

## API Endpoints

- `GET /api/historic-spots` - Retrieves historical location data
- `GET /api/jails` - Retrieves jail and prison facility data
- `GET /api/janitorial-services` - Retrieves buildings using prison janitorial services
- `GET /api/file` - Utility endpoint for processing parish GeoJSON data

## Data Sources

The application pulls data from three Airtable bases:

- **Historic Spots Map** - Historical locations and their significance
- **Jail Map** - Prison facilities with detailed demographics and labor information
- **Janitorial Services Map** - Buildings utilizing incarcerated labor for janitorial services

## Deployment

The project is configured for deployment on Vercel with the included `vercel.json` configuration:

```bash
vercel deploy
```

## File Structure

```
├── api/
│   ├── app.js          # Express application and API routes
│   └── index.js        # Server entry point
├── public/
│   ├── assets/         # Map marker icons and legends
│   ├── js/
│   │   ├── init.js     # Main application logic and map initialization
│   │   └── mapStyles.js # Google Maps custom styling
│   ├── json/           # Pre-processed parish boundary data
│   ├── index.html      # Main application page
│   └── main.css        # Application styles
├── parishData2.json    # Louisiana parish boundary GeoJSON data
└── vercel.json         # Vercel deployment configuration
```

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test locally
5. Submit a pull request

## License

MIT License - see LICENSE file for details

## Author

Nina Horne

## Acknowledgments

- Equal Justice Initiative
- Promise of Justice Project
- Data provided through Airtable integration
