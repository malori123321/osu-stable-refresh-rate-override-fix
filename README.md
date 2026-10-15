# osu!stable Refresh Rate Override — Aim Consistency Experiment

A potential workaround for inconsistent aim feel in osu!stable, particularly during fullscreen jumps.

## The issue

On a 1920×1080, 144 Hz laptop display, Windows reported 144 Hz while the osu!stable configuration contained:

```ini
RefreshRate = 60
OverrideRefreshRate = 0
```

After manually setting:

```ini
RefreshRate = 144
OverrideRefreshRate = 1
```

the mouse appeared to retain the same sensitivity while feeling more consistent and controllable.

A second player independently reported a similar improvement, especially during fullscreen jumps.

## How to try it

1. Close osu!stable completely.
2. Back up your `osu!.*.cfg` file from the osu! installation folder.
3. Open the configuration file in a text editor.
4. Set `RefreshRate` to your monitor's actual refresh rate.
5. Set `OverrideRefreshRate = 1`.
6. Save the file and restart osu!.

Example for a 144 Hz monitor:

```ini
RefreshRate = 144
OverrideRefreshRate = 1
```

For a 240 Hz monitor, use `RefreshRate = 240` instead.

## Important notes

- This is an experimental configuration change, not a verified input-latency fix.
- The results reported so far are subjective.
- It does not change mouse DPI or osu! sensitivity.
- Your monitor must actually support the refresh rate you specify.
- Results may differ by GPU, driver, fullscreen mode and osu! version.

## Reverting

Close osu! and restore your backed-up configuration file, or change:

```ini
OverrideRefreshRate = 0
```

## Testing and feedback

If you try this, please report:

- Display refresh rate
- GPU and operating system
- osu!stable version
- Fullscreen or windowed mode
- Raw Input status
- Whether aim consistency changed
- Whether FPS or frametime behavior changed

This project is independent and is not affiliated with osu! or ppy.

## Privacy

Never upload your complete osu! configuration file. It may contain saved credentials or other personal information.

## Community Results

See [RESULTS.md](RESULTS.md) for preliminary findings.

Want to contribute? [Submit a test report](../../issues/new/choose).

Both positive and negative results are welcome.
