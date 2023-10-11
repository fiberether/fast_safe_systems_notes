
## Rustup and Cargo
---

* rustup - tool for managing Rust installations
* `rustup update` - update Rust in one key tap

###### After installation there are 3 commands available
1) `cargo --version`
	* package manager, compilation manager, general-purpose tool
	* create project, build, add external packages & dependencies
1) `rustc --version`
	* Rust's compiler
	
1) `rustdoc --version`
	* can create nice documentation from comments for your package


#### Cargo
* Create package and initialize empty GIT repo:
	* `cargo new hello`
	* `cargo new --vcs none project` - initalize without REPOSITORY
	* `cargo run` - build (if not yet) and run app
	* cargo clean - clean build artifacts
* ```Cargo.toml``` - holds metadata for the package
	```toml
	[package]
	name = "hello"
	version = "0.1.0"
	authors = ["Me me@example.com"]
	edition = "2018"

	[dependencies]
```

* Cargo creates new directory named
	* ```target``` - that contains build artifacts
	* inside of which there are
		* release  - for release version
		* debug - ....

#### Code style

* RUST ALWAYS CHECKS ASSERTIONS except for `debug_assert!` - theese assertions are skipped when building for RELEASE
  * RUST ONLY INFERES Types inside of functions
  * Any block surrounded with CURLY braces can function like EXPRESSION

### Docs
```bash
rustup doc --std

```

