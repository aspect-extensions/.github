## 🤖 Aspect Extension Language

Hello, I’m **Marvin**, your friendly (and occasionally somber) build system robot.  
I help developers fill Bazel usability gaps with the **Aspect Extension Language (AXL).**

---

## Why This Exists

Bazel is fast, scalable, and battle-tested in the enterprise.  
But anyone who’s used it knows: some important workflows are… missing, awkward, or just not adapted to your organization.  
Coverage. Formatting. Linting. Test reporting. Documentation. Release automation.  

That’s where **AXL extensions** come in.  
They extend the build system in small, composable tasks that solve the *real* problems Bazel users run into every day.

---

## About the Language

AXL (Aspect Extension Language) is a **dialect of Starlark** — the same language Bazel itself uses.  
That means extensions are:
- 🔎 **Familiar**: if you’ve ever read a Bazel `BUILD` file or rule, AXL will be readable.  
- 🔒 **Safe and deterministic**: no hidden side effects, no unbounded execution — perfect for reproducible builds.  
- 🧩 **Composable**: tasks can interact with Bazel’s query & build APIs while staying lightweight and easy to share.  

By using Starlark under the hood, AXL makes it possible to write high-level workflow automation that still feels native to Bazel.
This is the Bazel equivalent of Buck2's https://buck2.build/docs/bxl/.

---

## Example Extensions

Some things that are possible using AXL:

- 🔍 **Impacted Targets** → drive [`bazel-diff`](https://github.com/Tinder/bazel-diff) to know exactly which targets are affected by your changes.  
- 📊 **Coverage** → a saner replacement for `bazel coverage`, with incremental coverage and CI-friendly LCOV output.  
- 🧹 **Format** → run multi-language formatters only on files you actually changed.  
- 🧪 **Test** → wrap `bazel test`, generate compact execlogs, publish artifacts for CI, and comment directly on your pull requests when tests fail.  
- 🏗️ **Build** → customize Bazel’s progress messages, support multiple BES backends, and stream execlogs in real time.  
- 🚚 **Delivery** → release or publish build outputs, optionally only if they’ve changed.  
- 🛠️ **Gazelle** → run Gazelle as a proper extension task, 
- 🧭 **Lint** → run linters as Bazel aspects, cacheable and review-friendly.  
- 📚 **Docgen** → build and package documentation targets across a repo without a target that "depends on the world".

---

## What You’ll Find Here

- 🧩 **Aspect-reviewed contrib plugins** — lightweight, discoverable, and each with its own maturity guidance.  
- 🧪 **Room to experiment** — not every extension is “enterprise stable.". Each plugin shows its maturity (e.g. `v0.x` or `EXPERIMENTAL` in the description).
- 🌱 **Community participation** — most plugins start inside a company; the best ones get shared here.

---

## First-Time Experience

We care about **fast time-to-value.**  
Every extension is:
- Easy to clone or install  
- Ready to run in minutes  
- Documented with a clear `README.md`  

If you try one and it doesn’t help you immediately, Marvin wants to hear about it.

---

## Get Involved

- 💡 Have an internal script or extension? Contribute it here!  
- 🤝 Share feedback — Marvin loves PRs, issues, and community discussions.  
