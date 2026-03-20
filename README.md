# IT Help Desk Dashboard

A fully functional, browser-based IT help desk application built with vanilla HTML, CSS, and JavaScript. Designed to simulate a real enterprise support environment with role-based access, live ticket management, real-time chat, and a built-in troubleshooting knowledge base.

---

## Overview

This project was built as a portfolio piece to demonstrate practical IT operations knowledge and full-stack web development skills. It requires no framework, no backend, and no installation — open the HTML file in any browser and it runs immediately.

The application supports two distinct portals accessed through a shared login screen: a **User portal** for employees submitting and tracking support requests, and an **Admin portal** for IT staff managing the ticket queue and communicating with users in real time.

---

## Features

### Authentication & Role-Based Access
- Login screen with role selection — **User** or **IT Staff / Admin**
- Each role routes to a completely separate portal with its own permissions and views
- Session state is cleared on sign-out, including ticket data and chat history

### User Portal
- Submit new support tickets with category, subcategory, priority, affected device, and full description
- View all personal open tickets filtered by priority (P1–P4)
- Track ticket progress through a live status timeline (Open → In Progress → Resolved)
- View assigned agent, estimated resolution time, and agent notes per ticket
- Submit star-rating feedback when a ticket is resolved
- Browse a self-help knowledge base with articles covering common issues across all six categories
- Live chat panel on each ticket for direct communication with IT staff
- Floating chat bubble for messaging support without leaving the current page

### Admin Portal
- Full ticket dashboard showing all tickets across all users
- Real-time ticket feed with auto-generated tickets every 20 seconds
- **Freeze / Unfreeze** toggle to pause incoming tickets — queued tickets flash in when feed is resumed
- Search by keyword, ticket ID, or reporter name
- Filter by category and priority simultaneously
- Ticket detail workspace with:
  - Live chat panel for direct messaging with the ticket reporter
  - Full ticket controls: assign agent, update status, add internal notes, escalate, mark resolved
  - Reporter info panel showing open ticket count and full history
- **General tips section** — dynamically renders curated troubleshooting tips based on the ticket's category and subcategory, covering all six categories and 18+ subcategory-specific guides
- Chat inbox showing all active conversations with unread counts, message previews, and timestamps
- Escalation tier reference guide (Tier 1 / Tier 2 / Tier 3)

### Live Chat System
- Real-time messaging between users and admin staff, keyed per ticket
- Typing indicators on both sides
- Timestamps on every message
- Read receipts showing when the other party has seen a message
- Admin can mark a ticket resolved directly from the chat, sending an automatic confirmation to the user
- Floating chat bubble on the user side with unread notification badge

### Ticket Management
- Six categories: Network & Connectivity, Hardware & Peripherals, Software & OS, Account & Access, Email & Comm Tools, Security & Compliance
- Dynamic subcategory dropdowns per category
- Four priority levels with a visual priority guide
- Ticket statuses: Open, In Progress, Escalated, Resolved
- Activity feed logging new tickets, escalations, and resolutions
- Volume-by-category bar chart updating in real time

---

## Tech Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 |
| Styling | CSS3 with custom properties (light/dark mode) |
| Logic | Vanilla JavaScript (ES6+) |
| Fonts | Google Fonts — DM Sans, DM Mono |
| Hosting | GitHub Pages (single file, no build step) |

---

## Getting Started

**Option 1 — Direct download**

Download `it_helpdesk_dashboard.html`, open it in any modern browser.

**Option 2 — GitHub Pages**

1. Fork or clone this repository
2. Rename the file to `index.html`
3. Go to **Settings → Pages → Source: main branch**
4. Your live URL will be `https://yourusername.github.io/repository-name`

No npm, no build tools, no dependencies.

---

## Usage

**Signing in as a User**
- Enter your name, select a department, and choose the **User** role
- Submit a ticket using the **+ New ticket** button
- Click any ticket to view its status, track progress, and chat with IT support

**Signing in as Admin**
- Enter your name and choose the **IT Staff / Admin** role
- Click any ticket in the dashboard to open the full detail workspace
- Use the **Live chat** panel to communicate with the reporter
- View the **General tips** section below the workspace for category-specific troubleshooting guidance
- Open **Chat inbox** from the topbar to manage all active conversations
- Use **Freeze** to pause the auto-generated ticket feed during review

---

## Project Structure

```
it_helpdesk_dashboard.html   ← Entire application (single file)
README.md                    ← This file
```

---

## Skills Demonstrated

- Role-based UI architecture and access control
- Real-time state management without a framework or backend
- Event-driven JavaScript patterns (live feed, typing indicators, read receipts)
- Responsive design with CSS Grid and custom properties
- REST API integration structure (Anthropic API pattern)
- Domain knowledge of IT help desk workflows, ticket prioritization, and escalation tiers
- UX design for both end-users and technical staff personas

---

## Author

Built by a graduating MIS student as a portfolio project demonstrating IT operations knowledge and front-end development skills.
