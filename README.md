
# 🎬 Movie Landing Page

Responsive, smooth, and performant movie listing app using **Vite + React + TypeScript + SCSS**.

---

#  Requirements Met

 **1. Vertical Scroll Only, No Horizontal Scroll + Virtualized Optimized Grid**

- The movie grid **only scrolls vertically**, no horizontal overflow.
- Layout is **grid-based** with proper `overflow-y: scroll` and restricted `overflow-x: hidden`.
- Virtualization is optimized by **lazy rendering** using **IntersectionObserver** – only images in view are loaded.

  **2. Lazy Loading of Content**

- **First page** is loaded on app start.
- **Next pages** (`page2.json`, `page3.json`, etc.) are fetched **seamlessly** as the user scrolls **near the bottom**.
- **Skeleton loaders** are shown while new data is being appended — **no blocking spinner or scroll freeze**.

  **3. Client-Side Search Without API**

- Search is implemented **purely client-side** using **Context API + useReducer**.
- Already loaded movie data is **filtered instantly** based on the search query.
- **No page reloads**, **no API calls**, and **results are shown live** in the main view itself.

  **4. Focus / Long Press Scale Animation**

- When a card is **hovered**, **focused** (keyboard), or **long pressed** (touch devices), a **smooth scale effect** is applied.
- CSS transitions are handled efficiently for a buttery-smooth experience.

  **5. Arrow Key Navigation**

- **Custom `useArrowNavigation` hook** is implemented.
- Users can **navigate between movie cards** using **Arrow keys (⬅️ ➡️ ⬆️ ⬇️)**, without any third-party library.

  **6. Proper Paginated API Handling**

- Only **page1.json** is fetched initially.
- As the user scrolls and approaches the end of the grid, **next page is requested dynamically**.
- **No preloading of all pages at once**.
- Fetches are **smooth**, **non-blocking**, and **do not interrupt scrolling**.

  **7. Proper Data Flow Management**

- **Context API** + **useReducer** is used to manage:
  - Search state (query, suggestions, search mode)
  - Grid state (infinite scroll trigger)
- Local caching of pages in **localStorage** with **TTL** expiration.
- Centralized hooks for data fetching (`useMovies`), scrolling (`useInfiniteScroll`), and arrow navigation.

  **8. Performance Optimizations**

- **Lazy loading** of images (only load images as they come into view).
- **Memoization** (`React.memo`) of cards (`MovieCard` component).
- **Split responsibilities** across hooks and components.
- **No unnecessary re-renders** thanks to careful dependency management in hooks.
- **Preconnects external resources** (fonts, assets) for faster first paint (FCP/LCP).

---

#  Tech Stack

- [Vite](https://vitejs.dev/) + [React](https://react.dev/) + [TypeScript](https://www.typescriptlang.org/)
- SCSS Modules
- Context API + useReducer
- IntersectionObserver API
- LocalStorage cache with TTL
- Fully optimized for performance, responsiveness, and smooth UX.
- ESLint + Prettier for code formatting

---

---

##  Running Locally

```bash
npm run dev
```
- Starts the app at `http://localhost:5173`
- Supports hot-reloading

---

##  Building for Production

```bash
npm run build
```
- Creates optimized production build inside `/dist`.

To preview the production build:

```bash
npm run preview
```

---

##  Running Tests

```bash
npm run test
```
- Runs unit tests using **Jest** and **React Testing Library**.

---

##  Generating Documentation

```bash
npm run docs
```
- Generates project documentation using **TypeDoc** into `/docs`.


#  Demo

[Live Demo Link](https://nvaneethm.github.io/mobile-landing-page/) 
