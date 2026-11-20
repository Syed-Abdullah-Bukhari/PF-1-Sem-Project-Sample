# CodeQuest

## Project Overview

CodeQuest is an interactive web-based coding game that helps beginners learn web development by completing practical missions instead of only reading theory. The game teaches three core web development courses:

1. **HTML** - Learn how to create the structure of a webpage using elements, headings, paragraphs, images, forms, tables, and semantic tags.
2. **CSS** - Learn how to design and style webpages using colors, fonts, spacing, borders, layouts, animations, and responsive rules.
3. **JavaScript** - Learn how to add logic and interactivity using variables, conditions, loops, functions, events, arrays, and DOM manipulation.

Learners complete coding challenges, quizzes, bug-fixing tasks, ordering activities, and live-preview exercises. They earn XP, stars, badges, and achievements as they progress through the courses.

## Project Objectives

- Introduce HTML, CSS, and JavaScript in a simple and engaging way.
- Convert coding lessons into short game missions.
- Help beginners practice real code instead of only learning theory.
- Give immediate feedback through live previews and challenge checks.
- Track player progress, XP, stars, and achievements.
- Provide a modern, responsive, and interactive learning experience.

## Main Features

- Separate courses for HTML, CSS, and JavaScript
- Multiple levels for each course
- Beginner-friendly mission instructions
- Multiple-choice, fill-in-the-blank, code, matching, ordering, and bug-fixing tasks
- Live preview for practical coding exercises
- Player XP and level system
- Star ratings and achievement badges
- Course and overall progress tracking
- Device/browser save support
- Optional PostgreSQL cloud save support
- Responsive design for desktop and mobile browsers

## Technologies Used

- Next.js
- React
- TypeScript
- Tailwind CSS
- PostgreSQL
- Drizzle ORM

## Learning Structure

### HTML Course

The HTML course teaches learners how webpages are structured. Topics include:

- HTML document structure
- Headings and paragraphs
- Links and images
- Lists and tables
- Forms and input elements
- Semantic HTML

### CSS Course

The CSS course teaches learners how to style webpages. Topics include:

- Colors and typography
- Margins and padding
- Borders and backgrounds
- Classes and selectors
- Flexbox and Grid
- Animations and responsive design

### JavaScript Course

The JavaScript course teaches learners how webpages can react and perform actions. Topics include:

- Variables and data types
- Operators and conditions
- Loops
- Functions
- Arrays and objects
- Events
- DOM manipulation

## Requirements

- Node.js 20 or newer
- npm
- A modern web browser
- Optional: PostgreSQL database for cloud progress storage

## Installation and Local Setup

1. Open the project folder in VS Code or another code editor.
2. Open a terminal in the project folder.
3. Install dependencies:

```bash
npm install
```

4. Start the development server:

```bash
npm run dev
```

5. Open the game in a browser:

```text
http://localhost:3000
```

## Production Build

To create and start an optimized production version:

```bash
npm run build
npm run start
```

## Database and Progress

CodeQuest can store progress in the browser or in PostgreSQL.

### Device/Browser Save

If PostgreSQL is unavailable or not configured, progress is saved in the current browser. This allows the game to work locally without a database.

### PostgreSQL Cloud Save

A PostgreSQL database can be configured using the following environment variable:

```text
DATABASE_URL=postgresql://username:password@host:5432/database
```

This value should be placed in a `.env.local` file in the project root or configured in a hosting provider's environment settings.

## Sharing the Project

### For a Teacher or Local Demonstration

Run the project locally and present it in the browser:

```bash
npm run dev
```

Then open:

```text
http://localhost:3000
```

### For a Class on the Same Wi-Fi Network

Start the server on all network interfaces:

```bash
npm run start -- --hostname 0.0.0.0 --port 3000
```

Find the host computer's IPv4 address using:

```bash
ipconfig
```

Students can open:

```text
http://YOUR-IPV4-ADDRESS:3000
```

All devices must be on the same network. Windows Firewall must allow the connection to port `3000`.

### For Internet Access

The project can be uploaded to GitHub and deployed through a hosting platform such as Vercel. Hosting creates a public link that can be shared with teachers, friends, or students. An `.exe` file is not required because CodeQuest is a web application.

## Useful Commands

| Command | Purpose |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Build the production version |
| `npm run start` | Start the production server |
| `npm run lint` | Check code quality |
| `npm run typecheck` | Check TypeScript types |

## Troubleshooting

### Application does not open

Make sure the server is running and open `http://localhost:3000` in the browser.

### Port 3000 is already in use

Start the project on another port:

```bash
npm run dev -- --port 3001
```

Then open `http://localhost:3001`.

### Database is unavailable

Confirm that `DATABASE_URL` is correct and that the PostgreSQL server is reachable. If the database is unavailable, CodeQuest will use browser/device storage.

## License

This project can be used for educational and demonstration purposes. Add a license before public distribution if required.
