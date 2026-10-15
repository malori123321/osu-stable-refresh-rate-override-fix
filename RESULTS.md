# Community Test Results

This document tracks community feedback on the osu!stable refresh rate override experiment.

## Preliminary Results

| Test | Refresh Rate | Hardware | Reported Result | Evidence |
|---|---|---|---|---|
| 001 | 60 → 144 Hz configuration | RTX 3050 Laptop + Intel Iris Xe | Improved aim consistency | Subjective report |
| 002 | Not yet documented | Not yet documented | Improved fullscreen jump control | Second player's subjective report |

**Initial feedback:** 2 positive subjective reports, 0 negative reports recorded, and 0 unchanged reports recorded.

These are preliminary observations, not controlled experimental results. The second player's full settings have not yet been documented.

## What We Know

The first tester reported more controllable cursor movement after changing:

```ini
RefreshRate = 144
OverrideRefreshRate = 1
```

The tester described the cursor as maintaining the same movement speed while feeling more consistent.

A second player reported a similar improvement, particularly with fullscreen jumps.

## What We Have Not Verified

- Whether osu! was actually rendering at a different refresh rate before the change
- Whether input-to-display latency decreased
- Whether frame pacing changed
- Whether hit accuracy improved
- Whether the difference is reproducible in blinded A/B testing

## Recommended Testing Procedure

1. Back up the original osu!stable configuration.
2. Record the current monitor refresh rate and osu! settings.
3. Test with automatic refresh rate detection.
4. Test with the manual refresh rate override.
5. Keep sensitivity, Raw Input, fullscreen mode and frame limiter unchanged.
6. Use the same beatmaps and comparable testing conditions.
7. Repeat the comparison in reverse order.
8. Report improvements, regressions or no change.

## Submit Results

Open a test report through the repository's Issues section.

Positive, negative and unchanged results are equally valuable.

## Disclaimer

This is an unofficial community experiment. It is not a verified input-latency fix and is not affiliated with osu! or ppy.
