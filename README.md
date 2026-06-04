# API Data Rendering

A modern React application built with Vite for fetching and displaying data from public APIs.

## Project Overview

This project demonstrates a complete workflow for:
- Fetching data from REST APIs
- Managing loading and error states
- Rendering dynamic lists with React components
- Building reusable, maintainable components

## Project Structure

```
api-data-rendering/
├── src/
│   ├── components/
│   │   ├── DataList.jsx       # Reusable component for rendering data list
│   │   ├── DataList.css       # Styles for DataList component
│   │   ├── Loader.jsx         # Loading spinner component
│   │   └── Loader.css         # Styles for Loader component
│   ├── App.jsx                # Main application component
│   ├── App.css                # Styles for App component
│   ├── main.jsx               # React entry point
│   └── index.css              # Global styles
├── index.html                 # HTML entry point
├── package.json               # Project dependencies
├── vite.config.js            # Vite configuration
└── README.md                  # This file
```

## Features

✅ **API Integration** - Fetches user data from JSONPlaceholder API
✅ **Loading State** - Displays spinner while data is loading
✅ **Error Handling** - Shows error messages when API calls fail
✅ **Responsive Design** - Works seamlessly on all screen sizes
✅ **Component Reusability** - Clean, maintainable component structure
✅ **Conditional Rendering** - Displays appropriate UI based on app state

## Installation

1. Install dependencies:
```bash
npm install
```

## Running the Project

### Development Server
```bash
npm run dev
```
The application will open at `http://localhost:3000`

### Production Build
```bash
npm run build
```

### Preview Production Build
```bash
npm run preview
```

## API Integration

The application uses the [JSONPlaceholder API](https://jsonplaceholder.typicode.com/) to fetch user data.

**Endpoint:** `https://jsonplaceholder.typicode.com/users`

Returns a list of users with the following properties:
- `id` - Unique identifier
- `name` - User's full name
- `email` - User's email address
- `phone` - Phone number
- `website` - Personal website
- `company` - Company information

## How It Works

1. **Component Initialization** - App.jsx loads and sets up state management
2. **Data Fetching** - useEffect hook triggers API call on component mount
3. **Loading State** - Loader component displays while fetch is in progress
4. **Data Processing** - Fetched data is stored in state
5. **Rendering** - DataList component maps over data and renders each item
6. **Error Handling** - Any errors are caught and displayed to the user

## Component Details

### App.jsx
- Manages global state (data, loading, error)
- Handles API fetching logic
- Implements conditional rendering for different states
- Props: None

### DataList.jsx
- Receives data array as prop
- Renders each item with unique key
- Props: `data` (array of items)

### Loader.jsx
- Displays animated spinner
- Shows loading message
- Props: None

## State Management

The application uses React's `useState` hook to manage:
- `data` - Stores fetched API data
- `loading` - Boolean flag for loading state
- `error` - Stores error message if API call fails

## Error Handling

- Try-catch block for API calls
- HTTP status validation
- User-friendly error messages
- Retry button to reload data

## Styling

- CSS Grid for responsive layouts
- Flexbox for component alignment
- Media queries for mobile responsiveness
- CSS animations for loader spinner
- Linear gradient backgrounds

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Future Enhancements

- [ ] Add pagination for large datasets
- [ ] Implement search/filter functionality
- [ ] Add data sorting options
- [ ] Cache API responses
- [ ] Add more API endpoints
- [ ] Implement infinite scroll
- [ ] Add local storage persistence

## Troubleshooting

**Port 3000 already in use?**
Edit `vite.config.js` and change the port number in the server configuration.

**CORS errors?**
The JSONPlaceholder API supports CORS. If using a different API, ensure it has CORS enabled.

**Blank page loading?**
Check browser console for errors. Ensure all dependencies are installed with `npm install`.

## License

MIT

## Author

Created as a React/Vite learning project for API data rendering.
