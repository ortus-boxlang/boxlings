# 🥊 BoxLings

[![Beta](https://img.shields.io/badge/status-beta-orange)](https://github.com/ortus-boxlang/boxlings)
[![BoxLang](https://img.shields.io/badge/BoxLang-1.11%2B-blue)](https://boxlang.ortusbooks.com/)
[![License](https://img.shields.io/badge/license-Apache2-green)](LICENSE)

![alt text](boxlings-banner.jpg)

> Small exercises to get you used to reading and writing **BoxLang** code while learning **Test-Driven Development (TDD)**!

Inspired by [rustlings](https://github.com/rust-lang/rustlings), **BoxLings** is an interactive CLI tool that guides you through learning BoxLang fundamentals through hands-on exercises with intentional errors. You fix the code, run tests, and progress through topics at your own pace.

**What makes BoxLings special?** We teach you **TDD/BDD** alongside BoxLang! Tests are visible and part of the learning experience. Read tests first to understand requirements, then fix code to make them pass.

---

## ✨ Features

- 🎯 **129 Progressive Exercises** across 28 topics
- 🧪 **TDD/BDD Learning** - Read and write TestBox tests
- 👀 **Watch Mode** - Auto-rerun on file changes
- 💡 **Hints System** - Get help when stuck
- 📊 **Progress Tracking** - Resume where you left off
- 🎨 **Beautiful CLI** - Colored output, progress bars
- 📝 **Three File Types** - Scripts (.bxs), Classes (.bx), Templates (.bxm)
- ✅ **Solutions Included** - Compare your code
- 🚀 **Built in BoxLang** - Dogfooding at its finest!

![alt text](boxlings-intro.png)

---

## 📋 Prerequisites

You'll need BoxLang installed on your system. If you don't have it yet:

- **BoxLang 1.12+** - [Installation Guide](https://boxlang.ortusbooks.com/getting-started/installation)
- **VScode** with our BoxLang Extension - As your IDE: https://boxlang.ortusbooks.com/getting-started/ide-tooling/boxlang-ide
- Terminal with ANSI color support (Windows users: Windows Terminal, Git Bash, or WSL recommended)
- Your favorite beverage ☕ for coding fuel!

We encourage you to use BVM ([BoxLang Version Manager](https://boxlang.ortusbooks.com/getting-started/installation/boxlang-version-manager-bvm)) to manage your BoxLang versions:

```bash
# Install BVM
curl -fsSL https://install-bvm.boxlang.io/ | bash
bvm install 1.12.0
bvm use 1.12.0
boxlang --version  # Verify BoxLang 1.12.0 is active
```

---

## 🚀 Quick Start

### 1. Clone the Repository

```bash
git clone https://github.com/ortus-boxlang/boxlings.git
cd boxlings
box install
```

### 2. Initialize Your Exercises

```bash
boxlang BoxLings.bx init
```

This creates your personal `exercises/` folder (git-ignored) from the templates stored in `src/exercises/`. You only need to run this once — or again if you want a completely fresh start.

### 3. Start Learning

```bash
boxlang BoxLings.bx
```

That's it! BoxLings will:

- Show you the first exercise
- Start **watch mode**
- Display the first exercise
- Auto-rerun when you save changes

---

## 🎮 How to Use

### Watch Mode (Default)

```bash
boxlang BoxLings.bx
```

Watch mode automatically:

- Shows current exercise
- Watches for file changes
- Reruns exercise on save
- Shows test results (if exercise has tests)

**Keyboard Shortcuts:**

- `n` - Next exercise (after completing current)
- `h` - Show hint
- `t` - Show test file
- `l` - List all exercises
- `r` - Manually rerun current exercise
- `c` - Clear terminal
- `q` - Quit

### Run Specific Exercise

```bash
boxlang BoxLings.bx run variables3
```

### Check All Exercises

```bash
boxlang BoxLings.bx check-all
```

### Reset an Exercise

Restores the exercise back to its **original broken state** (from the repository source):

```bash
boxlang BoxLings.bx reset variables3
```

### View the Solution

```bash
boxlang BoxLings.bx solution variables3
```

If you haven't solved the exercise yet, BoxLings will warn you and ask for confirmation before showing the answer.

### Show Hint

```bash
boxlang BoxLings.bx hint variables3
```

### Show Test File

```bash
boxlang BoxLings.bx show-test variables3
```

### List All Exercises

```bash
boxlang BoxLings.bx list
```

---

## � Troubleshooting

### "Command not found: boxlang"

**Solution:** BoxLang is not installed or not in your PATH.
- Verify installation: Check if BoxLang binary exists
- Add to PATH: Ensure BoxLang bin directory is in your system PATH
- Reinstall: Try [reinstalling BoxLang](https://boxlang.ortusbooks.com/getting-started/installation)

### "No exercises found" or "exercises/ folder is empty"

**Solution:** You need to run `init` first:
```bash
boxlang BoxLings.bx init
```

This creates your personal `exercises/` folder from the templates.

### Watch mode not detecting changes

**Possible causes:**
- **Network drives**: Watch mode may be slower on network/cloud synced folders
- **File permissions**: Ensure BoxLings can read the exercises directory
- **Manual rerun**: Press `r` to manually rerun the current exercise

### Colors not displaying correctly (Windows)

**Solution:** Enable ANSI color support:
- Windows 10+: ANSI is supported by default in newer terminals
- Use **Windows Terminal** for best experience
- Or try **Git Bash** or **WSL**

### TestBox errors or missing tests

**Solution:** Ensure TestBox is installed:
```bash
box install
```

This installs TestBox into the `testbox/` directory (required for exercises with tests).

### "Exercise already completed" but I want to redo it

**Solution:** Reset the exercise:
```bash
boxlang BoxLings.bx reset exercise-name
```

Or reset your entire progress:
```bash
rm -rf .boxlings exercises
boxlang BoxLings.bx init
```

### Still stuck?

- 📖 Check [BoxLang Documentation](https://boxlang.ortusbooks.com/)
- 💬 Ask on [Community Forum](https://community.ortussolutions.com/c/boxlang/42)
- 💭 Join [BoxLang Slack](https://boxteam.ortussolutions.com/)
- 🐛 [Open an issue](https://github.com/ortus-boxlang/boxlings/issues)

---

## �📚 Learning Path

### Phase 1: Core Fundamentals (50 exercises)

Perfect for beginners and those new to BoxLang:

1. **Introduction** (2) - Get started
2. **Variables** (6) - Dynamic typing, var keyword
3. **Functions** (6) - UDFs, closures, lambdas
4. **Conditionals** (4) - if/else, ternary, switch
5. **Data Types** (8) - Strings, numbers, booleans, arrays, structs
6. **Arrays** (4) - Array operations and member functions
7. **Scopes** (5) - variables, local, this, arguments
8. **Structs** (5) - Struct manipulation
9. **Strings** (6) - Interpolation, multi-line, operations
10. **Imports** (4) - Import classes, java: prefix

### Phase 2: Intermediate (40 exercises)

Dive deeper into BoxLang:

11. **Structs Advanced** (4) - Deep operations, merging
12. **Null Handling** (4) - Elvis operator, safe navigation
13. **Error Handling** (6) - try/catch, throw, exceptions
14. **Interfaces** (4) - Implementing Java interfaces
15. **Testing** (5) - **Write your own tests!**
16. **Functional** (8) - map, filter, reduce, lambdas
17. **Async** (6) - Threads, futures, async programming
18. **Components** (3) - bx:http, bx:query, etc.

### Phase 3: Advanced (48 exercises)

Master BoxLang-specific features:

19. **Casting** (5) - castAs, javaCast, conversions
20. **Quizzes** (3) - Comprehensive reviews
21. **Classes** (8) - OOP, properties, metadata
22. **BIFs** (6) - Built-in functions, member functions
23. **Templating** (4) - .bxm files, template syntax
24. **CLI Apps** (4) - Building CLI tools
25. **Java Interop** (6) - Calling Java, java: prefix
26. **Destructuring** (4) - Struct and array destructuring, renaming, nesting
27. **Spread** (4) - Spread operator for arrays, structs, and function calls
28. **Range** (2) - The `..` range operator and functional methods on ranges
29. **Assert** (2) - The `assert` statement with custom messages

---

## 🧪 TDD/BDD Learning Journey

BoxLings teaches you test-driven development alongside BoxLang:

### Step 1: Reading Tests (Topics 1-10)

**You learn to:**

- Read TestBox specs
- Understand `describe()` and `it()` blocks
- Interpret expectations: `expect().toBe()`, `expect().toInclude()`
- Use tests as documentation

**Example:**

```javascript
// Read this test FIRST
class extends="testbox.system.BaseSpec" {
    function run() {
        describe( "Variables Exercise 3", () => {
            it( "should calculate sum correctly", () => {
                // Your code should set x=10, y=20, sum=30
                expect( sum ).toBe( 30 );
            });
        });
    }
}
```

### Step 2: Understanding Patterns (Topics 11-14)

**You see:**

- Multiple assertions
- Setup/teardown (`beforeEach`, `afterEach`)
- Edge cases and error handling
- Complex test scenarios

### Step 3: Writing Tests (Topic 14: Testing)

**Now YOU write tests!**

- Practice `describe` / `it` / `expect` syntax
- Learn to think tests-first
- Write your own TestBox specs

### Step 4: TDD Practice (Topics 15-25)

**Apply full TDD cycle:**

- Write test (RED)
- Write code to pass (GREEN)
- Refactor (REFACTOR)

---

## 📂 Project Structure

**After running `boxlang BoxLings.bx init`, you'll see:**

```
boxlings/
├── BoxLings.bx              # Main CLI entry point
├── box.json                 # Package descriptor
├── info.json                # Exercise metadata (single source of truth)
├── src/                     # BoxLings source code
│   ├── AppState.bx
│   ├── Exercise.bx
│   ├── InfoFile.bx
│   ├── Runner.bx
│   ├── Terminal.bx
│   ├── Watcher.bx
│   ├── exercises/          # Exercise templates (for contributors)
│   └── solutions/          # Working solutions (for reference)
├── exercises/               # Your personal workspace (git-ignored!)
│   ├── 00_intro/
│   │   ├── intro1.bxs      # Fix these files!
│   │   └── intro2.bxs
│   ├── 01_variables/
│   │   ├── variables3.bxs
│   │   └── variables3Test.bx   # Test files (read these!)
│   └── ...
├── testbox/                 # TestBox framework
└── .boxlings/              # Your progress (auto-created)
    └── state.json          # Progress tracking
```

**Note:** The `exercises/` folder is created from `src/exercises/` templates when you run `init`. Your changes are saved here and won't be tracked by git!

---

## 🎓 Exercise Format

### Exercises WITHOUT Tests

Simple syntax fixes - compilation is the check:

```javascript
// exercises/01_variables/variables1.bxs
// TODO: Add the missing keyword
function main() {
    x = 5;  // <-- Fix this!
    println( "x = #x#" );
}
```

### Exercises WITH Tests

**Read the test FIRST:**

```javascript
// exercises/01_variables/variables3Test.bx
class extends="testbox.system.BaseSpec" {
    function run() {
        describe( "Variables Exercise 3", () => {
            it( "should initialize x with value 10", () => {
                include "variables3.bxs";
                expect( variables.x ).toBe( 10 );
            });
        });
    }
}
```

**Then fix the exercise:**

```javascript
// exercises/01_variables/variables3.bxs
// TODO: Read variables3Test.bx first!
// TODO: Initialize x with the value 10

// Fix this
x = ???

println( "x = #x#" );
```

---

## 🛠️ Development

Want to improve BoxLings or add new exercises? Here's how to get started.

### Install TestBox (For BoxLings Core Development)

```bash
box install
```

### Run BoxLings Tests

```bash
box run-script test
```

Or directly:

```bash
box testbox run
```

### Adding New Exercises

**Important:** Add exercises to `src/exercises/` and `src/solutions/`, NOT the user's `exercises/` folder!

1. **Create exercise file**: `src/exercises/{topic}/{name}.bxs`
2. **Create test file** (if applicable): `src/exercises/{topic}/{name}Test.bx`
3. **Add to info.json**: Insert new entry in correct order
4. **Create solution**: `src/solutions/{topic}/{name}.bxs`
5. **Test it**:
   ```bash
   # Initialize fresh exercises
   boxlang BoxLings.bx init
   # Test your exercise
   boxlang BoxLings.bx run {name}
   ```

### Directory Structure for Contributors

```
src/
├── exercises/        # Template exercises (source of truth)
├── solutions/        # Working solutions (for reference)
└── AppState.bx       # Core BoxLings code

exercises/           # User workspace (git-ignored, created by init)
```

---

## 🤝 Contributing

We **love** contributions! BoxLings is a community project and we welcome:

- 🐛 Bug fixes
- ✨ New exercises
- 📚 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Test improvements

### Quick Contribution Guide

1. **Fork the repository**
2. **Create a feature branch**: `git checkout -b feature/my-improvement`
3. **Make your changes**
4. **Test thoroughly**: `box test` (for BoxLings core) or test exercises manually
5. **Commit with clear messages**: `git commit -m "Add: New async exercise for futures"`
6. **Push and create PR**: `git push origin feature/my-improvement`

### Adding New Exercises

See our [Exercise Creation Guide](docs/CREATING_EXERCISES.md) for detailed instructions.

**Quick steps:**

1. Create exercise file in `src/exercises/{topic}/{name}.bxs`
2. Add test file (if applicable): `src/exercises/{topic}/{name}Test.bx`
3. Add entry to `info.json` in the correct order
4. Create solution in `src/solutions/{topic}/{name}.bxs`
5. Test the exercise: `boxlang BoxLings.bx run {name}`

### Code Style

- BoxLang: Follow [BoxLang Style Guide](https://boxlang.ortusbooks.com/programming-guide/style-guide)
- Clear comments and hints in exercises
- Progressive difficulty (each exercise slightly harder than previous)

For detailed contributing guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📖 Resources

- **BoxLang Documentation**: https://boxlang.ortusbooks.com/
- **TestBox Documentation**: https://testbox.ortusbooks.com/
- **BoxLang CLI Guide**: https://boxlang.ortusbooks.com/getting-started/running-boxlang/cli-scripting
- **BoxLang GitHub**: https://github.com/ortus-boxlang/boxlang
- **Rustlings** (inspiration): https://github.com/rust-lang/rustlings

---

## 📝 License

Apache 2 License - see [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Rustlings** - The original inspiration for this project
- **Ortus Solutions** - For creating BoxLang
- **BoxLang Community** - For feedback and contributions

---

## ❓ FAQ

### Do I need to know CFML to use BoxLings?

**No!** BoxLings teaches BoxLang from scratch. While BoxLang has CFML compatibility, these exercises focus on modern BoxLang syntax. Prior programming experience in any language is helpful but not required.

### How long does it take to complete all exercises?

**Varies by experience:**
- Beginners: 15-20 hours
- Experienced programmers new to BoxLang: 6-10 hours
- CFML developers: 4-6 hours

You can take breaks anytime - progress is automatically saved!

### Can I skip exercises?

Yes! While we recommend doing them in order, you can run any exercise directly:
```bash
boxlang BoxLings.bx run exercise-name
```

### What's the difference between .bxs, .bx, and .bxm files?

- **`.bxs`** - Scripts (most exercises): Execute directly, no class wrapper needed
- **`.bx`** - Classes: BoxLang class files with `class { }` wrapper
- **`.bxm`** - Templates: For HTML/template mixing exercises

### Are solutions available?

Yes! Use `boxlang BoxLings.bx solution exercise-name`. BoxLings will warn you if you haven't attempted the exercise yet, but you can still view it if needed.

### Can I use BoxLings offline?

Yes! Once cloned, BoxLings runs completely offline. Only the initial clone and any future updates require internet.

### How do I update BoxLings?

```bash
cd boxlings
git pull origin main
boxlang BoxLings.bx init  # Refresh exercises with new content
```

Your progress in `.boxlings/state.json` is preserved!

### Is BoxLings suitable for teaching/workshops?

Absolutely! BoxLings is designed for self-paced learning, classrooms, workshops, and bootcamps. The progressive structure and built-in hints make it ideal for learning environments.

### Can I contribute my own exercises?

Yes! We welcome contributions. See the [Contributing](#-contributing) section for details.

---

## 💬 Community & Support

- **Community Forum**: https://community.ortussolutions.com/c/boxlang/42
- **Slack**: https://boxteam.ortussolutions.com/
- **Issues**: https://github.com/ortus-boxlang/boxlings/issues

---

## 🎯 Goals

BoxLings aims to:

- ✅ Make learning BoxLang fun and interactive
- ✅ Teach TDD/BDD as a core skill (not an afterthought!)
- ✅ Provide immediate feedback and guidance
- ✅ Build confidence through progressive difficulty
- ✅ Create a supportive community of BoxLang learners
- 🔄 Continuously improve based on community feedback (we're in beta!)

---

**Ready to start learning? 🚀**

```bash
git clone https://github.com/ortus-boxlang/boxlings.git
cd boxlings
boxlang BoxLings.bx init
boxlang BoxLings.bx
```

**Found a bug or have feedback?** [Open an issue](https://github.com/ortus-boxlang/boxlings/issues) or join us on [Slack](https://boxteam.ortussolutions.com/)!

---

**Made with ❤️ by the BoxLang Community**
