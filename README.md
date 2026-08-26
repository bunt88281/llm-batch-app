# llm-batch-app

Batch prompt runner with retries and progress

Side project, maintained when I have time.

## Examples

```bash
python batch.py prompts.jsonl -o answers.jsonl --workers 4
```

## Install

```bash
pip install -r requirements.txt
export OPENAI_API_KEY=sk-...
```

## Highlights

- Retries failed items with backoff, logs them aside
- Idempotent: skips ids already present in the output
- JSONL in, JSONL out: stream-safe for huge inputs
- Concurrent workers with a rate ceiling

## Project structure

```text
├── .github/
│   ├── ISSUE_TEMPLATE/
│   │   └── bug_report.md
│   ├── dependabot.yml
│   └── pull_request_template.md
├── docs/
│   ├── faq.md
│   └── usage.md
├── tests/
│   └── test_smoke.py
├── .gitattributes
├── .gitignore
├── CHANGELOG.md
├── CODE_OF_CONDUCT.md
├── CONTRIBUTING.md
├── LICENSE
├── batch.py
├── prompts.sample.jsonl
└── requirements.txt
```

## License

MIT. Do whatever you want.
