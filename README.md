# Smart Complaint Escalation System

A role-based complaint management platform that automatically routes and escalates service requests based on worker availability, workload, and area — reducing manual coordination between customers, workers, and administrators.

## Overview

The system connects three types of users through a single platform:

- **Customers** — submit complaints or job requests, which are logged into the system.
- **Workers** — register with their job descriptions, skills, and availability.
- **Admins** — oversee the platform and handle escalated cases.

When a complaint comes in, the backend automatically assigns it to a suitable worker based on their **availability**, **current workload**, and **service area**. This removes the need for manual dispatching and speeds up resolution time.

## Escalation Logic

If an assigned worker doesn't accept a task within a set time window (2–3 days), the system automatically:

1. Reassigns the task to the next available worker.
2. Repeats this process until a worker accepts, or the time threshold is exceeded.
3. Escalates the task to a higher authority (admin) if no worker accepts it in time, ensuring nothing falls through the cracks.

## Project Scope

The original design targeted a municipal-wide deployment, with escalation flowing up to city/municipal authorities. Given the timeline of the course project, the scope was deliberately reduced to a **single apartment complex**, with the admin role standing in for the municipal authority. The underlying architecture (roles, routing, and escalation logic) is designed to scale back up to a larger deployment.

## Key Features

- Role-based access for customers, workers, and admins
- Automated, skill- and availability-based task routing
- Time-based automatic escalation to prevent unresolved complaints
- Extensible backend logic to support additional departments or regions

## Planned Improvements

- **Fairness in task routing** — prevent the same worker from being repeatedly skipped or overloaded
- **Configurable escalation windows** — justify and tune the 2–3 day threshold based on real usage data rather than a fixed default
- **Audit/logging trail** — track who was assigned what, when, and why, for traceability when something goes wrong

## Tech Stack

<!-- Fill in the actual languages/frameworks you used, e.g.: Node.js, Express, MongoDB, React -->

## Setup

<!-- Add installation/run instructions once the code is pushed -->
