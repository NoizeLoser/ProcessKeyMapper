

# Contributing to ProcessKeyMapper

Thank you for your interest in contributing to ProcessKeyMapper.

ProcessKeyMapper is a source-available project maintained and controlled by its Original Author. Community contributions are welcome, but all changes to the Official Repository are subject to review and approval by the Original Author.

By participating in this project, you agree to follow the requirements described in this document and in [`LICENSE.md`](LICENSE.md).
Capitalized terms used but not defined in this document have the meanings assigned to them in LICENSE.md.

---

## 1. General Contribution Principles

Before proposing a contribution, please understand the following principles:

- The Official Repository is controlled exclusively by the Original Author.
- Contributors do not receive direct write access to the Official Repository.
- All external contributions must be submitted through a personal fork and Pull Request.
- The Original Author has the final decision on whether a contribution is accepted, modified, postponed, or rejected.
- Submitting a Pull Request does not guarantee that the proposed changes will be included.
- Contributions must comply with the project's license and attribution requirements.

The goal is to maintain the project's architecture, reliability, portability, and design principles.

## 2. How to Submit Code Contributions

All code and functionality contributions must follow this process:

1. Fork the official ProcessKeyMapper repository.
2. Create a separate branch in your fork for the proposed changes.
3. Make and test your changes.
4. Prepare the required explanation and evidence.
5. Submit a Pull Request to the Official Repository.

Do not attempt to push directly to the Official Repository.

## 3. Pull Request Requirements

Every Pull Request proposing code changes, bug fixes, or new functionality must contain a sufficiently detailed explanation.

A Pull Request must describe:

### 3.1 Problem Description

Explain what problem exists and under which circumstances it occurs.

For bug fixes, include reproducible steps whenever possible.

### 3.2 Proposed Solution

Explain:

- What exactly has been changed.
- How the proposed solution works.
- Why this particular approach was chosen.
- Why the change is preferable to leaving the problem unresolved.

### 3.3 Evidence of Functionality

Provide evidence demonstrating that the proposed changes work.

Acceptable evidence includes:

- Screenshots.
- Video recordings.
- Demonstrations of the affected functionality.
- Relevant diagnostic output.
- Reproduction and verification steps.

### 3.4 Regression Considerations

Explain how existing functionality was checked and why the proposed change should not break unrelated parts of the application.

If a change affects multiple components, describe which components were affected and how they were tested.

Incomplete Pull Requests may be rejected or returned for additional information.

## 4. Localization Contributions

Localization proposals follow a mandatory two-stage approval process.

This process applies to:

- Adding a new language.
- Replacing an existing localization.
- Significantly revising an existing translation.

### Stage 1 — GitHub Discussions

Before opening a localization Pull Request, the contributor must create a GitHub Discussion presenting the proposed localization.

The Discussion must include:

1. The language being proposed.
2. The localization file or a representative translation sample.
3. Screenshots of the actual running ProcessKeyMapper GUI using the proposed localization.
4. At least four positive reactions from other users.

**At least four positive reactions are required before proceeding to Stage 2.**

#### Screenshot Requirements

Screenshots must show the running application with the proposed translation applied.

Screenshots of an INI file, text editor, or translation table alone are not sufficient to demonstrate the localization in the application.

The purpose is to allow the community and Original Author to evaluate:

- Translation quality.
- Text readability.
- Button and interface layout.
- Whether translated text is clipped or overlaps other elements.
- General usability of the localization.

#### Critical Error Messages

Critical error messages and diagnostic texts do not need to be demonstrated by intentionally causing system failures.

These translations may be included directly in the Discussion as copied `key=value` lines from the localization INI file.

### Stage 2 — Pull Request

After the Discussion receives at least four positive reactions, the contributor may submit a Pull Request from their fork.

The Pull Request must:

- Link to the original GitHub Discussion.
- Include the proposed localization file.
- Explain why the localization should be added or why it should replace an existing translation.
- Confirm that the localization has been tested in the running application.

Both conventional translations and creative, humorous, or community-oriented translations may be proposed.

The Original Author retains the final decision on whether a localization is accepted.

## 5. Project Architecture and Compatibility

Contributions should respect the established architecture and technical requirements of ProcessKeyMapper.

