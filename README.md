# First Rust Project

Let’s add a dependency to our application. You can find all sorts of libraries on crates.io, the package registry for Rust. In Rust, we often refer to packages as “crates.”

In this project, we’ll use a crate called ferris-says.

In our Cargo.toml file we’ll add this information (that we got from the crate page):

```rust
[dependencies]
ferris-says = "0.2"
```

Now we can run:

`cargo build`

...and Cargo will install our dependency for us.

You’ll see that running this command created a new file for us, **Cargo.lock**. This file is a log of the exact versions of the dependencies we are using locally.

To use this dependency, we can open **main.rs**, remove everything that’s in there (it’s just another example), and add this line to it:

```rust
use ferris_says::say;
```

This line means that we can now use the **say** function that the **ferris-says** crate exports for us.