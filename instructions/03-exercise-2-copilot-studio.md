# 2 - Build the app with Copilot Studio

## Exercise 2 — Copilot Studio:

Copilot Studio supports enterprise agents, workflows and now apps. This exercise specifically uses **app creation**, not agent or workflow creation.

### Get started

1. Open +++https://copilotstudio.microsoft.com/+++.
1. Select **App** from the homepage.

    ![Select the App card](../img/02.0-select-app-card.png)

### Prepare the prompt

Create a separate app rather than importing a previous exercise's app. The prompt describes the desired app, its behaviors and accessibility, fictional data and storage boundaries, and publishing expectations.

1. Copy the entire prompt below and paste it once into the Copilot Studio prompt box. Copy only the contents of the block, not the backticks.

    ```text
    Create LAB668 Onboarding - Studio as a managed app.

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

1. Review the complete prompt, including all four fictional tasks, then send it to Copilot Studio.

    ![Prompt input](../img/02.1-prompt.png)

### Build and test the app

1. Allow Copilot Studio to generate the app. Generation builds the source files and an interactive preview, which may appear before the agent finishes. You can inspect the preview when it becomes available, but wait until initial generation finishes before requesting a correction or publishing.

    **Optional:** Open [Create an app in Microsoft Copilot Studio](https://learn.microsoft.com/microsoft-copilot-studio/apps-experience/create-app) in a separate browser tab while you wait, then switch back to the Copilot Studio browser tab containing the app editor and conversation.

1. Once generation finishes, test the interactive preview. Confirm the original four tasks appear, with a total of four, one **Complete**, one **In progress**, and two **Not started**. Test status filtering and editing, restore any changed status, and confirm an empty task name cannot be added. Check that the controls can be used with the keyboard. Request at most one focused correction, and wait for it to finish before continuing.

    ![Generate and preview](../img/02.2-generate-and-preview.png)

1. Confirm “Fictional lab data” is visible and no enterprise connection was required. Keep the app self-contained for this exercise.

1. In the interactive app preview, use **Add a task** to create two fictional onboarding tasks:

    1. Enter +++Schedule welcome meeting+++ as the task name.
    1. Enter +++Team lead+++ as the owner role.
    1. Select **Not started** as the status, or keep it if already selected.
    1. Click **Add task**.
    1. Repeat these steps to add +++Set up workstation+++ with owner role +++IT coordinator+++ and status **In progress**.

    Confirm both tasks appear in the list and the total task count increases by two. These preview edits may reset when you open the app.

### Publish the app

1. Select the **Publish** button on the top right to host the app in Copilot Managed Runtime. Review the intended audience and capture the app link, but do not share the app with others in this lab.

    Publishing makes the requested version separately available; a working preview alone does not confirm publication. Wait for publishing to finish before using the app link to verify this version.

    ![Share and play](../img/02.3-share-button.png)

1. While publishing completes, review the default **full-screen** layout. Select the **Device preview** icon (a phone and monitor) in the toolbar once to switch to the **Tablet** layout, then select the same icon again to switch to the **Mobile** layout. Inspect each layout and confirm the app remains clear and usable at each size.

    ![Device preview icon in the toolbar](../img/02.4-device-preview-icon.png)

    ![App in the mobile preview layout](../img/02.5-mobile-preview.png)

1. Once publishing finishes, open the app using the link in a new browser tab or click play. Confirm the published checklist and task interactions work as expected.

### Add and publish light/dark mode

1. Switch back to the Copilot Studio browser tab containing the app editor and conversation. Request this final revision:

    ```
    Keep the existing app and fixture unchanged.
    Add a light/dark mode switch so users can choose either appearance.
    Preserve all existing interactions.
    ```

1. After the revision finishes, preview it and confirm the switch works in both modes and the checklist interactions still work.

1. Select **Publish** again and wait for publishing to finish. Reopen or refresh the published app in its browser tab to confirm the switch works in both modes.

### Inspect the generated code

1. Switch back to the Copilot Studio browser tab containing the app editor and conversation. Select the **Code view** icon (`</>`) within the editor to inspect the generated code. Open the **src** folder and select **App.tsx** to view one of the generated files. Feel free to inspect the other source files. To switch back to the app view within the same editor, select the **App preview** icon.

## Exercise end

You built and published a separate app with Copilot Studio, then added a light/dark mode switch as a revision. You reopened the app to confirm the switch works in both modes and inspected its generated source in **Code view**.

Select **Next** to continue to the following section.
