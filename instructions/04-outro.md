# Outro

## Hosted access, developer bridge, and governance:

### Verify access and sharing

Choose one app you successfully deployed. Open its hosted link independently and demonstrate one interaction. Where approved sharing controls are available, grant only the designated lab partner or group access. Have that partner open the link using their own approved account; do not exchange credentials. If no authorized partner is available, observe the facilitator's access test.

A link is not itself a permission grant. App-use permission, source edit permission, and rights to a connected data source are distinct. The fixture demonstrates no enterprise-data authorization, and two users may see separate local state.

### Presenter-led SDK/CLI bridge

Discussion for how developers with tenant access and app edit rights can clone editable source from platform-managed Git using the supported CLI and continue in compatible tools. That developer path has prerequisites such as the CLI, Node.js, and Git credential management; attendees do not need to install anything here.

The conceptual sequence is **obtain source → edit locally → build/preview → deploy → share**. Pushing source to Git is not live deployment. SDK/CLI guidance covers configuration, typed data services, local development, preview, deployment, and sharing; use current documentation for exact commands, packages, and supported app requirements.

### Presenter-led administration

The presenters will, using an approved administrator account, will show the relevant validated app-management view in **Microsoft 365 administration** and identify available identity, access, and data controls.

## Session validation:

- [ ] I opened at least one app I deployed at a hosted link outside authoring preview.
- [ ] I tested fixture counts, filtering, task creation, and status editing.
- [ ] I verified the Cowork revision after republishing, or recorded why it was not completed.
- [ ] I can explain preview versus deployment, and app sharing versus data rights.

Keep a private note of your app titles and hosted links. Remove only your own lab apps and sharing grants through supported lifecycle controls if instructed. Do not delete prepared shared apps, data sources, or tenant settings. The organizer supplies the retention policy; there is no scripted cleanup in this guide.

## Troubleshooting

| Symptom | Action |
| --- | --- |
| Entry point or publish controls missing | Confirm account/tenant with facilitator; use the approved demonstration |
| Generation stalls or app is noninteractive | Try one focused correction, then use fallback at the cutoff |
| Preview works but hosted link fails | Check deployment outcome, URL type, signed-in account, and authorized audience |
| Hosted app still shows the old title | Confirm republish completed and reopen the current deployment link |
| Connector asks for unexpected consent | Stop; core exercises require no connector or additional permissions |

Rehearse both exercises with an attendee-equivalent account. Measure generation, publish, and Cowork republish against the cutoffs; verify fixture tests, permissions, and independent hosted access. Check the Studio feature gate explicitly. Prepare separate fallback apps in advance, including the Cowork before/after revision.

### Continue learning

+++https://learn.microsoft.com/en-us/microsoft-365/managed-apps/+++
