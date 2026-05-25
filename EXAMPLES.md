# Examples

One short worked example per skill, showing the kind of output each workflow produces.

---

## 1. Roadmap: learning Rust

**Prompt**: a roadmap for learning Rust, coming from a Python background.

**Sketch of the output**:

- **Prerequisites**: comfort with one language, basic command line, install `rustup` and `cargo`.
- **Foundation**: ownership, borrowing, and lifetimes; the type system; `Result` and `Option`; `match`. Practice: rewrite three small Python scripts as Rust binaries.
- **Intermediate**: traits and generics; error handling with `?`; iterators and closures; modules and crates. Practice: build a small CLI with `clap`.
- **Advanced**: lifetimes in depth; `async`/`await` and `tokio`; unsafe and FFI; macros. Practice: a concurrent file processor.
- **Mastery**: read the standard library source; contribute to a crate; write about a hard concept you struggled with.
- **Milestones**: first compiling CLI; first crate published to crates.io; first contribution merged.
- **Common pitfalls**: fighting the borrow checker instead of restructuring ownership; reaching for `clone()` to silence errors; skipping `Result` handling with `unwrap()`.

The value is the ordering: ownership before async, traits before macros, so each topic rests on the one before it.

---

## 2. Explain: closures

**Prompt**: explain closures.

**Sketch of the output**:

- **Simple idea**: a closure is a function that remembers the variables from where it was created, even after that scope has finished.
- **Problem it solves**: you want to package some behavior together with the data it needs, and pass it around as one thing.
- **Core principle**: the closure captures its surrounding variables by reference or by value; those captured variables outlive the scope that created them.
- **Example**: a `makeCounter()` that returns a function incrementing a private `count` each call, where `count` is not visible anywhere else.
- **Analogy**: a backpack the function carries. Wherever the function goes, the backpack of captured variables goes with it.
- **Gotcha**: capturing a loop variable by reference, then all closures see the final value. Capture by value, or bind a fresh variable per iteration.
- **Practice**: write a closure-based memoizer that caches results of an expensive function.

---

## 3. Practice: SQL joins

**Prompt**: practice exercises for SQL joins.

**Sketch of the output**:

- **Warm-up**: given `customers` and `orders`, list every customer with their order count using a `LEFT JOIN`. Expected: customers with zero orders still appear, count `0`.
- **Core practice**: list orders with the customer name and the assigned sales rep name, joining three tables. Then rewrite an implicit comma join as an explicit `INNER JOIN`.
- **Challenge**: find customers who have never placed an order, two ways, `LEFT JOIN ... WHERE o.id IS NULL` and `NOT EXISTS`. Discuss which the planner prefers.
- **Real-world**: build a monthly revenue-by-region report joining `orders`, `customers`, and `regions`, handling customers with no region.
- **Solutions**: each with the query, the result shape, and a note on the trap, for example why a `WHERE` clause on the right table silently turns a `LEFT JOIN` back into an inner join.

---

## 4. Cheatsheet: git

**Prompt**: a cheatsheet for git.

**Sketch of the output**:

- **Most common operations**: `status`, `add -p`, `commit`, `pull --rebase`, `push`, `switch -c`, `log --oneline --graph`, `stash`, `restore`, `reset`.
- **Syntax reference**: discard local changes to a file with `git restore <file>`; unstage with `git restore --staged <file>`; amend the last commit with `git commit --amend`.
- **Common patterns**: feature branch then PR; rebase onto updated main; interactive rebase to clean history before review.
- **Gotchas**: `reset --hard` discards working changes irreversibly; force-pushing a shared branch rewrites others' history; a detached `HEAD` after checking out a commit.
- **Quick examples**: undo the last commit but keep changes with `git reset --soft HEAD~1`; recover a deleted branch via `git reflog`.

The output is one scannable page, the kind you keep open in a second tab.

---

## 5. Compare: REST vs GraphQL

**Prompt**: compare REST and GraphQL for a new API.

**Sketch of the output**:

- **Overview**: REST exposes resources at URLs with HTTP verbs; GraphQL exposes one endpoint with a query language that lets the client specify exactly what it wants.

| Aspect | REST | GraphQL |
|---|---|---|
| Data fetching | Fixed per endpoint, often over- or under-fetches | Client selects fields, one request |
| Caching | HTTP caching works out of the box | Needs application-level caching |
| Learning curve | Lower, widely understood | Higher, schema and resolvers to learn |
| Tooling | Mature, universal | Strong, but heavier setup |

- **When to use REST**: simple resource model, caching matters, public API where consumers expect convention.
- **When to use GraphQL**: many clients with different data needs, deeply nested data, fast-moving frontends that should not wait on new endpoints.
- **Migration path**: GraphQL can wrap existing REST endpoints in resolvers, so adoption can be incremental rather than a rewrite.
- **Recommendation**: for a small first API with one client, REST is less to learn and less to operate; reach for GraphQL when the client count and data-shape variety grow.
