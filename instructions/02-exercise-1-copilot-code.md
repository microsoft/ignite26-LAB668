# 1 - Build the app with Copilot Code

## Exercise 1 — Copilot Code:

Build, publish, and then revise the same app in this exercise.

1. Go to +++https://copilot.cloud.microsoft/home+++
1. Sign in using the username and Temporary Access Pass below.

    **Username:** +++@lab.CloudCredential(WWLM365E7).AdministrativeUsername+++<br />
    **Temporary Access Pass:** +++@lab.Variable(TAP)+++

    If a welcome screen appears, click **X** to close it and continue.

1. Select the **Code** button shown in the screenshot.
    ![Select the Code button](../img/01.1-select-code-button.png)

1. In the Copilot Code prompt box, type +++Create LAB668 Onboarding - Code as a managed app+++. Press **Shift + Enter** to insert a new line without sending the prompt.
1. Copy the entire **App brief text** block below and paste it after the request in the same prompt. Copy the entire **JSON demo data fixture** block and paste it after the brief. Copy only the contents of each block, not the backticks. Do not send the prompt yet.

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

    ```
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

    Once the request, brief, and JSON data are all in the same prompt, send it to Copilot Code.

    ![Enter prompt](../img/01.2-use-app-skill-and-enter-prompt.png)

1. Allow generation to finish. Confirm you received an interactive app rather than only an explanation or static document. Observe its authoring preview.
    ![Generating app](../img/01.3-allow-to-finish.png)

1. Run a standard preview test, ensuring everything is working. If needed, type one focused correction such as +++Keep the existing app. Fix only the failing checklist test and preserve the fixture and scope.+++
    ![Generating app](../img/01.4-standard-preview.png)

1. Before publishing, ask the facilitator to confirm the currently supported Copilot Code deployment flow for this lab. Use only that confirmed flow to deploy to Copilot Managed Runtime; if it is unavailable or unconfirmed, pause instead of guessing at controls. Confirm deployment completed; a preview or source-code update is not a confirmed hosted deployment.
1. Open the hosted deployment link provided by the confirmed deployment flow in a new browser tab. Use the same lab account if needed, and confirm the app looks and works as expected.
    ![Open in browser](../img/01.5-open-in-browser.png)

1. Return to authoring and request this small change:

    ```
    Keep the app and fixture unchanged. Change the visible app title to
    "LAB668 Onboarding — Code v2" and add this sentence below it:
    "Practice checklist: fictional data; session edits may reset."
    Keep all existing interactions working.
    ```

    ![Authoring change](../img/01.6-authoring-change.png)

1. Confirm the new title and sentence in preview.
1. Use the confirmed deployment flow to publish the revision. Then reopen or refresh the hosted deployment link independently of authoring. Confirm “Code v2” and the new sentence appear, then test filtering and adding a task again.
    ![Refresh after publish](../img/01.7-refresh-after-publish.png)

1. Check the title.
    ![Confirm changes](../img/01.8-confirm-changes.png)

1. Return to authoring and request this final revision:

    ```
    Keep the existing app and fixture unchanged.
    Add a progress bar showing the percentage of tasks marked Complete; update it when tasks are added or their status changes.
    Add a **New task** button that opens the existing task form in an accessible modal with a Cancel option.
    Preserve all existing interactions.
    ```

1. Preview the revision. Confirm the progress bar initially shows 25% for the fixture's one completed task out of four. Change a task's status and add a task using **New task**; confirm the percentage updates after each change and existing filtering and status editing still work. Verify the modal can be operated with the keyboard, and that **Cancel** closes it without adding a task.
1. Use the confirmed deployment flow to publish the revision, then reopen the hosted link. Verify the progress percentage updates after a status change and a new task, and confirm the **New task** modal and **Cancel** option work there too.

## Exercise end

You built and published an app with Copilot Code, updated its title, and added a completion progress bar and an accessible **New task** modal. You reopened the hosted app to confirm the percentage updates and the task interactions work.

Select **Next** to continue to the next exercise.
