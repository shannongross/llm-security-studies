# LLM security studies

Small, measured studies of attacks on LLM applications and the defenses against them.
Each study is a notebook that runs from saved results.

All data here is synthetic. The setting is a fictional food bank that uses an AI assistant
to read intake notes. No real organization or person is involved.

## Studies

| # | Question | Result | Main limit |
|---|---|---|---|
| [001](001-injection-detector/injection_detector.ipynb) | Can a detector catch prompt injection in intake notes? | An LLM judge caught all 21 attacks it answered with 0 false alarms, and gave no answer on 3. A keyword list caught 13 of 24 and flagged 5 real notes. | 58 hand-written notes, one model, one prompt |

## Run

```
pip install -r requirements.txt
jupyter notebook
```

The notebooks load saved predictions, so no API key is needed. Cells that call a model are
marked optional and read `ANTHROPIC_API_KEY` from an env file.
