# lollms_prompts_zoo

![License: Apache 2.0](https://img.shields.io/badge/License-Apache%202.0-blue.svg)
![Maintainer: ParisNeo](https://img.shields.io/badge/Maintainer-ParisNeo-blue)
![Chat Prompts](https://img.shields.io/badge/Prompts-lollms%20chat-green)
![Issues](https://img.shields.io/github/issues/ParisNeo/lollms_prompts_zoo)
![Forks](https://img.shields.io/github/forks/ParisNeo/lollms_prompts_zoo)
![Stars](https://img.shields.io/github/stars/ParisNeo/lollms_prompts_zoo)

A collection of prompts designed for the lollms chat application.

## Overview

This repository offers a library of diverse prompts to enhance user experience on the lollms platform. Each prompt is designed to address specific needs (creativity, productivity, assistance, etc.) and facilitate the integration of new use cases into the application.

## Repository Structure

- `ux_design_assistant/`: Example assistant for UX/UI design, including description, icon, and prompt.
- Each folder contains:
  - `description.yaml`: Metadata and description of the prompt.
  - `prompt.txt`: Prompt text usable in lollms.
  - `icon.png`: Icon associated with the prompt.

## Standard Prompt Structure

Each prompt should be placed in its own folder and include the following files:

- `description.yaml`: Contains metadata about the prompt (author, category, description, creation date, etc.).
- `prompt.txt`: The actual prompt text, with placeholders for user input.
- `icon.png`: An icon representing the prompt.

### Placeholders Declaration and Usage

Placeholders allow you to customize prompts dynamically. They are declared in `prompt.txt` using the following format:

```
@<placeholder_name>@  
title: Placeholder Title  
type: str | text | int | float  
options: Option1, Option2, ... (optional)  
help: Description of the placeholder  
@</placeholder_name>@  
```

Supported types: `str`, `text`, `int`, `float`.

To use a placeholder in your prompt, reference it as `@<placeholder_name>@`.

**Example:**
```txt
@<platform>@  
title: Target Platform  
type: str  
options: Web, Mobile (iOS), Mobile (Android), Desktop  
help: The platform you are designing for.  
@</platform>@  

@<max_items>@  
title: Maximum Items  
type: int  
help: The maximum number of items to generate.  
@</max_items>@  

Based on the platform: @<platform>@, generate up to @<max_items>@ items.
```

### description.yaml Structure

The `description.yaml` file should follow this structure:

```yaml
author: YourName
category: CategoryName
creation_date: 'YYYY-MM-DDTHH:MM:SS'
description: Brief description of the prompt.
disclaimer: Any disclaimer or usage notes.
last_update_date: 'YYYY-MM-DDTHH:MM:SS'
model: ModelName
name: Prompt Name
version: 1.0
```

**Example:**
```yaml
author: ParisNeo & Lollmz
category: Design & Creativity
creation_date: '2025-08-06T11:00:00.000000'
description: An assistant for generating user interface and experience design recommendations based on user needs, product goals, and style preferences.
disclaimer: This assistant provides generalized suggestions and should be reviewed by a UX professional before implementation.
last_update_date: '2025-08-06T11:00:00.000000'
model: GPT-4o
name: UX Design Assistant
version: 1.0
```

## Usage

1. Clone this repository:
   ```sh
   git clone https://github.com/ParisNeo/lollms_prompts_zoo.git
   ```
2. Add the desired prompts to your lollms installation.
3. Customize or create your own prompts following the proposed structure.

## Contributing

Contributions are welcome! Submit your prompts via pull requests or open an issue to suggest improvements.

## License

This project is licensed under the [Apache 2.0](LICENSE) license.

---
