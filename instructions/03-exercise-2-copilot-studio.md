# 2 - Build the app with Copilot Studio

## Exercise 2 — Copilot Studio:

Copilot Studio supports enterprise agents, workflows and now apps. This exercise specifically uses **app creation**, not agent or workflow creation.

> **Feature gate:** If users are unable to create using MCS, this segment becomes a facilitator demonstration using the [shared app brief and fixture in Exercise 1, step 5](02-exercise-1-cowork.md).

Use the shared [app brief and JSON demo data fixture from Exercise 1, step 5](02-exercise-1-cowork.md).

1. Open +++https://copilotstudio.microsoft.com/+++. Confirm you are in the lab tenant.
1. Select App from the homepage.
1. Type +++In Copilot Studio, create LAB668 Onboarding — Studio as a managed app.+++ Then paste the common brief and fixture. Create a separate app rather than importing a previous exercise's app.
   ![Prompt input](../img/02.1-prompt.png)

1. Generate and preview it. Run the standard preview test; request at most one focused correction.
   ![Generate and preview](../img/02.2-generate-and-preview.png)

1. Confirm “Fictional lab data” is visible and no enterprise connection was required. Keep the app self-contained for this exercise.
1. Use Studio's publishing button to host the app in Copilot Managed Runtime. Now you can review the intended audience and capture the hosted deployment link.
   ![Share and play](../img/02.3-share-button.png)

1. Open that link independently in a new tab or click play to see the published app.

**Checkpoint:** A Studio-authored supported app runs at its hosted link, or the worksheet honestly records a demonstration-only outcome. Apps built in Studio can use connectors, but cannot call agents or workflows from the app.
