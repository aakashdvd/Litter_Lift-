# Contributing to Litter Lift

Thanks for your interest in contributing! This document explains how to get the project running locally and how to propose changes.

## Getting Started

1. Fork the repository and clone your fork.
2. Install dependencies with `npm install`.
3. Copy `.env.example` to `.env` and fill in the required values.
4. Start the development server with `node app.js`.

## Branching

- Create a feature branch from `main` using a descriptive name, for example `feat/leaderboard-filters` or `fix/map-marker-icons`.
- Keep branches focused on a single change.

## Commit Messages

We follow a lightweight Conventional Commits style:

- `feat:` a new feature
- `fix:` a bug fix
- `docs:` documentation only changes
- `style:` formatting, missing semicolons, etc.
- `refactor:` code change that neither fixes a bug nor adds a feature
- `test:` adding or updating tests
- `chore:` build process or auxiliary tool changes

## Pull Requests

- Make sure the app still starts (`node app.js`) before opening a PR.
- Describe what changed and why in the PR body.
- Link any related issues.
- Keep diffs small and reviewable.

## Reporting Issues

When opening an issue, please include:

- Steps to reproduce
- Expected behaviour
- Actual behaviour
- Browser / OS / Node version where relevant

Thanks for helping make Litter Lift better!
