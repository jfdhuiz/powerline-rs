# powerline-rs

`powerline-rs` is a rewrite of [powerline-shell](https://github.com/b-ryan/powerline-shell), inspired by [powerline-go](https://github.com/justjanne/powerline-go).

## Why?

Speed! I would argue that even the debug version of `powerline-rs` at least feels faster than `powerline-go`.
The Rust language is perfect for fast applications, since copying large objects isn't implicit.

### What's new?

Well, the default modules have changed to not include the username and hostname.
I feel like most people already know that.
But you can always enable it, of course!

### What's optimized?

 - Generally just using Rust.
 - Using `libgit2` over calling and parsing `git` output (Thanks [tbodt](https://github.com/tbodt) for suggesting it!)
 - `libgit2` can be disabled at compile time if you don't plan on using git functionality.
 - Themes are using a simple small `key=value` scripts. No JSON overhead or similar.
 - The output of `powerline-rs` is slightly smaller than the 2 alternatives I mentioned. To be honest, I have no idea why.

### What's removed?

Most of the service-specific modules are deleted. I am very lazy.  
Pull requests are welcome, though.

Also, the `jobs` module won't work with `--shell bare`.