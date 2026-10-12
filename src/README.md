# Source

Paste this prompt, that's an app brief into the app-creation experience, with the JSON demo data fixture below. Add the entry-point sentence shown in each exercise.

```text
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

```json
[
  {"id":"T1","task":"Review welcome guide","ownerRole":"New starter","status":"Complete"},
  {"id":"T2","task":"Confirm equipment checklist","ownerRole":"IT coordinator","status":"In progress"},
  {"id":"T3","task":"Schedule team introduction","ownerRole":"Team lead","status":"Not started"},
  {"id":"T4","task":"Read security basics","ownerRole":"New starter","status":"Not started"}
]
```