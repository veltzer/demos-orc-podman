# TOFIX

Findings from a code scan on 2026-10-04.

## High

- `README.md:2` - the README promises "Demos for the podman container technology" but the repo contains no demos at all (only README, config/project.lua and the shared fleet files). Either add the podman demos (e.g. a `demos/` or `scripts/` folder with run/build/pod/rootless examples, wired into `rsconstruct.toml` with shellcheck) or reduce the description in `config/project.lua:3` and the README to say it is a placeholder.

## Low

- `config/project.lua:1` - the Lua config is not linted: there is no `.luacheckrc` and no `[processor.luacheck]` in `rsconstruct.toml`, unlike most of the fleet (e.g. pypluggy). Add the fleet `.luacheckrc` and `[processor.luacheck]` with `src_dirs = ["config"]`.
