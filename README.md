# LLM security studies

Small, measured studies of attacks on LLM applications and the defenses against them.
Each study is a notebook that runs from saved results.

All data here is synthetic. The setting is a fictional food bank that uses an AI assistant
to read intake form text. No real organization or person is involved.

## Studies

| # | Question | Result | Main limit |
|---|---|---|---|
| [001](001-injection-detector/injection_detector.ipynb) | Can a classifier catch prompt injection in intake form text? | An LLM classifier caught 21 of 24 injected entries with 0 false alarms and gave no answer on the other 3. A keyword classifier caught 13 of 24 and flagged 5 of 34 normal entries. | 58 hand-written entries, one model, one prompt |

## Run

```
pip install -r requirements.txt
jupyter notebook
```

The notebooks load saved predictions, so no API key is needed. Cells that call a model are
marked optional and read `ANTHROPIC_API_KEY` from an env file.
