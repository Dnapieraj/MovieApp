# 🎬 MovieApp

A modern, responsive movie discovery and search application built with React and Vite. Explore trending movies, search your favorites, and discover new films with beautiful UI powered by Tailwind CSS.

## ✨ Features

- **🔍 Smart Movie Search** - Search for movies with debounced real-time results
- **📈 Trending Movies** - Discover what's trending this week with popularity tracking
- **🎨 Modern UI** - Beautiful, responsive design built with Tailwind CSS
- **⚡ Fast Performance** - Optimized with Vite for lightning-fast development and builds
- **💾 Search History** - Tracks and displays most-searched movies
- **📱 Fully Responsive** - Works seamlessly on desktop, tablet, and mobile devices
- **🔄 Real-time Updates** - Debounced search for smooth user experience

## 🛠️ Tech Stack

- **Frontend Framework**: React 19.2.6
- **Build Tool**: Vite 8.0.12
- **Styling**: Tailwind CSS 4.3.0 with Vite plugin
- **Backend**: Appwrite (BaaS)
- **Movie Data**: The Movie Database (TMDB) API
- **Code Quality**: ESLint with React hooks support
- **Utilities**: react-use for custom hooks

## 📋 Prerequisites

Before you begin, ensure you have the following installed:

- Node.js (v16 or higher)
- npm or pnpm package manager

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/MovieApp.git
cd MovieApp/vite-project
```

### 2. Install Dependencies

```bash
npm install
# or
pnpm install
```

### 3. Environment Configuration

Copy the environment template and add your API credentials:

```bash
# Copy the environment template
cp .env.example .env.local
```

Now open `.env.local` and replace the placeholder values with your actual API credentials:

```env
VITE_TMDB_API_KEY=your_tmdb_api_key_here
VITE_APPWRITE_ENDPOINT=your_appwrite_endpoint
VITE_APPWRITE_PROJECT_ID=your_project_id
VITE_APPWRITE_DATABASE_ID=your_database_id
VITE_APPWRITE_COLLECTION_ID=your_collection_id
```

> **Important**: 
> - The `.env.local` file is added to `.gitignore` and should **never** be committed to the repository
> - Each developer must create their own `.env.local` file with their credentials
> - Never share `.env.local` or paste credentials into `.env.example`

### 4. Run Development Server

```bash
npm run dev
# or
pnpm dev
```

The application will be available at `http://localhost:5173`

## 📦 Available Scripts

```bash
# Start development server with Hot Module Replacement (HMR)
npm run dev

# Build for production
npm run build

# Preview production build locally
npm run preview

# Run ESLint to check code quality
npm run lint
```

## 🎯 Project Structure

```
vite-project/
├── src/
│   ├── components/
│   │   ├── MovieCard.jsx       # Individual movie card component
│   │   ├── Search.jsx          # Search input component
│   │   └── Spinner.jsx         # Loading spinner component
│   ├── assets/                 # Static assets
│   ├── App.jsx                 # Main application component
│   ├── appwrite.js             # Appwrite database functions
│   ├── main.jsx                # Application entry point
│   ├── index.css               # Global styles
│   └── App.css                 # App-specific styles
├── public/                     # Static files (hero.png)
├── index.html                  # HTML template
├── vite.config.js             # Vite configuration
├── eslint.config.js           # ESLint configuration
├── package.json               # Project dependencies
└── .env.local                 # Environment variables (create locally)
```

## 🔌 API Integration

### TMDB API

The application fetches movie data from The Movie Database (TMDB) API:

- **Trending Endpoint**: `/trending/movie/week` - Gets trending movies
- **Search Endpoint**: `/search/movie` - Searches movies by query
- **Discover Endpoint**: `/discover/movie` - Gets popular movies

### Appwrite Integration

Uses Appwrite as a backend service to:

- Track search statistics and frequency
- Store and retrieve trending searches
- Maintain search history data

> **Note**: Requires proper `.env.local` configuration with valid Appwrite credentials

## 🎨 Styling

The project uses **Tailwind CSS** for utility-first CSS styling with custom components:

- **Hero Section**: Gradient text effects and banner images
- **Movie Grid**: Responsive card layouts
- **Search Bar**: Rounded input with focus states
- **Loading States**: Spinner animations

## 🐛 Error Handling

The application includes robust error handling for:

- Failed API requests to TMDB
- Network connectivity issues
- No search results scenarios
- Appwrite database errors

## 🚀 Deployment

### Build for Production

```bash
npm run build
```

This generates an optimized production build in the `dist/` folder.

### Deploy Options

- **Vercel** - Recommended for React/Vite projects
- **Netlify** - Great CI/CD integration
- **GitHub Pages** - Free static hosting
- **Any Static Host** - Supports SPA routing configuration

**Important**: Always set your environment variables in your deployment platform's settings. Never commit `.env.local` or any files containing API keys.

## 📚 Additional Resources

- [React Documentation](https://react.dev)
- [Vite Documentation](https://vitejs.dev)
- [Tailwind CSS Documentation](https://tailwindcss.com)
- [TMDB API Documentation](https://www.themoviedb.org/settings/api)
- [Appwrite Documentation](https://appwrite.io/docs)

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 👨‍💻 Author

Created with ❤️ by [Your Name]

## 📞 Support

If you have any questions or need help, please open an issue on GitHub or contact the development team.

---

**Happy Movie Hunting! 🍿🎬**
