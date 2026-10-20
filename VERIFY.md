# VERIFY

Merge evidence for Nercari. Paste the real output of these commands in the PR body. When behavior changes, update this file in the same PR.

## Essential check

Org profile; the check confirms the published files exist.

```
python3 -c "import pathlib,sys; sys.exit(0 if all(pathlib.Path(f).is_file() for f in ['README.md', 'llms.txt']) else 1)"
python -m unittest tests.test_merge_gate -q
```
