# Safary - Interview App

## Overview

Hello!

This is a barebone Remix app we'll use for a few exercises. You'll need to run
it locally and make some changes as described below.
You shouldn't need to know how to work with Remix in order to complete this, but
if that helps you can have a look at the [Remix docs](https://remix.run/docs/en/main/pages/philosophy)

This app mimics the current Safary MVP, so it will give you a taste of our
codebase in the process.

## Development

- Start by forking this repository and cloning it on your machine
- install the modules with:
  ```sh
  npm i
  ```
- start the database with Docker
  ```sh
  npm run docker
  ```
- build the project for the first time with:
  ```sh
  npm run build
  ```
- Then start the dev server with:
  ```sh
  npm run dev
  ```
- Finally, navigate to [http://localhost:3000](http://localhost:3000)

## Exercises

To share your answers you can either:
- fork the repository and publish a _private_ repo with your changes, then
  invite [Tim Alby](https://github.com/timothee-alby) to give them access
- create a public repository __without a direct fork__ and share a link to that
  repo

**Do not fork this into a public repo, do not open a PR as this would make your
answers visible to anyone.**

### 1. Loading State

The data populating the chart is fetched remotely; which can be a slow
operation. for a better UX, can you add a loading state?
Tip: MUI has `LinearProgress` and `CircularProgress` components.

### 2. Doughnut Chart

Create a new chart page "My awesome Doughnut chart" displaying a doughnut chart.
Reuse the same underlying data as for the Pie chart.

### 3. US population over time

Build a new graph "US population" as a line chart, showing the US population per
year, as returned from https://datausa.io/api/data?drilldowns=Nation&measures=Population
(please do fetch the data in real-time).

### 4. Safe redirect

The app comes with auto-redirect: try navigating to [http://localhost:3000/?return_to=/simple-lines](http://localhost:3000/?return_to=/simple-lines).
However, that's quite unsafe! Do you know why?
Please update the `safeRedirect` method to ensure all redirects are safe. A test
harness already exists for that function; make sure to extend it in order to
cover all use-cases.
