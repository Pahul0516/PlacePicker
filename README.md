# PlacePicker

A small learning project focused on React, built to practice fetching data, managing side effects, and keeping the interface in sync with a backend.

## About the app

PlacePicker lets you browse destinations and build a collection of places you would like to visit. It uses your browser's location, with your permission, to sort available places by distance. You can add places to your collection or remove them through a confirmation dialog with a three-second countdown that automatically confirms removal unless cancelled. The app loads and saves the collection through a backend API and displays loading states and error messages.

## What I learned

The frontend is built with React, JavaScript (JSX), CSS, and Vite. My learning in this project focused on the React part: connecting components to data, managing asynchronous updates, and extracting reusable logic.

Through this project, I practiced:

- Splitting the interface into reusable components and passing data and event handlers through props.
- Managing selected places, modal visibility, and errors with `useState`, using functional updates and immutable array operations.
- Using `useEffect` to fetch data and synchronize a dialog with React state, while choosing dependencies that control when effects rerun.
- Creating a custom `useFetch` hook to share data-fetching logic, loading state, and error handling between components.
- Connecting React components to HTTP requests to load available and selected places and save collection changes.
- Applying optimistic updates: updating the interface immediately, then restoring the previous state and showing an error if a save fails.
- Using `useRef` to access the native dialog element and remember the place selected for removal without triggering another render.
- Using `useCallback` to stabilize the removal handler used by the confirmation timer's effect.
- Rendering modals with `createPortal` and using component composition through the `children` prop.
- Managing a countdown and progress bar with effects, and cleaning up timeouts and intervals when components unmount.
- Rendering lists with stable keys and showing loading messages, empty states, and errors conditionally.

## Hosting

Try the app here: [PlacePicker](https://place-picker-frontend.onrender.com/).

The app is hosted on Render.
