<h1 align="center">Hi, I'm Mateo Del Rio Usma 👋</h1>

<p align="center">
  <b>Senior Ruby on Rails Engineer · Tech Lead</b><br>
  Backend, PostgreSQL, APIs and Rails upgrades
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/mateo-del-rio-usma/"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&amp;logo=data:image%2Fsvg%2Bxml;base64,PHN2ZyBmaWxsPSJ3aGl0ZSIgcm9sZT0iaW1nIiB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI%2BPHBhdGggZD0iTTIwLjQ0NyAyMC40NTJoLTMuNTU0di01LjU2OWMwLTEuMzI4LS4wMjctMy4wMzctMS44NTItMy4wMzctMS44NTMgMC0yLjEzNiAxLjQ0NS0yLjEzNiAyLjkzOXY1LjY2N0g5LjM1MVY5aDMuNDE0djEuNTYxaC4wNDZjLjQ3Ny0uOSAxLjYzNy0xLjg1IDMuMzctMS44NSAzLjYwMSAwIDQuMjY3IDIuMzcgNC4yNjcgNS40NTV2Ni4yODZ6TTUuMzM3IDcuNDMzYy0xLjE0NCAwLTIuMDYzLS45MjYtMi4wNjMtMi4wNjUgMC0xLjEzOC45Mi0yLjA2MyAyLjA2My0yLjA2MyAxLjE0IDAgMi4wNjQuOTI1IDIuMDY0IDIuMDYzIDAgMS4xMzktLjkyNSAyLjA2NS0yLjA2NCAyLjA2NXptMS43ODIgMTMuMDE5SDMuNTU1VjloMy41NjR2MTEuNDUyek0yMi4yMjUgMEgxLjc3MUMuNzkyIDAgMCAuNzc0IDAgMS43Mjl2MjAuNTQyQzAgMjMuMjI3Ljc5MiAyNCAxLjc3MSAyNGgyMC40NTFDMjMuMiAyNCAyNCAyMy4yMjcgMjQgMjIuMjcxVjEuNzI5QzI0IC43NzQgMjMuMiAwIDIyLjIyMiAwaC4wMDN6Ii8%2BPC9zdmc%2B"></a>
  <a href="https://www.upwork.com/freelancers/~01c0ffe177ba00ed7c"><img alt="Upwork" src="https://img.shields.io/badge/Upwork-14A800?style=for-the-badge&amp;logo=upwork&amp;logoColor=white"></a>
</p>

## About me

- 💼 6 years building production SaaS with Ruby on Rails, in US healthcare and hospitality.
- 🧭 Tech Lead today: Rails and PostgreSQL architecture, code reviews and mentoring.
- 🔧 What I do best: safe Rails upgrades, slow queries and N+1s, background jobs and APIs.
- 🤖 Integrated an AI model that writes clinical notes on a US healthcare platform, raising insurer acceptance and saving over $90K a month.
- 🎓 Master's in Software Engineering (in progress) and a bachelor's in Marketing, both at Universidad de Medellín.
- 🌎 English (C1) and Spanish (native). Medellín, Colombia (UTC-5).

## Featured project: Gym Membership Manager

Front desk software for small gyms in Colombia, which I built on my own with Rails 8.1 and PostgreSQL 17. It handles members identified by their ID documents, plans and session packs, memberships with freezes, payments, check-in by document number, and an access reader at the door. It's deployed to production.

<p align="center">
  <img src="assets/gym-membership-manager/demo.gif" width="280" alt="The front desk on a phone: a member with visits left checks in, one whose plan expired is offered a renewal, and the simulated reader opens for an active member and stays closed for a frozen one">
</p>

- **Multitenancy**: several gyms share one installation, each with its own staff, roles and settings. acts_as_tenant scopes every query to the current gym, and Pundit authorizes every action.
- **Rules the database enforces**: PostgreSQL exclusion constraints stop overlapping memberships and freezes, even when two sales race, and a partial unique index lets a pack spend one visit a day at most.
- **Privacy by design**: under Colombian Law 1581, biometric data never reaches the app. The reader keeps the fingerprints, and the app only sends it which member IDs may enter and until when, through an `AccessGateway` a real device plugs into.
- **Operations**: deployed with Kamal to a VPS over HTTPS, with nightly backups to Cloudflare R2, a restore I've tested, and errors, uptime and backups watched in Sentry.
- **Tests**: nearly 900 RSpec examples, with Capybara system specs at phone width, run in GitHub Actions along with RuboCop and Brakeman.

| Member page | Expirations | Simulated reader |
|---|---|---|
| ![A member's page: a frozen month and a renewal the freeze pushed back](assets/gym-membership-manager/member.png) | ![Members ending soon, with their phone, plan and end date](assets/gym-membership-manager/expirations.png) | ![The simulated reader stays closed for a frozen member, and the app records the attempt as frozen](assets/gym-membership-manager/reader.png) |

The code is private. If you'd like to read it, [write to me on LinkedIn](https://www.linkedin.com/in/mateo-del-rio-usma/) and I'll share it with you.

## Tech stack

![Ruby, Rails, PostgreSQL, Redis, JavaScript, Git and Linux](https://skillicons.dev/icons?i=ruby,rails,postgres,redis,js,git,linux)
