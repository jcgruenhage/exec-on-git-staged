# exec-on-git-staged

`exec-on-git-staged` is a script that takes in commands via stdin and executes them
in the staged version of the current git repo.
It's useful for running linters in pre-commit hooks,
that only concern themselves with the currently staged state,
not changes that haven't been added yet.

## Installation
Put exec-on-git-staged into your PATH.

## Usage
Let's assume you have a cargo based rust project and want to check
that the staged state is formatted correctly.
This would be a pre-commit file that accomplishes that:

```bash
#!/bin/bash
echo "cargo fmt -- --check" | exec-on-git-staged
```

## Contributing
Pull requests are welcome. For major changes,
please open an issue first to discuss what you would like to change.

## License
[GPL-3.0-or-later](https://spdx.org/licenses/GPL-3.0-or-later.html)
