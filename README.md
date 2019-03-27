# unfk

> Remove all `f**k`s in your git commit history

## Usage

```sh
unfk                      # Check if index is f**k'd
unfk -f -t emmm           # Repace all f**ks with emmm in index
unfk HEAD                 # Check if HEAD is f**k'd
unfk -f HEAD              # Fix HEAD
unfk -f --depth inf HEAD  # Fix the whole history from HEAD
unfk -f --depth 10 master # Fix 10 commits from master
unfk -f --depth inf --all # Fix the whole repo
unfk --install            # Run unfk before every commit
```

- If `-n` is specified:
    - Return value `0` indicates no `f**k` is found;
    - Return value `1` indicates some `f**k`s are found;
    - Return value `2` indicates error.
- If `-f` is specified:
    - Return value `0` indicates all `f**k`s are fixed (if any);
    - Return value `2` indicates error.
