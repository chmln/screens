# `enact`

`enact` will detect the proper resolution of your secondary monitor (if any) and automatically set it up as soon as you plug it in (or out).

It uses `xrandr` under the hood and works great with window managers like i3, bspwm, and others.

Use cases:
- a laptop and an abritrary secondary monitor (e.g. at work, home, etc.)
- a desktop with two monitors

## Install

Download the binary from [releases](https://github.com/chmln/enact) or install via cargo: `cargo install --git https://github.com/chmln/enact`

## Usage

Test it out then place this in your `.xinitrc`.

```sh
# Set up second monitor above laptop 
enact --pos top
```

Or to do the same, but also watch for changes and allow hotplugging

```sh
enact --pos top --watch &
```

## Comparison With Similar Tools

Pros:
- monitor hotplugging that actually works (never got this to work with autorandr or any other tool)
- no need to setup any "profiles" or configuration, it just works
- Single compiled binary, no dependencies on python or anything else apart from `xrandr`

Drawbacks:
- Supports up to two displays max (at least currently)
