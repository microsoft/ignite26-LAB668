# 2 - Build the app with Copilot Studio

## Exercise 2 — Copilot Studio:

Copilot Studio supports enterprise agents, workflows and now apps. This exercise specifically uses **app creation**, not agent or workflow creation.

1. Open +++https://copilotstudio.microsoft.com/+++. Confirm you are in the lab tenant.
1. Select App from the homepage.
1. Type +++In Copilot Studio, create LAB668 Onboarding — Studio as a managed app.+++ Then copy the entire **App brief text** block below and paste it into the same prompt. Copy the entire **JSON demo data fixture** block and paste it after the brief. Copy only the contents of each block, not the backticks. Create a separate app rather than importing a previous exercise's app.

    **App brief text**

    ```
    Create a supported interactive managed app for this lab, not a static HTML
    page, agent, or workflow. Use the exercise's LAB668 Onboarding title.

    Display a fictional onboarding checklist with task, owner role, and status.
    Status choices must be Not started, In progress, and Complete.
    Show the total task count and counts by status. Allow filtering by status,
    adding a task, and editing a task's status. Require a nonempty task name.
    Keep the interface small, readable, and keyboard usable.

    Start with the pasted JSON fixture. Label the screen "Fictional lab data".
    Use session-local or illustrative local state; do not connect to enterprise
    data or promise durable, shared, cross-user storage. State that edits may
    reset when reopened. Do not add a backend, call agents or workflows, or
    request additional services. Keep scope to this brief.

    Prepare the app for the entry point's supported Copilot Managed Runtime
    publish/deploy path. Do not treat a preview or source-code update as a
    confirmed hosted deployment.
    ```

    **JSON demo data fixture**

    ```json
    [
      {
        "id": "T1",
        "task": "Review welcome guide",
        "ownerRole": "New starter",
        "status": "Complete"
      },

      {
        "id": "T2",
        "task": "Confirm equipment checklist",
        "ownerRole": "IT coordinator",
        "status": "In progress"
      },

      {
        "id": "T3",
        "task": "Schedule team introduction",
        "ownerRole": "Team lead",
        "status": "Not started"
      },

      {
        "id": "T4",
        "task": "Read security basics",
        "ownerRole": "New starter",
        "status": "Not started"
      }
    ]
    ```

    Once the brief and JSON data are both in the same prompt, send it to Copilot Studio.

    ![Prompt input](../img/02.1-prompt.png)

1. Generate and preview it. Run the standard preview test; request at most one focused correction.
    ![Generate and preview](../img/02.2-generate-and-preview.png)

1. Confirm “Fictional lab data” is visible and no enterprise connection was required. Keep the app self-contained for this exercise.
1. Use Studio's publishing button to host the app in Copilot Managed Runtime. Now you can review the intended audience and capture the hosted deployment link.
    ![Share and play](../img/02.3-share-button.png)

1. Open that link independently in a new tab or click play to see the published app.

1. Return to authoring and request this final revision:

    ```
    Keep the existing app and fixture unchanged.
    Add a light/dark mode switch so users can choose either appearance.
    Preserve all existing interactions.
    ```

1. Preview the revision, publish it, and reopen the hosted link to confirm the switch works in both modes.

**Checkpoint:** A Studio-authored supported app runs at its hosted link, or the worksheet honestly records a demonstration-only outcome. Apps built in Studio can use connectors, but cannot call agents or workflows from the app.
