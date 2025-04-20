# Commit GPT
**Get chat GPT to write your commit messages**

This project generates concise commit messages based on the `git diff` information of your staged changes. It uses GPT-4 via the OpenAI API to create clear and effective commit messages. The messages aim to be brief, summarizing small changes with a simple title or separating multiple unrelated changes with bullet points.

## Prerequisites

- Git installed on your machine
- Python 3.x
- OpenAI API Key

## Installation

1. Clone this repository:

   ```bash
   git clone <repository-url>
   ```

2. Ensure you have required dependencies (install via `pip` if needed):

   ```bash
   pip install openai
   ```

## Setup

### API Key

You need to set the OpenAI API key in your environment. You can do this by exporting it in your terminal session:

```bash
export OPENAI_API_KEY='your-api-key'
```

Make sure to replace `'your-api-key'` with your actual OpenAI API key.

### Default Instructions

The script comes with default instructions to generate commit messages. These are already specified in the script:

```
"Generate a concise commit message based on the diff information provided. If there are multiple, unrelated changes, separate them with bullet points. For small or simple changes, only provide a brief title. Avoid using any formatting, code blocks, or indicators like 'Title:' or 'Body:'. Keep it short and straightforward."
```

### Custom Instructions

To override the default instructions, create a file at `~/.commit_message_instructions` and write your custom instructions in it. The script will automatically load these instructions if the file exists.

## Usage 

For each version controlled project, copy `prepare-commit-msg` to the `.git/hooks/` directory.

## License

This project is open-source and available under the [MIT License](LICENSE).
