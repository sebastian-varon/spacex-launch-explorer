# SpaceX Launch Explorer

A single-page Angular app for browsing SpaceX launches. It pulls live data from the public SpaceX REST API, lets you filter missions by launch year and opens a detail page for each mission.

**Live demo:** https://101394889-lab-test2-comp3133.vercel.app

## Features

- **Mission list:** every past launch as a responsive card with flight number, mission name, year, mission patch, rocket and links to Wikipedia, video and articles.
- **Filter by year:** a sidebar filter narrows the list to one launch year; "All" resets it.
- **Mission details:** `/mission/:id` shows the full record (image, launch success, rocket, launch site) with back navigation.

<img width="1398" alt="Screenshot 2025-04-02 at 15 07 30" src="https://github.com/user-attachments/assets/619c6871-3575-4189-a8ba-d77caae707f7" />

## Tech stack

- Angular 17 with standalone components and the Angular Router
- Angular Material (Material 3 theming)
- RxJS and `HttpClient` in a dedicated `SpacexService`
- Typed `Mission` model in TypeScript
- SpaceX API v3 (`https://api.spacexdata.com/v3/launches`)
- Deployed on Vercel

## Project structure

```
src/app/
  components/
    missionlist/      list view with cards
    missionfilter/    launch-year filter
    missiondetails/   detail view for /mission/:id
  services/spacex.service.ts   API calls
  models/mission.model.ts      Mission type
  app.routes.ts                routes
```

## Screenshots

<img width="1398" alt="Screenshot 2025-04-02 at 15 07 56" src="https://github.com/user-attachments/assets/8c8548c1-78c4-4b41-800f-d3ae6df6d388" />
<img width="1398" alt="Screenshot 2025-04-02 at 15 08 02" src="https://github.com/user-attachments/assets/9a207ce1-dd23-478c-bcd0-3a8bc771b3a2" />

## Run locally

```bash
git clone https://github.com/sebastian-varon/spacex-launch-explorer.git
cd spacex-launch-explorer
npm install
npx ng serve
```

Then open http://localhost:4200.
