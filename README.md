# React Router Dom v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router Dom v6.  The problem arises because the catch-all route, intended to handle 404 errors, unintentionally matches all other routes, leading to incorrect page rendering.

## Problem

The `/*` route in the example code matches all paths, including the home route `/`. This causes the `NotFound` component to render instead of the `Home` component when navigating to `/`.

## Solution

The solution involves reordering the routes. By placing the catch-all route after other more specific routes, we ensure it only matches paths that don't match any of the other routes.