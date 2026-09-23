# Echos — AI Meeting & Voice-Memo Assistant

**Built solo for the AssemblyAI Voice Agent Hackathon**

## What it does

Echos turns a spoken voice memo or meeting recording into a clear, structured record. Record audio directly in the browser or upload an existing file, and Echos returns:

- A full transcript with confidence score
- An AI-generated summary
- Key highlighted phrases
- Overall sentiment analysis (positive / neutral / negative)

## The problem

Meetings and voice memos are easy to record but hard to act on. Important context gets buried in raw audio nobody re-listens to. Echos closes that gap: talk, and get a structured, readable record back in under a minute.

## How it works

1. **Capture** — record audio in-browser via the Web Audio API (`MediaRecorder`), or upload an existing audio file. This works across all major browsers, not just Chrome.
2. **Upload** — the audio is sent to AssemblyAI's `/v2/upload` endpoint.
3. **Transcribe & analyze** — a single AssemblyAI transcript request enables summarization, auto-highlights, and sentiment analysis in one call.
4. **Poll & display** — the app polls AssemblyAI until the job completes, then renders the transcript, summary, key phrases, and sentiment breakdown.

## Tech stack

- Vanilla HTML / CSS / JavaScript — no build step, no framework
- Browser `MediaRecorder` API for cross-browser audio capture
- [AssemblyAI API](https://www.assemblyai.com/) for transcription, summarization, highlight extraction, and sentiment analysis
- Single self-contained file — runs anywhere, including GitHub Pages

## Try it

Live demo: *https://github.com/Youssef-El-Attaoui/Echos-Voice-Agent/*

To run locally: download `index.html`, open it in any browser, paste in a free AssemblyAI API key, and start recording or upload an audio file.

## Team

Solo build — Youssef.

## Notes

Built end-to-end during the hackathon window, from problem framing to a working, API-integrated demo. Possible next steps: multi-speaker detection, exporting summaries to PDF/Notion, and a history of past transcripts.