In particular, contributors should avoid introducing changes that contradict the project's design principles:

- Native C++ and Win32 API implementation.
- No external application frameworks or virtual machines.
- Portable directory structure.
- Dynamic runtime linking (`/MD` or equivalent) with required runtime DLLs bundled locally in the portable directory.
- No unnecessary external DLL dependencies.
- No unnecessary writes to system directories or the Windows registry.
- Separation of responsibilities between Launcher, Watcher, Backend, and GUI.
- External INI-based localization.

A contribution that changes architectural assumptions must clearly explain why the change is necessary and what consequences it introduces.

Do not silently replace an established technical mechanism with a different one.

## 6. Localization File Requirements

Localization files belong in the `locals/` directory.

The three required base localization files are:

- `RU_ru.ini`
- `EN_en.ini`
- `SR_rs.ini`

Every fork must retain support for all three base localizations in accordance with [`LICENSE.md`](LICENSE.md).

Additional community localizations may be proposed through the process described in Section 4.

A localization contribution should preserve the expected INI structure and required keys. Missing or malformed entries may prevent the application from displaying the intended text correctly.

## 7. Bug Reports and Feature Requests

Use the appropriate GitHub Issue template when reporting a problem or proposing an improvement.

For bug reports, provide:

- A clear description of the problem.
- Steps to reproduce it.
- Expected behavior.
- Actual behavior.
- Relevant screenshots, video, or diagnostic information.
- Windows version and relevant application context, when known.

For feature requests, provide:

- A description of the proposed functionality.
- The problem it solves.
- Why it would be useful.
- Examples or references, where appropriate.

Opening an Issue does not guarantee implementation.

## 8. Review and Final Decision

The Original Author personally controls the acceptance of contributions into the Official Repository.

The Original Author may:

- Accept a Pull Request.
- Reject a Pull Request.
- Request changes.
- Ask for additional testing or evidence.
- Select a different destination branch.
- Close a proposal without merging it.

There is no obligation to accept every technically valid contribution.

The final decision is made by the Original Author.

## 9. Licensing and Attribution

All contributions must comply with the project's [`LICENSE.md`](LICENSE.md).

By submitting a contribution, you confirm that:

- You have the right to submit the proposed material and grant the permissions described in this section.
- Your contribution does not knowingly violate third-party rights.
- You understand that acceptance does not transfer ownership or copyright of the Official Repository.
- You agree that the contribution will be distributed under the project's applicable license terms if accepted.
- You retain ownership and copyright of your original contribution.

### 9.1 Contributor License Grant

By submitting a contribution to the Official Repository, the contributor grants the Original Author a perpetual, worldwide, non-exclusive, royalty-free, irrevocable, and sublicensable license to use, reproduce, modify, adapt, create derivative works from, distribute, publish, and otherwise exploit the contribution.

This license includes the right to:

- Incorporate the contribution into the Original Project and any Derivative Works.
- Modify, adapt, or remove the contribution at the Original Author's discretion.
- Distribute the contribution as part of the Original Project or any Derivative Work.
- Authorize third parties to use, modify, distribute, and sublicense the contribution.
- Grant commercial-use permissions involving the contribution, including permissions issued under Section 5 of `LICENSE.md`.

This license grant does not constitute a transfer of copyright ownership. The contributor retains ownership of their original contribution.

The contributor represents that they have the legal right to grant the permissions described in this section.

This grant applies to contributions submitted through Pull Requests, whether or not they are ultimately accepted into the Official Repository.

Do not submit code, assets, or translations copied from third parties unless you have the necessary rights to do so.

## 10. Commercial Use

Contributing to ProcessKeyMapper does not grant permission for commercial use.

Commercial use remains subject to the restrictions and exception procedure described in [`LICENSE.md`](LICENSE.md).

A Pull Request, Issue, Discussion, or private conversation does not constitute commercial-use authorization.

## 11. Final Notes

ProcessKeyMapper is maintained with an emphasis on stability, portability, transparency, and deliberate project direction.

Thoughtful contributions are welcome. Clear explanations, reproducible evidence, and respect for the project's technical principles help make the review process useful for everyone.

Thank you for helping improve ProcessKeyMapper.
