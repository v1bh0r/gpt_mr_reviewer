# gpt_mr_reviewer
A Gitlab merge request reviewer that uses GPT3 models from openai. This straightforward script gets the MR diffs from Gitlab API, and generates a comment in the merge request.
The default model used is text-davinci-003. The prompt used is "Analyze the following code changes and find issues that need fixing if any. The code changes are in git diff notation, lines starting with - are deleted, lines starting with + are added"

## Prerequisites
- A Gitlab API token, set in environment variable GITLAB_ACCESS_TOKEN
- An OpenAI API key, set in environment variable OPENAI_API_KEY
- Gitlab information in environment variables: GITLAB_URL, GITLAB_PROJECT_ID, GITLAB_MR_ID

Example
```bash
GITLAB_ACCESS_TOKEN=glpat-<snip> OPENAI_API_KEY=sk-<snip> GITLAB_URL=https://gitlab.com/api/v4 GITLAB_PROJECT_ID=207 GITLAB_MR_ID=201 python mr_reviewer.py
```

## Usage
python mr_reviewer.py

## About
Original blog post with how this repo was created: https://medium.com/@mariealice.blete
