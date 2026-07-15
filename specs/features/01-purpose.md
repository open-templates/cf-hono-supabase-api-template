---
type: Feature
title: Purpose
description: Thin Hono worker between Supabase-authenticated SPA and Supabase services.
tags: [backend, hono, cloudflare, supabase]
timestamp: 2026-07-15T00:00:00Z
---

# Purpose

Authentication is delegated to Supabase; the worker validates access tokens and performs server-side operations that should not run in the browser.

Pairs with [react-supabase-auth-template](https://github.com/open-templates/react-supabase-auth-template).
