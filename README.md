---
layout: home
permalink: index.html

# Please update this with your repository name and title
repository-name: cepdnaclk/e21-co227-PeraVerse-Event-Details-Page
title: Event Details Page of PeraVerse - Dynamic Schedule Board
---

[comment]: # "This is the standard layout for the project, but you can clean this and use your own template"

# Event Details Page of PeraVerse - Dynamic Schedule Board

---

## Team
- E/21/050, H.B.C.T. Bandara, [e21050@eng.pdn.ac.lk](mailto:e21050@eng.pdn.ac.lk)
- E/21/226, N.S. Kothalawala, [e21226@eng.pdn.ac.lk](mailto:e21226@eng.pdn.ac.lk)
- E/21/019, A.M.H.S. Adikari, [e21019@eng.pdn.ac.lk](mailto:e21019@eng.pdn.ac.lk)
- E/21/052, H.M.P.D. Bandara, [e21052@eng.pdn.ac.lk](mailto:e21052@eng.pdn.ac.lk)

## Supervisors
- Ms. Yasodha Vimukthi, [yasodhav@eng.pdn.ac.lk](mailto:yasodhav@eng.pdn.ac.lk)

## Table of Contents
1. [Introduction](#introduction)
2. [Solution & Impact](#solution--impact)
3. [Features & Architecture](#features--architecture)
4. [How to Run](#how-to-run)
5. [Deployment](#deployment)
6. [Links](#links)

---

## Introduction

PeraVerse is a lightweight event management web application developed for EngEx 2025.

Our team was responsible for building the Single Event Details Page, which serves as the user’s main interaction point for viewing detailed event information, marking interest, sharing events, and navigating to the rating system.
This page is fully responsive, deployed in the cloud, and connected to a real backend and database.

## Solution & Impact

The Single Event Details Page provides:

- A clear, intuitive interface for exploring event information
- A dynamic Interested system stored with anonymous user cookies
- Real-time interested count updates
- A mobile-friendly share feature (Web Share API)
- A photo carousel for event images
- Direct integration with the rating/feedback page
- A modern, cloud-hosted full-stack experience

This improves user engagement, event visibility, and user interaction within the PeraVerse ecosystem.

## Features & Architecture

### Key Features
- Event Details Section: Title, date, time, description, venue
- Status Badge: Upcoming / Ongoing / Ended (time-based logic)
- Photo Carousel: Swipeable images with arrows + dots
- Interested Button: Mark/unmark interest, with optimistic UI updates
- Share Button: Mobile share popup / Desktop URL copy
- Rate Event Button: Redirects to the rating page

### Architecture Overview
- **Frontend:** React + Vite, React Router, CSS (Responsive with media queries)
- **Backend:** Node.js + Express, REST API Routes (/api/events/:id, /status, /interested, /photos)
- **Database:** Supabase PostgreSQL, Tables: events, event_photos, interested_events, event_categories
- **Deployment:** Frontend: Vercel, Backend: Vercel Serverless Functions, Database: Supabase Cloud

## How to Run

1.  **Clone Repository**
    ```bash
    git clone https://github.com/cepdnaclk/e21-co227-PeraVerse-Event-Details-Page.git
    cd e21-co227-PeraVerse-Event-Details-Page
    ```

2.  **Install Dependencies**

    *Frontend*
    ```bash
    cd frontend
    npm install
    npm run dev
    ```
    *Backend*
    ```bash
    cd backend
    npm install
    npm start
    ```

3.  **Environment Variables**
    Edit `.env` file inside the `backend`:
    ```
    SUPABASE_URL="Your Supabase URL"
    SUPABASE_ANON_KEY="Your Supabase Anon Key"
    SUPABASE_SERVICE_KEY="Your Supabase Service Key"
    NODE_ENV=development
    PORT=3000
    ```

4.  **Running the System Locally**
    - Start backend on http://localhost:3000
    - Start frontend on http://localhost:5173
    - Navigate to the Event List Page
    - Click any event → opens the Single Event Details Page

## Deployment

The complete system is deployed on Vercel:

- Frontend: https://peraverse-events.vercel.app
- Backend: Deployed as Vercel serverless API
- Database: Supabase Cloud

All environment variables are stored securely in Vercel.

## Links
- [Live Application](https://peraverse-events.vercel.app/)
- [Project Repository](https://github.com/cepdnaclk/e21-co227-PeraVerse-Event-Details-Page)
- [Department of Computer Engineering](http://www.ce.pdn.ac.lk/)
- [University of Peradeniya](https://eng.pdn.ac.lk/)

### Tags
`React` `Vite` `Express.js` `Node.js` `Supabase` `Full-Stack` `Cloud Deployment` `Vercel` `Event Management`
