# Next.js 15 Runtime Error in Production: Undefined Variable

This repository demonstrates a common runtime error in Next.js 15 applications that occurs when an undefined variable is accessed in a production environment.  The error is not consistently caught during development.

## Issue Description

A simple Next.js application is created with two pages: a home page and an about page. The about page contains a `console.log` statement that attempts to access an undefined variable.  This causes a runtime error in production but often goes unnoticed during development.

## Steps to Reproduce

1. Clone this repository.
2. Install dependencies: `npm install`
3. Run the development server: `npm run dev` (Error will not show in dev, may require a production build to reproduce)
4. Build the application: `npm run build`
5. Run the production server: `npm run start`
6. Navigate to `/about`.  A runtime error will be thrown.

## Solution

The solution is simple.  Ensure all variables are properly defined and handled before being accessed.  Adding error handling or conditional checks can prevent this type of runtime error.