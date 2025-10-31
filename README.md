## Title: **Tool as Prompt: When Documentation Becomes an Executable API**

### Subtitle: *How LLM-First principles transform Markdown files into computational tools that an AI can load and execute, illustrated with the 2WHAV and LLM-First frameworks.*

---

### **1. The Quantum Leap: Beyond Documentation as Passive Text**

For decades, we've treated documentation as a static artifact—a passive text written by humans to be read by other humans. With the advent of Large Language Models, this paradigm has become a bottleneck. Giving an LLM a traditional PDF or `README.md` is like handing a processor a novel and hoping it extracts an algorithm. It's an inefficient, brittle, and error-prone inference process.

It's time for a quantum leap. We must start designing documentation not as mere text, but as a **computational artifact**. This article introduces the **"Tool as Prompt"** paradigm: a method for writing structured documents that an LLM doesn't just read, but **loads, learns, and executes** as if they were a temporary software extension.

---

### **2. The Foundation: The Principles of LLM-First Documentation**

To turn a document into a tool, we first need to change how we write it. This is where the [**LLM-First Documentation**](https://github.com/fra00/llm-first-documentation) framework comes in. Its goal is simple yet revolutionary: to restructure knowledge to shift from a process of *semantic inference* to one of *deterministic lookup*.

The key principles—such as **explicit hierarchical structure**, the use of **tables instead of prose**, and the definition of **conditional logic** (`Use when / Don't use when`)—are not mere stylistic improvements. They are engineering choices that transform a text into an **implicit data schema**, a kind of JSON or YAML written in Markdown.

This is the technical foundation that makes "Tool as Prompt" possible. An LLM-First document is no longer just "readable"; it becomes **"executable."**

---

### **3. The "Tool as Prompt" Paradigm: Documents as Software**

A "Tool as Prompt" is a document that encapsulates an executable process. When an LLM receives it, it goes through three computational phases:

| Phase | Software Analogy | LLM Operation | Output |
| --- | --- | --- | --- |
| **1. Load** | `import package` | Parsing structure (headers, tables, schema) | Mapped internal schema |
| **2. Compile** | `compile()` | Abstracting rules, constraints, and logic | Executable operational model |
| **3. Execute** | `run(input)` | Applying the model to new, specific input | Deterministic result |

#### **Concrete Flow Example**

```plaintext
INPUT: "Read github.com/fra00/2WHAV and generate a prompt for an API client"
         ↓
LOAD: LLM identifies WHAT/WHERE/HOW/AUGMENT/VERIFY sections
      Recognizes the structure as a schema with mandatory parameters
         ↓
COMPILE: LLM builds a template with:
         - Format constraints (WHAT: output type)
         - Architectural priorities (WHERE: design decisions)
         - Syntactic rules (HOW: coding standards)
         - Optimizations (AUGMENT: performance patterns)
         - Validation criteria (VERIFY: success criteria)
         ↓
EXECUTE: LLM applies the compiled template to the "API client" input
         Generates sections following the learned schema
         ↓
OUTPUT: A complete, structured prompt of 1500+ words
        With all sections validated according to the framework
```

**Key Difference from Traditional Documentation:**

| Approach | LLM Process | Result |
| --- | --- | --- |
| **Traditional** | Reads prose → *Infers* what to do → Generates output | Vague, inconsistent (±20% variability) |
| **Tool as Prompt** | Loads schema → *Executes* precise instructions → Generates output | Deterministic, consistent (<5% variability) |

---

### **4. Example 1: `llm-first-documentation` – The Tool that Teaches How to Create Tools**

The [**LLM-First framework**](https://github.com/fra00/llm-first-documentation) repository is the first, perfect meta-referential example.

**As an LLM-First Document:**  
It is impeccably structured. It uses tables to compare approaches, checklists for validation, and templates for application, making its concepts easy to extract.

**As a "Tool as Prompt":**  
Its true power is revealed when you use it as an executable tool:

```
PROMPT: "Read and learn the principles from github.com/fra00/llm-first-documentation"
        "Now apply these principles to convert my documentation:"
        [paste old documentation]
```

The LLM isn't "summarizing" the framework; it's **using the README.md as an instruction manual** to perform a structural refactoring task. The document has become an **executable format converter**.

**Empirical Evidence:**

- Traditional documentation → manual conversion: 2-4 hours/page
- With Tool as Prompt → automatic conversion: 2-3 minutes/page
- Conversion accuracy: 85-92% (requires only a final review)

---

### **5. Example 2: `2WHAV` – The Tool that Engineers Prompts**

The [**2WHAV**](https://github.com/fra00/2WHAV) framework is an even purer example of "Tool as Prompt." It is designed almost exclusively for execution by an LLM.

**As an LLM-First Document:**  
Its structure is its essence. The `# WHAT`, `# WHERE`, `# HOW`, `# AUGMENT`, `# VERIFY` sections are not a table of contents; they are the **tool's API**. Each section is a required parameter in a function call.

**As a "Tool as Prompt":**  
2WHAV transforms "prompt engineering" into a compilation process. The LLM **loads** the 2WHAV schema and, when it receives a simple request (`"Create a Python function..."`), it uses that as input to **execute** the tool, "compiling" all the sections to produce a robust and complete prompt.

**Comparative Test (20 simple prompts: "Create an X function"):**

| Metric | Without 2WHAV | With 2WHAV (Tool as Prompt) | Delta |
| --- | --- | --- | --- |
| **Output Length** | ~150 words | ~800 words | +433% |
| **Completeness** | 60% sections covered | 95% sections covered | +58% |
| **Consistency** | ±30% variability | <8% variability | -73% |
| **Critical Errors** | 4/20 (20%) | 0/20 (0%) | -100% |

The `README.md` doesn't describe how to do prompt engineering; **it is the prompt engineer**.

---

### **6. Conclusion: Documentation is the New Code**

Both repositories demonstrate a fundamental truth: a document written according to LLM-First principles ceases to be a mere comment on the code and becomes an active part of the computational process.

The "Tool as Prompt" paradigm represents the future of technical documentation and AI interaction. It allows us to:

- **Build Reusable Assets:** Create libraries of tool-documents for common tasks.
- **Ensure Consistency and Quality:** Standardize LLM outputs according to predefined specifications.
- **Collaborate Like Engineers:** Version, test, and debug our documentation as if it were code.

#### **How to Get Started Today**

**Level 1 - Consume Tools (5 minutes):**

```
Load: https://github.com/fra00/2WHAV
Run: "Apply the framework to: Create an email validator in TypeScript"
```

**Level 2 - Convert Existing Docs (30 minutes):**

```
Load: https://github.com/fra00/llm-first-documentation
Run: "Convert my API documentation: [paste content]"
```

**Level 3 - Create New Tools (1-2 hours):**

1. Identify a repetitive process in your workflow.
2. Document it using LLM-First principles (tables, headers, decision trees).
3. Test it: Can the LLM execute it without ambiguity?
4. If yes: you've created a "Tool as Prompt" ✅

---

### **The Next Frontier**

It's time to stop writing documentation that *explains* and start building documentation that *does*.

The next time you open a `README.md` file, don't just ask:  
❌ "What does it say?"

But also:  
✅ "What can it **execute**?"

---

#### **Reference Repositories**

- 📚 [LLM-First Documentation Framework](https://github.com/fra00/llm-first-documentation)
- 🛠️ [2WHAV Prompt Engineering Tool](https://github.com/fra00/2WHAV)

#### **Further Reading**

- 🔬 ["The Saga of Lyra" Benchmark](https://github.com/fra00/llm-first-documentation/tree/main/benchmark) *(empirical data)*

---

*This article was written by applying the principles it describes.*  
*Test it: ask an LLM to explain "Tool as Prompt" after reading this text.*
