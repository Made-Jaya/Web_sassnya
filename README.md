# Apple-Style Portfolio Template

[English](README.md) | [简体中文](README.zh-CN.md)

A modern, minimalist portfolio template built with Astro and designed with Apple's design aesthetic in mind.

live demo: [apple-style-portfolio](https://apple-style-portfolio.larryxue.dev/)

If you find this project helpful, please consider giving it a star ⭐️.

## Features

- 🍎 Apple-style design aesthetic
- ⚡️ Built with Astro for optimal performance
- 🎨 Tailwind CSS for styling
- 🌟 GSAP animations
- 📱 Fully responsive design
- 🎬 Three.js integration for 3D elements
- ⚛️ React components integration

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
  - [Development](#development)
  - [Building for Production](#building-for-production)
- [Deployment](#deployment)
  - [Deploy with Vercel](#deploy-with-vercel)
  - [Deploy with Cloudflare Pages](#deploy-with-cloudflare-pages)
- [Docker Deployment](#docker-deployment)
  - [Prerequisites](#prerequisites-1)
  - [Running with Docker](#running-with-docker)
  - [Docker Commands Reference](#docker-commands-reference)
- [Tech Stack](#tech-stack)
- [License](#license)

## Getting Started

### Prerequisites

- Node.js (v20 or higher)

### Installation

1. Clone the repository:

```bash
# Clone the repository
git clone https://github.com/larry-xue/apple-style-portfolio
cd apple-style-portfolio

# Or use astro create
npm create astro@latest -- --template larry-xue/apple-style-portfolio
```

2. Install dependencies:

```bash
npm install
```

### Development

To start the development server:

```bash
npm run dev
```

The site will be available at `http://localhost:4321`

### Building for Production

To create a production build:

```bash
npm run build
```

To preview the production build:

```bash
npm run preview
```

## Deployment

### Deploy with Vercel

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/larry-xue/apple-style-portfolio)

1. Fork this repository
2. Connect to Vercel using your GitHub account
3. Select the forked repository
4. Vercel will automatically detect Astro and configure the build settings
5. Click "Deploy"

### Deploy with Cloudflare Pages

[![Deploy to Cloudflare Pages](https://img.shields.io/badge/Deploy%20to-Cloudflare%20Pages-orange.svg?logo=cloudflare)](https://dash.cloudflare.com/sign-up)

1. Fork this repository
2. Log in to the Cloudflare dashboard
3. Select "Pages" from the sidebar
4. Create a new project and connect your GitHub repository
5. Configure the build settings:
   - Build command: `npm run build`
   - Build output directory: `dist`
   - Node.js version: 20.x
6. Click "Save and Deploy"

## Docker Deployment

### Prerequisites
- Docker installed on your system
- Port 80 available on your host machine

### Running with Docker

1. Build the Docker image (this may take a few minutes as it builds the Astro application):
```bash
docker build -t apple-portfolio .
```

2. Run the container:
```bash
# Run in detached mode
docker run -d -p 80:80 apple-portfolio

# Or run in interactive mode to see the logs
docker run -it -p 80:80 apple-portfolio
```

The application will be available at `http://localhost`

### Docker Commands Reference
- View running containers:
```bash
docker ps
```

- Stop the container:
```bash
docker stop $(docker ps -q --filter ancestor=apple-portfolio)
```

- Remove the container:
```bash
docker rm $(docker ps -aq --filter ancestor=apple-portfolio)
```

- View container logs:
```bash
docker logs $(docker ps -q --filter ancestor=apple-portfolio)
```

- Rebuild and run (useful during development):
```bash
docker build -t apple-portfolio . && docker run -d -p 80:80 apple-portfolio
```

- Use a different port (e.g., 8080):
```bash
docker run -d -p 8080:80 apple-portfolio
```

## Tech Stack

- [Astro](https://astro.build)
- [React](https://reactjs.org)
- [Tailwind CSS](https://tailwindcss.com)
- [GSAP](https://greensock.com/gsap)
- [Three.js](https://threejs.org)
- [Inter Font](https://rsms.me/inter)
- [Source Sans Pro](https://fonts.google.com/specimen/Source+Sans+Pro)

## License

MIT License
