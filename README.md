# Visual Procedure Coach

**Follow the task. Understand the steps. Find the moment something went wrong.**

A camera can record a procedure without understanding it. A useful assistant needs to follow the sequence, notice a possible mistake, and show the evidence that led to its conclusion.

Visual Procedure Coach is being built around that idea: a video application for reviewing physical procedures, with live guidance as a later milestone.

## The experience

1. Choose a supported procedure and upload a recording.
2. Review a timeline of recognized steps and possible mistakes.
3. Open the relevant video clip, inspect the evidence, and correct the interpretation.

The intended live-camera experience will use only footage already observed, with explicit uncertainty when an action is hidden or ambiguous.

## Current status

**Early development.** Small model-feasibility pilots have been run. A reliable improvement from fine-tuning has not yet been demonstrated. This repository starts the application project; it does not contain a finished product or a production release.

Accuracy, false alerts per hour, and end-to-end live feedback latency remain to be established. Proposed targets are not achieved results.

## Build sequence

- [ ] Recording upload, playback, and a synchronized review timeline
- [ ] Step recognition for a small, explicitly supported procedure library
- [ ] Timestamped mistake candidates with supporting clips
- [ ] Model adaptation and comparisons against strong baselines
- [ ] Continuous-video evaluation without supplied step boundaries
- [ ] Live-camera input, interruption recovery, and reproducible deployment

## Planned stack

Python · PyTorch · PEFT · FastAPI · Docker

## Evaluation principles

Measure recognition quality together with false alerts and detection delay. Keep participants separate across training and evaluation where the data permits. Report the procedure coverage, hardware, sampling settings, failures, and limitations alongside each result.

A successful isolated clip prediction is not evidence of reliable live coaching. The application must make that distinction visible.
