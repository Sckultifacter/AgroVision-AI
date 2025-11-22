This folder contains consolidated requirement files for the workspace.

Files:
- `combined-requirements.txt` - a best-effort aggregation of all `requirements.txt` found in the workspace.
- `*-requirements.txt` - per-subproject requirements copied from their original files for traceability.

Conflict resolution rules used:
- If one project pins an exact version (==), that exact version is chosen where compatible.
- Otherwise the highest minimum (`>=`) was preferred.
- Comments and duplicate entries were removed.

How to install the combined environment (Windows cmd):

    cd "C:\Users\nandi\Desktop\MINI_PROJECT"
    pip install -r requirements\combined-requirements.txt

Notes:
- The combined file includes heavy ML packages (e.g. `torch`) which may require specific platform wheels and substantial disk space.
- If you only need a subproject, install from its per-project file instead, e.g.:

    pip install -r requirements\leaf-requirements.txt

If you want different conflict-resolution (e.g., prefer latest versions or full pinning), tell me and I will regenerate the combined file accordingly.
