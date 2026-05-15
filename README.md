# MediaSearch

A React-based media discovery app that lets you search for **photos**, **videos**, and **GIFs** across multiple APIs and save your favorites to a personal collection.

## Features

- 🔍 **Search** across Unsplash (photos), Pexels (videos), and Tenor (GIFs)
- 🖼️ **Tab-based browsing** — toggle between Photos, Videos, and GIF results
- 💾 **Save to Collection** — build a personal media library with one click
- ❌ **Remove from Collection** — manage your saved items easily
- 🗑️ **Clear All** — wipe your entire collection in one click
- 💾 **Persistent storage** — your collection is saved to `localStorage`
- 🔔 **Toast notifications** — visual feedback when adding or removing items
- ⚡ **Built with Vite** — fast development and optimized production builds

## Tech Stack

| Technology | Purpose |
|---|---|
| [React 18](https://react.dev/) | UI framework |
| [Redux Toolkit](https://redux-toolkit.js.org/) | State management |
| [React Router DOM](https://reactrouter.com/) | Client-side routing |
| [Tailwind CSS 4](https://tailwindcss.com/) | Utility-first styling |
| [Axios](https://axios-http.com/) | HTTP client |
| [React Toastify](https://fkhadra.github.io/react-toastify/) | Toast notifications |
| [Vite](https://vitejs.dev/) | Build tool & dev server |

## APIs Used

- [Unsplash API](https://unsplash.com/developers) — photos
- [Pexels API](https://www.pexels.com/api/) — videos
- [Tenor API](https://developers.google.com/tenor) — GIFs

## Getting Started

### Prerequisites

- [Node.js](https://nodejs.org/) (v16 or later)
- npm (comes with Node.js)

### Installation

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd project
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the project root with your API keys:
   ```env
   VITE_UNSPLASH_KEY=your_unsplash_access_key
   VITE_PEXELS_KEY=your_pexels_api_key
   VITE_TENOR_KEY=your_tenor_api_key
   ```

   > **Getting API Keys:**
   > - **Unsplash:** Register at [unsplash.com/developers](https://unsplash.com/developers) and create an app to get your Access Key.
   > - **Pexels:** Sign up at [pexels.com/api](https://www.pexels.com/api/) and get your API key.
   > - **Tenor:** Go to [developers.google.com/tenor](https://developers.google.com/tenor) and create a project to get your API key.

### Running the App

Start the development server:

```bash
npm run dev
```

Open [http://localhost:5173](http://localhost:5173) in your browser.

### Building for Production

```bash
npm run build
```

The output will be in the `dist/` directory. You can preview the production build with:

```bash
npm run preview
```

## Project Structure

```
project/
├── public/               # Static assets
├── src/
│   ├── api/
│   │   └── mediaApi.js       # API calls to Unsplash, Pexels, Tenor
│   ├── components/
│   │   ├── CollectionCard.jsx  # Card for saved collection items
│   │   ├── Navbar.jsx          # Top navigation bar
│   │   ├── ResultCard.jsx      # Card for search results
│   │   ├── ResultGrid.jsx      # Grid layout of result cards
│   │   ├── SearchBar.jsx       # Search input form
│   │   └── Tabs.jsx            # Photo / Video / GIF tab switcher
│   ├── pages/
│   │   ├── HomePage.jsx        # Main search page
│   │   └── CollectionPage.jsx  # Saved collection page
│   ├── redux/
│   │   ├── store.js            # Redux store configuration
│   │   └── features/
│   │       ├── collectionSlice.js  # Collection state & reducers
│   │       └── searchSlice.js      # Search state & reducers
│   ├── App.jsx              # Root component with routing
│   ├── index.css            # Global styles (Tailwind)
│   └── main.jsx             # Entry point
├── .env                    # API keys (not committed)
├── .eslintrc.cjs           # ESLint configuration
├── index.html              # HTML template
├── package.json            # Dependencies & scripts
├── vite.config.js          # Vite configuration
└── README.md               # This file
```

## Usage

1. **Search** — Type a keyword into the search bar and click "Search".
2. **Filter** — Use the tabs (Photos / Videos / GIF) to switch between media types.
3. **Explore** — Results are displayed as cards. Hover and click to view the full media on the source site.
4. **Save** — Click the **Save** button on any result card to add it to your collection.
5. **View Collection** — Click **Collection** in the navbar to see all saved items.
6. **Remove** — Click **Remove** on a collection item to delete it.
7. **Clear All** — Click **Clear Collection** to remove every saved item at once.