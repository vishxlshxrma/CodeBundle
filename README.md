# **CodeBundle 📦✨**

### *Bundle your entire codebase into a clean, single text file — perfect for AI tools, analysis, and sharing.*

CodeBundle is a lightweight, blazing-fast CLI tool designed to combine all files from a directory into a single, structured `.txt` file.
Ideal for feeding codebases to LLMs (ChatGPT, Claude, Gemini), performing code reviews, documentation prep, or simply exporting project snapshots.

---

## 🚀 **Features**

* **📂 Directory-to-Text Export**
  Converts an entire folder (and subfolders) into a clean `.txt` output.

* **⚡ Fast Mode**
  Boosts performance by skipping ordering (useful for large repos).

* **🧠 Optimized for AI Tools**
  Clean output format makes it easy to give entire projects to LLMs.

* **🗂 Smart Structure Display**
  Shows a simple tree-like structure of files being bundled.

* **🎯 Zero Config, Instant Usage**
  Simple CLI interface with intuitive flags.

---

## 📦 **Installation**

You can install CodeBundle after adding Go to your system:

```
go install github.com/vishxlshxrma/CodeBundle@latest
```

This will create a `codebundle` binary in your Go bin directory.

---

## 🛠 **Running Locally (Without Install)**

Clone the repository:

```bash
git clone https://github.com/vishxlshxrma/CodeBundle.git
cd CodeBundle
```

Build & run manually:

```bash
go build -o bin/codebundle ./cmd/cli
./bin/codebundle --help
```

---

## 🧪 **Usage**

Basic usage:

```bash
codebundle --input ./my-folder --output project.txt
```

Enable fast mode:

```bash
codebundle --input ./src --output flat.txt --fast
```

### **Flags**

| Flag            | Description                                             |
| --------------- | ------------------------------------------------------- |
| `--input, -i`   | **(Required)** Path to the directory you want to bundle |
| `--output, -o`  | Output file path (default: `output.txt`)                |
| `--fast`        | Faster bundling but may skip ordering                   |
| `--help, -h`    | Show help menu                                          |
| `--version, -v` | Show version                                            |

---

## 📁 **Example Output Structure**

```
┌───────────────────────────────┐
│ 🕒 Collection Time: 0s        │
└───────────────────────────────┘
Source code files structure

├── src
│   ├── main.go
│   ├── utils.go
│   └── handlers
│       └── user.go
```

And the final `project.txt` will contain a clean, concatenated version of all your files.

---

## 🧩 **How It Works**

1. Walks through your directory recursively
2. Collects all readable files
3. Prints a structured tree representation
4. Bundles file contents into one `.txt`
5. (Optional) Uses fast mode to skip ordering

Simple, predictable, and perfect for code export workflows.

---

## 🤝 **Contributing**

Contributions are welcome!
Feel free to open an issue or submit a PR at:

👉 **[https://github.com/vishxlshxrma/CodeBundle.git](https://github.com/vishxlshxrma/CodeBundle.git)**

---