# Architecture and boundaries

## Components

| Component | Responsibility | Status |
| --- | --- | --- |
| ElevenLabs Agents | Voice interaction, model orchestration and conversation interface | Prototype platform selected |
| System prompt | Discovery, conditional questions, guardrails and next-step recommendation | Documented |
| Greeting | AI disclosure, purpose and privacy reminder | Documented |
| Post-call analysis | Extract confirmed facts and score the interaction | Reference configuration; deployment unverified |
| Human review | Review uncertain regulatory matters and diagnostic completeness | Proposed manual process |
| CRM, live tariffs and freight APIs | Potential future integrations | Not connected in this prototype |

## Conversation design

1. Capture the customer's main objective.
2. Ask product-specific questions based on the intended use.
3. Clarify quantity, origin, destination, supplier status and value when available.
4. Identify potential checks, not definitive regulations.
5. Summarize confirmed facts and ask the customer to correct errors.
6. Recommend a proportionate next step; do not claim to execute it.

## Data flow

Voice input is processed by the configured platform. The conversational model generates short responses based on the prompt. If enabled, post-call analysis produces separate structured fields and evaluation labels. A human reviewer compares these against the conversation record and resolves uncertain findings. No external persistence, automated handoff or integration is implemented by this repository.

## Trust and privacy

Use synthetic data only in the demonstration. Do not request identifiers, credentials, bank details or supplier documents. Review platform recording, retention, access and deletion settings before inviting anyone to test. Do not publish raw transcripts or recordings with identifying details. Confirm figures, distinguish supplier location from country of origin, and leave missing facts unknown rather than guessing. Human review is required before using outputs for a real operation.

## Failure handling

If speech recognition is ambiguous, ask for clarification. If the customer corrects a number, use the corrected confirmed value. If a conversation ends early, mark completion as false or unavailable rather than successful. If the platform cannot extract a field, leave it unknown and log it for review.
