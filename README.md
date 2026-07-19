<a id="readme-top"></a>

[![Contributors][contributors-shield]][contributors-url]
[![Forks][forks-shield]][forks-url]
[![Stargazers][stars-shield]][stars-url]
[![Issues][issues-shield]][issues-url]

<br />
<div align="center">
  <a href="https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation">
    <img src="docs/images/logo-placeholder.svg" alt="n8n Automation - Child Story Creation logo placeholder" width="90" height="90">
  </a>

  <h3 align="center">n8n Automation - Child Story Creation</h3>

  <p align="center">
    Sanitized n8n workflow automation that generates personalized AI childrens storybooks with story scenes, images, PDF conversion, Google Drive storage, and email delivery.
    <br />
    <a href="docs/GITHUB_DESCRIPTION.md"><strong>Explore the docs Â»</strong></a>
    <br />
    <br />
    <a href="#usage">View Usage</a>
    &middot;
    <a href="https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/issues/new">Report Bug</a>
    &middot;
    <a href="https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/issues/new">Request Feature</a>
  </p>
</div>

<details>
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about-the-project">About The Project</a><ul><li><a href="#built-with">Built With</a></li></ul></li>
    <li><a href="#getting-started">Getting Started</a><ul><li><a href="#prerequisites">Prerequisites</a></li><li><a href="#installation">Installation</a></li></ul></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#how-it-works">How It Works</a></li>
    <li><a href="#project-structure">Project Structure</a></li>
    <li><a href="#validation">Validation</a></li>
    <li><a href="#roadmap">Roadmap</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
    <li><a href="#acknowledgments">Acknowledgments</a></li>
  </ol>
</details>

## About The Project

[![Project overview placeholder][project-screenshot]](#usage)

Sanitized n8n workflow automation that generates personalized AI childrens storybooks with story scenes, images, PDF conversion, Google Drive storage, and email delivery.

The repository currently offers:

- Webhook-based story request flow
- AI parsing for character, setting, and theme
- Five-scene story generation
- Scene splitting and image alignment
- AI image generation for each scene
- HTML storybook assembly and PDF conversion
- Google Drive upload and email delivery

This README follows the shared template requested for the repository set and keeps the claims limited to files and documentation present in this project.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Built With

- n8n
- OpenAI
- Hugging Face
- PDFShift
- Google Drive
- SMTP
- JSON

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Getting Started

Follow these steps to clone the repository and run the project locally.

### Prerequisites

- n8n instance
- OpenAI API credential
- Hugging Face API token
- PDF conversion API credential
- SMTP credential
- Google Drive OAuth credential

### Installation

~~~bash
git clone https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation.git
cd n8n-Automation-ChildStoryCreation
Import workflows/child-story-creation.workflow.json into n8n
~~~

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Usage

Useful commands and entry points:

~~~bash
POST /generate-image with character, setting, theme, and email fields
~~~

~~~bash
Reconnect credentials inside n8n
~~~

~~~bash
Test the webhook and activate the workflow
~~~

### Visual Placeholders

Placeholder images are included under `docs/images/` so you can replace them manually later without changing the README layout.

<p align="center">
  <img src="docs/images/project-overview-placeholder.svg" alt="n8n Automation - Child Story Creation overview placeholder" width="48%">
  <img src="docs/images/workflow-placeholder.svg" alt="n8n Automation - Child Story Creation workflow placeholder" width="48%">
</p>

Suggested final visuals:

- Project overview screenshot or main terminal output.
- Workflow, architecture, or data-flow diagram.
- Example result, dashboard, report, or generated artifact screenshot.
- Short GIF only when it is small and useful.

Avoid committing large raw videos, private datasets, credentials, runtime logs, or generated secrets. Use sanitized screenshots and diagrams.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## How It Works

`	ext
Webhook -> OpenAI story planning -> scene generation -> image generation -> HTML storybook -> PDF conversion -> email and Google Drive
`

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Project Structure

- workflows/ - sanitized n8n workflow JSON
- examples/ - sample webhook request
- docs/ - import, setup, security, and workflow overview notes
- README.md - project guide

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Validation

Run the most relevant checks for this repository:

~~~bash
Import the workflow into n8n
~~~

~~~bash
Run examples/sample-request.json through the webhook after credentials are connected
~~~

Some validations depend on local tools, services, datasets, API credentials, or a configured lab environment.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Roadmap

- [ ] Replace placeholder images with final screenshots or diagrams.
- [ ] Keep setup commands synchronized with the current project files.
- [ ] Add more examples or test fixtures when the project grows.
- [ ] Add a repository-level license if the project will be reused outside its original context.

See the [open issues](https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/issues) for proposed features and known issues.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contributing

Contributions are welcome for documentation, examples, tests, and implementation improvements.

1. Fork the project.
2. Create your feature branch:

   ~~~bash
   git checkout -b feature/AmazingFeature
   ~~~

3. Commit your changes:

   ~~~bash
   git commit -m "Add some AmazingFeature"
   ~~~

4. Push to the branch:

   ~~~bash
   git push origin feature/AmazingFeature
   ~~~

5. Open a pull request.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

### Top Contributors

<a href="https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=ahmed3bahaa/n8n-Automation-ChildStoryCreation" alt="Top contributors for n8n Automation - Child Story Creation" />
</a>

## License

No repository-level license file was verified in this project. Add a license before reuse or distribution outside the intended coursework, lab, or prototype context.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Contact

Project owner: [@ahmed3bahaa](https://github.com/ahmed3bahaa)

Project Link: [https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation](https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Acknowledgments

- README structure adapted from [ahmed3bahaa/readme-template](https://github.com/ahmed3bahaa/readme-template).
- Project files, reports, fixtures, and documentation included in this repository.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[contributors-shield]: https://img.shields.io/github/contributors/ahmed3bahaa/n8n-Automation-ChildStoryCreation.svg?style=for-the-badge
[contributors-url]: https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/graphs/contributors
[forks-shield]: https://img.shields.io/github/forks/ahmed3bahaa/n8n-Automation-ChildStoryCreation.svg?style=for-the-badge
[forks-url]: https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/network/members
[stars-shield]: https://img.shields.io/github/stars/ahmed3bahaa/n8n-Automation-ChildStoryCreation.svg?style=for-the-badge
[stars-url]: https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/stargazers
[issues-shield]: https://img.shields.io/github/issues/ahmed3bahaa/n8n-Automation-ChildStoryCreation.svg?style=for-the-badge
[issues-url]: https://github.com/ahmed3bahaa/n8n-Automation-ChildStoryCreation/issues
[project-screenshot]: docs/images/project-overview-placeholder.svg
