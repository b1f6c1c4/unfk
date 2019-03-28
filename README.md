# unfk

> Remove all `f**k`s in your git commit history

## Usage

```sh
unfk                      # Check if index is f**k'd
unfk -f -t emmm           # Replace all f**ks with emmm in index
unfk -f -- -- 1.txt       # Fix 1.txt only
unfk --install            # Run unfk before every commit
unfk HEAD                 # Check if HEAD is f**k'd
unfk -f HEAD              # Fix HEAD
unfk -f -- master         # Fix the whole history from master
unfk -f -- HEAD ^HEAD~10  # Fix 10 commits from HEAD
unfk -f -- --all -- 1.txt # Fix the whole repo, 1.txt only
```

## Exit status

- If `-n` is specified:
    - Return value `0` indicates no `f**k` is found;
    - Return value `1` indicates some `f**k`s are found;
    - Return value `2` indicates error.
- If `-f` is specified:
    - Return value `0` indicates all `f**k`s are fixed (if any);
    - Return value `1` indicates some `f**k`s are found but can't be fixed;
    - Return value `2` indicates error.

## License

MIT
