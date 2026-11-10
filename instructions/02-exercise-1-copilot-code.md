# 1 - Build the app with Copilot Code

## Exercise 1 — Copilot Code:

Build, publish, and then revise the same app in this exercise.

1. Open Microsoft Edge (a shortcut is on the desktop).
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

    ![Enter the managed-app prompt in Copilot Code](../img/01.2-enter-managed-app-prompt-in-code.png)

1. After sending the prompt, confirm the activity shows **Used skill app-generation**. Allow generation to finish, then confirm you received an interactive app rather than only an explanation or static document, and observe its authoring preview. If the activity is not shown, ask the facilitator how to proceed; do not try an undocumented command to trigger it.
    ![Copilot Code showing the app-generation skill activity](../img/01.3-app-generation-skill-activity.png)

1. If the app doesn't open to the side, select **Open** at the bottom of the chat conversation or select **Open LAB668 Onboarding** under **Output**.
    ![Open the generated LAB668 Onboarding app](../img/01.4-open-lab668-onboarding.png)

1. **Optional:** Expand the app by selecting the expand icon highlighted at the upper-right of the Preview pane.
    ![Expand the app in the Preview pane](../img/01.5-expand-app-preview.png)

1. When you're ready to return to the conversation, select the restore-size icon highlighted below to return the app canvas to its previous size.
    ![Restore the app canvas to its previous size](../img/01.6-restore-preview-size.png)

1. Run a standard preview test, ensuring everything is working. Then request this focused task-form change:

    ```
    Keep the existing app and fixture unchanged.
    Move the existing task form into an accessible modal opened by a **New task** button with a Cancel option.
    Preserve all existing interactions.
    ```

1. Preview the change. Confirm **New task** opens the form in a modal that can be operated with the keyboard, and **Cancel** closes it without adding a task. Verify filtering and status editing still work, restoring any status you change.
    ![LAB668 Onboarding preview before opening the New task modal](../img/01.7-standard-preview.png)
    ![New task form displayed in an accessible modal](../img/01.8-new-task-modal.png)

1. In the interactive app preview, use the **New task** modal to add two fictional onboarding tasks:

    1. Select **New task** to open the modal for the first task.
    1. Enter +++Schedule welcome meeting+++ as the task name.
    1. Enter +++Team lead+++ as the owner role.
    1. Select **Not started** as the status, or keep it if already selected.
    1. Select **Add task**.
    1. Select **New task** again to open the modal for the second task.
    1. Enter +++Set up workstation+++ as the task name.
    1. Enter +++IT coordinator+++ as the owner role.
    1. Select **In progress** as the status.
    1. Select **Add task**.

    Confirm both tasks appear in the list and the total task count increases by two. These preview edits may reset when the app is reopened.

1. Select **Publish** in the Preview pane. Wait for the **Your app is published** confirmation.

1. In the publishing confirmation, select **Open app**. Use the same lab account if needed, and confirm the published app looks and works as expected.
    ![Select Open app in the publishing confirmation](../img/01.9-open-in-browser.png)

1. Return to authoring and request this small change:

    ```
    Keep the app and fixture unchanged. Change the visible app title to
    "LAB668 Onboarding — Code v2" and add this sentence below it:
    "Practice checklist: fictional data; session edits may reset."
    Keep all existing interactions working.
    ```

    ![Authoring change](../img/01.10-authoring-change.png)

1. Confirm the new title and sentence in preview.
1. In the Copilot Code conversation, type +++Publish it live+++ and send the prompt to publish the app with the latest changes. Wait for confirmation that publishing has completed.
1. Reopen or refresh the app independently of authoring. Confirm “Code v2” and the new sentence appear, then test filtering and adding a task again.
    ![Refresh after publish](../img/01.11-refresh-after-publish.png)

1. Check the title.
    ![Confirm changes](../img/01.12-confirm-changes.png)

1. Return to authoring and request this final revision:

    ```
    Keep the existing app and fixture unchanged.
    Add a progress bar showing the percentage of tasks marked Complete; update it when tasks are added or their status changes.
    Preserve all existing interactions.
    ```

1. Preview the revision. Verify the progress percentage matches completed tasks divided by total tasks. For reference, the original four-task fixture yields 25%, while six tasks with one complete yield about 17%. Change a task's status and add a task using the existing **New task** button; confirm the percentage updates after each change and existing filtering and status editing still work.
    ![Completion progress bar showing 25 percent with one of four tasks complete](../img/01.13-completion-progress-bar.png)

1. In the Copilot Code conversation, type +++Publish it live+++ and send the prompt to publish the app with the latest changes. Wait for confirmation that publishing has completed.
    ![Publish it live prompt sent in the Copilot Code conversation](../img/01.14-publish-progress-revision.png)

1. After the revision is published, reopen the app. Verify the progress percentage updates after a status change and a new task, and confirm the existing **New task** modal and **Cancel** option still work.

## Exercise end

You built and published an app with Copilot Code, updated its title, moved task creation into an accessible **New task** modal, and added a completion progress bar. You reopened the app to confirm the percentage updates and task interactions work.

Select **Next** to continue to the next exercise.
