# unfk

> Remove all `f**k`s in your git commit history

Note: you can use `unfk -e <your_password_here>` to check if the index contains your password, and use `-f` to remove it.

## Usage

```sh
unfk                      # Check if index is f**k'd
unfk -f -e 114 -t 514     # Replace all 114 with 514 in index
unfk -f -- 1.txt          # Fix 1.txt only
unfk --install            # Run unfk before every commit
```

## Install

We recommand you to install it using [Git-Get](https://github.com/b1f6c1c4/git-get).

Locally: `~/.local/bin/unfk`
```sh
git get b1f6c1c4/unfk -f -o ~/.local/bin/unfk -- unfk
# Or, without git-get:
curl -fSSL https://raw.githubusercontent.com/b1f6c1c4/unfk/master/unfk > ~/.local/bin/unfk && chmod +x ~/.local/bin/unfk
```

Globally (with sudo): `/usr/bin/unfk`
```sh
git get b1f6c1c4/unfk -f -o- -- unfk | sudo tee /usr/bin/unfk && sudo chmod +x /usr/bin/unfk
# Or, without git-get:
curl -fSSL https://raw.githubusercontent.com/b1f6c1c4/unfk/master/unfk | sudo tee /usr/bin/unfk >/dev/null && sudo chmod +x /usr/bin/unfk
```

## Exit status

- If `-f` is specified:
    - Return value `0` indicates all `f**k`s are fixed (if any);
    - Return value `1` indicates some `f**k`s are found but can't be fixed;
    - Return value `2` indicates error.
- If `-n` is specified, or neither `-f` nor `-n` is specified:
    - Return value `0` indicates no `f**k` is found;
    - Return value `1` indicates some `f**k`s are found;
    - Return value `2` indicates error.

## License

MIT
