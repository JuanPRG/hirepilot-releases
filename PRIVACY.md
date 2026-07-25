# HirePilot Privacy Policy

Effective date: July 23, 2026

HirePilot is a Chrome extension and local Windows companion application for
tailoring resumes and cover letters to a job posting and, at the user's
request, assisting with application-form filling.

## Summary

- HirePilot does not operate a developer-owned data collection server.
- The Chrome extension communicates with the HirePilot companion backend on
  the user's own computer at `http://127.0.0.1:7321`.
- When a user requests AI generation or matching, the local backend sends the
  information needed for that task to the AI provider that the user configured.
- HirePilot does not sell personal data, use it for advertising, or track
  browsing activity.
- HirePilot does not collect click, scroll, keystroke, mouse-position, or
  network-monitoring activity and has no analytics or telemetry.

## Data HirePilot Processes

HirePilot may process the following data when the user invokes a feature:

- Resume and profile information, including name, contact details, location,
  work history, education, skills, work authorization, and compensation
  preferences that the user chooses to provide.
- Content from the active job page, including its URL, employer, job title,
  job description, and visible application-field labels and options.
- Tailored resume text, cover letters, generated documents, and the user's
  output and prompt preferences.
- Operational records such as local error logs, model/provider attempt names,
  timing reports, and local tailor-job state.

HirePilot does not read or fill passwords, one-time authentication codes,
credit-card fields, security codes, Social Security numbers, Social Insurance
Numbers, or file-upload controls. Existing values from application fields are
not sent to the backend.

## When Page Access Occurs

HirePilot accesses only the active tab after the user opens the extension,
uses its context-menu action, presses Reset, Tailor, Fill, or Re-fill, or
otherwise directly invokes a HirePilot action. It does not continuously track
pages or maintain a browsing-history service.

## Where Data Goes

The extension sends task data only to the local HirePilot backend on the same
computer. The backend may then:

- Process data locally with deterministic code.
- Send relevant job, resume, profile, prompt, or form-schema data to the hosted
  AI providers that the user has configured, such as Groq, Cerebras,
  OpenRouter, or Google Gemini.
- Send data to a user-configured local OpenAI-compatible model instead of a
  hosted provider.

Hosted AI requests use the provider's HTTPS API and are subject to that
provider's own terms and privacy policy. Users choose which providers to
configure and supply their own API keys. HirePilot's developer does not receive
those requests or API keys.

## Local Storage And Retention

The Chrome extension uses Chrome storage for current job context, generated
resume text, UI state, and output preferences. Session data is scoped to the
browser session; selected preferences may persist until the extension data is
cleared or the extension is removed.

The Windows companion stores profile and resume inputs, provider
configuration, prompt preferences, local logs, prompt snapshots, timing
reports, and job state under `%USERPROFILE%\.hirepilot`. Generated user
documents are saved directly in the user's Downloads folder. These files
remain until the user deletes them.

Uninstalling the Windows application preserves `.hirepilot` by design so an
upgrade or reinstall does not destroy the user's profile and configuration.
To remove all local HirePilot data, stop HirePilot, remove the extension, and
delete `%USERPROFILE%\.hirepilot` plus any generated files in Downloads.

Hosted providers may retain request data according to their own policies and
the user's account settings. HirePilot does not control provider retention.

## Data Sharing And Use

HirePilot uses data only to provide user-requested resume tailoring, cover
letters, document generation, form assistance, local diagnostics, and product
configuration. It does not:

- Sell or rent user data.
- Use user data for advertising or personalized advertising.
- Transfer data to data brokers.
- Use data for creditworthiness, lending, insurance, or employment decisions.
- Collect analytics or telemetry for the developer.

Data is shared only with AI providers configured by the user when needed to
perform a requested task, or when the user intentionally shares generated
files or diagnostics.

## Chrome Web Store Limited Use

HirePilot's use and transfer of information received from Google APIs complies
with the Chrome Web Store User Data Policy, including its Limited Use
requirements:

- Data is used only to provide or improve HirePilot's single purpose and
  user-facing features.
- Data is transferred only when necessary to provide those features, when the
  user intentionally requests a transfer, for security, or as required by law.
- Data is never used or transferred for personalized, retargeted, or
  interest-based advertising.
- Humans do not read user data as part of normal operation. Human access would
  occur only with the user's specific consent for support, when necessary for
  security, when required by law, or after data is aggregated and anonymized
  for permitted internal operations.

## Security

The companion backend listens on the computer's loopback interface, and the
extension's host permission is limited to `127.0.0.1`. Hosted-provider traffic
uses HTTPS. No security measure is absolute, and users should protect their
Windows account and provider API keys.

## User Choices

Users can:

- Choose which AI providers to configure, including a local model.
- Choose which documents to generate.
- Review and edit all generated content before using it.
- Disable or remove the extension at any time.
- Delete Chrome extension storage, `.hirepilot`, and generated Downloads files.

## Changes

Material changes will be published in this file with a new effective date.

## Contact

For privacy questions or deletion help, open an issue at
https://github.com/JuanPRG/hirepilot-releases/issues. Do not include API keys,
resume contents, or other sensitive personal information in a public issue.
