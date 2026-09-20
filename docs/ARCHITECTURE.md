# Architecture

## Tech Stack
- **Backend:** Node.js with Express (Chosen for fast, asynchronous handling of webhooks).
- **Database:** MongoDB (Chosen for flexible schemas to store patient profiles and triage logs).
- **Voice API:** Twilio (Industry standard for Programmable Voice and IVR routing).

## Data Flow
- A user calls the toll-free Twilio number.
- Twilio triggers a webhook to the Express server.
- The server processes the input, queries/updates MongoDB, and responds with TwiML (Twilio Markup Language) to play the next audio prompt.

## Key Entities
- **Patient:** Stores phone number, language preference, and basic profile.
- **TriageLog:** Records the symptoms collected during the IVR call.
- **Doctor:** Stores availability and routing numbers for final consultation handoff.
