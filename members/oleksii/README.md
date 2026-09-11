# Member record — how to instantiate

Copy this whole folder to `members/<name>/` to start a new family member's pipeline:

    cp -R _templates/member/. members/<name>/

Then fill stage outputs in order (`01_profile` → … → `05_longterm`). A member is a *stub* until
`01_profile/output/` holds files other than `.gitkeep`.

Per-stage contracts in `stages/NN_*/CONTEXT.md`: each names its inputs, process, outputs and the
human check. The shared roster + rules live in `_shared/` — do not copy them per member.
Person-specific certificates/scans stay in the member's own output folders, never in `_shared/`.