# Mapkeeper

## Project Overview

Mapkeeper is a Google Capstone Design project conducted at Ajou University. The project helps small local business owners, especially digitally underserved business owners, manage their online store information more easily.

Many small restaurant owners, especially older owners and digitally underserved owners, have difficulty updating business information across online map services because the current management tools often require complex web forms, multiple menus, and repeated manual updates.

Mapkeeper aims to reduce that burden by providing a simple voice-based assistant. A business owner can speak a short request, such as "Please update today's closing time to 8 PM," and the system converts that request into a structured business information update.

This project is currently being developed for academic and prototype purposes as part of the Google Capstone Design program at Ajou University.

## Organization / Team

- Project name: Mapkeeper
- Korean project name: 맵지기
- Affiliation: Google Capstone Design program at Ajou University
- Target users: Digitally underserved small local business owners, especially older restaurant owners near university districts
- Current stage: Prototype / MVP development

## Problem We Are Solving

Small business owners often need to update information such as:

- Business hours
- Temporary closures
- Special holiday hours
- Menu information
- Store descriptions
- Customer review replies

Our primary target users are digitally underserved small business owners. Many of them run their stores for long hours and are familiar with direct verbal communication, but they may not be comfortable using complex online management dashboards, mobile forms, or repeated manual updates across multiple platforms. For these users, even simple updates such as changing business hours or replying to reviews can become a significant burden.

However, many owners do not update this information regularly because the existing tools are difficult to use during daily store operations. As a result, customers may see outdated business hours, incorrect menu information, or unmanaged reviews.

Mapkeeper is designed to make business profile management easier and more accessible by using voice input, AI-based intent recognition, and clear confirmation steps before any update is submitted.

## Purpose of Using Google Business Profile APIs

We are requesting access to Google Business Profile APIs in order to let verified business owners manage their own Google Business Profile information through the Mapkeeper prototype.

The API will be used only after the business owner signs in with Google and grants the required permission through OAuth.

Our intended API use cases include:

1. Reading the connected business profile information so the owner can review the current store information inside the app.
2. Updating business information such as business hours or special hours after explicit owner confirmation.
3. Updating supported profile attributes where applicable.
4. Helping owners reply to customer reviews after the owner reviews and approves the reply text.
5. Showing update status to the owner after an API request is submitted.

## How the API Will Be Used in the Product

The planned user flow is:

1. The business owner signs in and connects their Google Business Profile account.
2. The owner speaks or types a business information update request.
3. Mapkeeper converts the request into a structured update proposal.
4. The app shows the proposed change to the owner in a confirmation screen.
5. The owner must approve the change before any API update is sent.
6. After approval, Mapkeeper sends the update request to the Google Business Profile API.
7. The app displays the result, such as success, pending, failed, or action required.

Mapkeeper will not automatically publish AI-generated changes without the business owner's explicit approval.

## Example User Scenarios

### Business Hours Update

A restaurant owner says:

> Please close at 8 PM today.

Mapkeeper interprets the request as a temporary business hours update, shows a confirmation screen, and submits the update to the connected Google Business Profile only after the owner approves it.

### Special Closure

A business owner says:

> We are closed tomorrow because of a private event.

Mapkeeper converts the request into a special hours or temporary closure update and asks the owner to confirm before submitting it.

### Review Reply Assistance

A business owner asks:

> Help me reply to recent reviews.

Mapkeeper may draft a reply, but the owner must review and approve the final text before it is submitted as a review reply.

## Data Access and User Consent

Mapkeeper will access Google Business Profile data only for business accounts that the user owns or manages and only after OAuth consent.

We will request only the permissions required for the prototype's business profile management features.

The project will not sell Google Business Profile data, transfer it to third-party advertising services, or use it for unrelated purposes.

## Data Handling

The project is designed with the following data handling principles:

- Business profile data is used only to display, manage, and update the owner's own business information.
- API access tokens are handled on the server side and are not exposed to the mobile client.
- Sensitive credentials and tokens will be stored securely.
- AI-generated suggestions are treated as drafts and require user confirmation.
- Logs will be used only for debugging, update status tracking, and academic prototype evaluation.
- Customer review data will be handled only for review analysis and reply assistance features.

## Google API Scope Usage

The primary OAuth scope expected for this project is:

```text
https://www.googleapis.com/auth/business.manage
```

This scope is needed so verified business owners can manage their own business profile information through the Mapkeeper prototype.

## What We Will Not Do

Mapkeeper will not:

- Modify a business profile without explicit owner approval.
- Manage profiles that the signed-in user does not own or have permission to manage.
- Scrape Google services.
- Use automated browser control to bypass Google Business Profile policies.
- Sell, share, or use Google Business Profile data for unrelated advertising or data brokerage.
- Generate or publish misleading business information.

## MVP Scope

For the MVP, Google Business Profile will be the primary platform for direct API-based updates.

Other map platforms may be supported only through manual guidance or deep links if they do not provide a public official write API. This project will follow each platform's policies and will not attempt to bypass API restrictions.

## Contact

For questions about this project, please contact the Mapkeeper capstone team.

- Project: Mapkeeper
- Affiliation: Google Capstone Design program at Ajou University
- Contact email: TODO: add team contact email
