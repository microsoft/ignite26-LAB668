# 1 - Build the app with Cowork

## App brief

Copy and paste this app brief into the app-creation experience, along with the JSON demo data fixture below. Add the short entry-point sentence shown in each exercise by typing it.

```
Create a supported interactive managed app for this lab, not a static HTML
page, agent, or workflow. Use the exercise's LAB666 Onboarding title.

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

## Exercise 1 — Cowork:

Cowork fits broader work tasks where creating an app is part of getting the work done. Build, publish, and then revise the same app in this exercise.



1. Go to +++[https://copilot.cloud.microsoft/home](https://copilot.cloud.microsoft/home)+++
2. Enter the user name and password.
3. Select the +++Cowork++ button.
![Select Cowork](../img/01.1-select-cowork-button.png)

4. Type +++/app+++.
5. Type +++In Cowork, create LAB666 Onboarding — Cowork as a managed app.+++ Then paste the common brief and fixture.
![Enter prompt](../img/01.2-use-app-skill-and-enter-prompt.png)

6. Allow generation to finish. Confirm you received an interactive app rather than only an explanation or static document. Observe its authoring preview.
![Generating app](../img/01.3-allow-to-finish.png)

7. Run a standard preview test, ensuring everything is working. If needed, type one focused correction such as +++Keep the existing app. Fix only the failing checklist test and preserve the fixture and scope.+++
![Generating app](../img/01.4-standard-preview.png)

8. If your app was not published, click publish to deploy to Copilot Managed Runtime, making your app hosted, secure, governed and shareable.
9. Click **Open in browser**. This will then open it in a new browser tab (make sure you're using the same lab account if you cannot access), confirm the app looks and works the same.
![Open in browser](../img/01.5-open-in-browser.png)

10. Return to authoring and request this small change:

   ```
   Keep the app and fixture unchanged. Change the visible app title to
   "LAB666 Onboarding — Cowork v2" and add this sentence below it:
   "Practice checklist: fictional data; session edits may reset."
   Keep all existing interactions working.
   ```

![Authoring change](../img/01.6-authoring-change.png)

11. Confirm the new title and sentence in preview.
12. Click publish. Then, once published, reopen or refresh the current hosted deployment link independently of authoring. Selected "refresh" on the updated app pop-up. Confirm “Cowork v2” and the new sentence appear, then test filtering and adding a task again.
![Refresh after publish](../img/01.7-refresh-after-publish.png)

13. Check the title.
![Confirm changes](../img/01.8-confirm-changes.png)

**Checkpoint:** A hosted app opens independently of the Cowork preview and shows the revision with working interactions. Preview alone is not completion; iIf publishing fails, observe the prepared hosted app by the lab providers.

---

[Previous: Intro](01-intro.md) | [Lab sections](README.md) | [Next: Exercise 2 - Copilot Studio](03-exercise-2-copilot-studio.md)
