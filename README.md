# Contribute to Open-source Workshop (COW🐮) 2025

<p align="center">
  <img width="100" alt="devs-logo" src="frontend/public/devs-favicon.svg" />
</p>

## Architecture

## Getting Started

### 1. Prerequisites

Make sure you have the following installed:

- **Node.js** v18 or later (we use v23)
- **npm** (comes with Node.js)
- **Git**

Node.js can be installed [here](https://nodejs.org/en/download). Once downloaded, you can check your Node version with:

```bash
node -v
```

### 2. Clone the Repository

```bash
git clone https://github.com/devsuoa/contribute-to-open-source-workshop-2025.git
cd contribute-to-open-source-workshop-2025
```

### 3. Environment Variables

There are two `.env` files. One of them should be placed in the `frontend` folder, the other should be placed in the `backend` folder.

Create a frontend `.env` and add the following line:

```env
VITE_API_BASE_URL=http://localhost:3000
```

Create a backend `.env` and add the following line:

```env
PORT=3000
```

Your project tree should look like this:

![env](/images/env.png)

‼️‼️Note that this is for demonstration purposes only. **DO NOT** ever leak your `.env` content to the public, treat them like passwords.

### 4. Install Dependencies

`npm install` in both the `frontend` and `backend` directory seperately:

```bash
cd frontend
npm install
```

```bash
cd backend
npm install
```

![install](/images/install.png)

### 5. Initialise Database

Run the `init-db.ts` script in `backend/src/db` by the following command (while in the `backend` directory):

```bash
npm run init-db
```

This will clear the existing database and populate it with the values defined in the script. The database is located at `backend/database.sqlite`.

### 6. Start the App

`npm run dev` in both the `frontend` and `backend` directory seperately. In other words, run `npm run dev` for both the frontend and backend in separate terminal tabs:

```bash
cd frontend
npm run dev
```

```bash
cd backend
npm run dev
```

## Making a Contribution

These git actions can be performed anywhere in the project directory (unless there is a git submodule, which we don't in this example).

### 1. Create a Branch

```bash
git checkout -b your-branch-name
```

There are usually naming conventions for branches. For introducing a new feature, use `feature/your-feature-name`. For fixing a bug, use `bugfix/your-bug-name`.

### 2. Commit Changes

After you have made changes, stage and commit them to your local repository:

```bash
git add .
git commit -m "Your commit message"
```

### 3. Push Changes

Push you changes so everyone else can see them:

```bash
git push origin your-branch-name
```

After sucessfully pushing, you should be able to see a notification on GitHub to create a pull request.

![pr](/images/pr.png)

### 4. Create a Pull Request

Click on "Compare & pull request", add a description of your changes, and submit the pull request.

The description usually includes:

- A description on the purpose and effect of the change
- How to test if the change works as intended

### 5. Checks and Review

Now your pull request is ready for review. However, it needs to pass the formatting and linting checks first.

![review](/images/review.png)

If it fails like the image above, go into your `frontend` and `backend` directories and run:

```bash
npm run format
npm run lint
```

Then commit these automatic changes and push again.

## Activities

We are excited to announce the DEVS online contest platform 🎉🎉🎉! However, due to underpaid and overworked developers, there are some ~~unintended bugs~~ "unique features" 👀. We need your help to make it better!

### Easy

#### E1: No Sekrit Dokuments

Currently, when you make a submission the expected value will be shown in the submissions tab. We don't want that! Remove it on the frontend.

#### E2: 

### Medium

#### M1: Seeing Double

In `backend/src/routes/api/submissions.ts`, the POST method to make a submission will create a new entry to the `competition_user_status` table every time a submission is made. We don't need to do that if the user already has a previous entry to this competition!

#### M2: 

- Path protection

### Hard

#### H1:

- User registration

#### H2:

- Competition Leaderboard
