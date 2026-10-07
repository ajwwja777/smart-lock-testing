# Smart Lock Testing

A smart-lock project covering requirements analysis, user story design, black-box testing, and user experience validation. The repository brings together the product demonstration, test documentation, UI prototypes, and implementation references.

Developed during a testing internship at **iSoftStone, Xi’an, China**, from **July to August 2025**, advised by **Bin Wang**.

## Demo

[Watch / download the smart-lock demo](materials/Demo.mp4)

[View the project presentation](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E6%99%BA%E8%83%BD%E9%97%A8%E9%94%81%E4%BA%A7%E5%93%81%E6%B1%87%E6%8A%A5.pptx) for the product overview and project walkthrough.

## Feature scope

| Area | Features covered by the project documentation |
|---|---|
| Authentication and access | Fingerprint, password and RFID unlocking; credential registration, deletion and freezing |
| Remote access | Remote unlocking, temporary passwords, account-to-lock association and MQTT communication |
| Access records | Unlocking log synchronization, storage, filtering and identity management |
| Security and feedback | Incorrect-attempt alerts, abnormal-event notifications and low-battery reminders |
| User interface | App interaction design and a web-based UI prototype |

## Testing approach

Testing follows user-facing operations across the lock and application, with Story identifiers connecting feature descriptions to test steps.

- **Requirements analysis:** define expected functionality and security behavior before describing test scenarios.
- **User stories:** organize operations such as fingerprint deletion, temporary password generation and identity editing around user goals.
- **Black-box tests:** describe actions and expected outcomes, including whether access still works after a credential is removed.
- **User experience validation:** check confirmation messages, application state, identity labels and access-log visibility.
- **Functional defect analysis:** compare observed behavior with the expected result and use the documented steps to support reproduction and reporting.

See [test procedures](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E6%B5%8B%E8%AF%95/%E6%B5%8B%E8%AF%95%E6%AD%A5%E9%AA%A4.md) and [updated test cases](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E6%B5%8B%E8%AF%95/%E6%9B%B4%E6%96%B0%E7%9A%84%E6%B5%8B%E8%AF%95%E7%94%A8%E4%BE%8B.md) for concrete examples.

## Project documents

| Document | Purpose |
|---|---|
| [Functional requirements](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E9%9C%80%E6%B1%82%E4%B9%A6/%E9%9C%80%E6%B1%82%E4%B9%A6-%E5%8A%9F%E8%83%BD.md) | Product behavior and feature requirements |
| [Security requirements](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E9%9C%80%E6%B1%82%E4%B9%A6/%E9%9C%80%E6%B1%82%E4%B9%A6-%E7%B3%BB%E7%BB%9F%E5%AE%89%E5%85%A8.md) | Security-related requirements |
| [User stories and feature checklist](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/story%EF%BC%88%E6%9C%80%E6%96%B0.md) | Authentication, remote control and safety features |
| [Test procedures](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E6%B5%8B%E8%AF%95/%E6%B5%8B%E8%AF%95%E6%AD%A5%E9%AA%A4.md) | Story-linked test steps and expected outcomes |
| [Updated test cases](materials/%E5%AD%A6%E6%A0%A1%E5%AE%9E%E4%B9%A0%EF%BC%88%E4%B8%B4%E6%97%B6%EF%BC%89/%E6%B5%8B%E8%AF%95/%E6%9B%B4%E6%96%B0%E7%9A%84%E6%B5%8B%E8%AF%95%E7%94%A8%E4%BE%8B.md) | Additional and revised test scenarios |
| [Story spreadsheet template](materials/%E5%BE%AE%E4%BF%A1%E6%96%87%E4%BB%B6/Story%E5%88%97%E8%A1%A8_%E6%A8%A1%E6%9D%BF-v1.xlsx) | Supporting story-documentation template |
| [UI prototype](materials/%E5%BE%AE%E4%BF%A1%E6%96%87%E4%BB%B6/ui.zip) | Archived web interface prototype |
| [Implementation reference](materials/%E5%BE%AE%E4%BF%A1%E6%96%87%E4%BB%B6/%E6%99%BA%E8%83%BD%E9%97%A8%E9%94%81%E6%BA%90%E7%A8%8B%E5%BA%8F%EF%BC%88%E5%89%8D30%E9%A1%B5%EF%BC%89.docx) | Source-code excerpts with connection credentials redacted |

## Repository structure

```text
smart-lock-testing/
├── README.md
├── materials/
│   ├── Demo.mp4
│   ├── 学校实习（临时）/      # Requirements, tests, notes and presentation
│   └── 微信文件/              # Collected documents, prototypes and earlier versions
├── source-manifest.json       # File inventory and SHA-256 checksums
└── redaction-report.json      # Credential redaction record
```

Original filenames, document versions and duplicate copies are retained to preserve the project record. The collected materials also include shared templates and general reference documents.

## Using the materials

Start with the demo and presentation, then follow the requirements, stories and test procedures. Download Word, Excel and PowerPoint files to view them locally. Extract `ui.zip` to inspect the archived interface prototype.

This repository preserves historical project documents and source excerpts; a complete buildable firmware/application package and a deployment guide are not currently included.

## Publication notes

Wi-Fi connection details and MQTT credentials in the two source-code Word copies have been replaced with `REDACTED`. The original local files are preserved. `source-manifest.json` records original and published checksums, and `redaction-report.json` identifies the edited copies.
