# Baseline Pipeline Viewer

Static comparison of baseline hand-object reconstruction results across
EgoInfinity, VGGT-Omega, and Do-As-I-Do.

The viewer loads geometry and videos only as their table rows approach the
viewport. Drag a 3D view to rotate it, use the mouse wheel to zoom, and use the
timeline beneath each view to inspect individual frames.

## VGGT depth pointmaps in Viser

The static site cannot host Viser's Python/WebSocket server. Start its companion
viewer from the repository root, then open `http://localhost:8081`:

```bash
/data/yixuans/.venvs/baselines-site/bin/python \
  models/baselines/view_vggt_pointmaps.py
```

It discovers the shared caches under `runs_0710/depth_cache/vggt_new`, exposes
the same DexYCB and HO3D examples in a picker, and keeps exactly one RGB
pointmap in the Viser scene at a time. Use `--list` to print the available
examples or pass a unique example substring to choose the initial one.
