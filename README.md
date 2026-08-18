# Verified-anchor grounding for Grounded VideoQA

A method report for the Perception Test 2026 challenge, Task 2 (Grounded VideoQA), shown end to end
on a single question rather than as a diagram.

**Read it: https://neilyysun-ui.github.io/perception-test-task2-v26-report/**

Every image on the page is the actual bytes a pipeline stage consumed, taken from that stage's cache:
the 3 fps bank the event scan saw, the densely sampled event-window frames the disambiguation pass
saw, the original-resolution frames the grounder saw, and byte-for-byte copies of the crops sent to
the verifier. Every number is read from an artifact on disk by the generator, so the page cannot
drift from the run it describes.

`report.json` holds the same content as structured data.

## Headline

| | Test HOTA |
|---|---:|
| This method | **0.5063117** |
| Previous submission | 0.4743749 |
| 2025 winning entry (SGVR@KAIST) | 0.4968439 |

Measured on 688 held-out validation questions with the same tracker on both sides and only the
anchors changed: HOTA 0.473696 to 0.577942, DetA 0.465930 to 0.568405, AssA 0.489868 to 0.593310.

## Attribution

Video frames and annotations are from the [Perception Test](https://github.com/google-deepmind/perception_test)
benchmark (Google DeepMind), used under CC BY 4.0. The question shown is from the public validation
split, which carries published annotations; no test-split imagery appears in this repository. The
2025 comparison figure is the public EvalAI leaderboard for that year's Grounded VideoQA test phase.
