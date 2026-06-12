# Rapid Sentiment Triage for Open-Ended Survey Responses

**The problem:** a survey closes the day before a leadership briefing and there are 1,000+ open-ended comments. Nobody has time to read them all, but leadership needs to know how respondents are feeling, and the most critical comments need human eyes first.

**The approach:** score every response with VADER sentiment analysis within minutes of survey close, then split everything into a "flagged for review" queue and an "other responses" queue. The output is a review-ready Excel workbook with built-in columns for a human analyst to confirm flags, tag themes, and add notes. The model does the sorting; a person does the judging.

**The result:** when I ran this workflow on a real 150-response provider survey, the pipeline took the analysis from survey close to review-ready workbook in under an hour. Leadership had a defensible same-day read on sentiment ahead of potential public statements by a stakeholder association.

## What's in this repo

| File | What it is |
|---|---|
| `sentiment_triage.ipynb` | The full workflow, with narrative explaining each analytical decision |
| `data/synthetic_survey_responses.csv` | Synthetic survey data used to demonstrate the pipeline |

## A note on the data

All data in this repository is **synthetic**, generated to demonstrate the workflow. It mirrors the structure of a real provider survey I analyzed professionally, but contains no real respondents, organizations, or results. The original analysis was conducted on confidential data that cannot be shared.

## Run it yourself

```bash
pip install -r requirements.txt
jupyter notebook sentiment_triage.ipynb
```
