# DataX.now — Agents Deployed and Shared as One HTML File

**Your browser is the runtime.**

[Ying LEE YouTube profile](https://www.youtube.com/@YingLEE) · [Open playlist on YouTube](https://www.youtube.com/playlist?list=PL3RLIfS0Rx-5ibBxEygyWjWVx2LmYmH-Q)

## Executive Summary

**Sharing agent code is not deploying a working environment.** A recipient still needs compatible language runtimes, dependencies, supporting files, and somewhere to execute them. Local installation transfers that work to the recipient; hosted execution transfers it to a platform team; building a separate application adds another delivery cycle. DataX.now targets this environment handoff: getting from an agent that works for its creator to one a colleague can actually use.

DataX.now is a **browser-native platform for building, deploying, sharing, and using agents**, starting with enterprise analytical workflows. Specialists build in Python, R, and JavaScript, then package and share their agent project as one HTML file using JupyterLite Briefcase. Opening the file imports its notebooks and supporting files into DataX.now with folder structure preserved, making the project available in an integrated, stateful browser runtime without a local language installation or a hosted notebook server per recipient.

**The file is both the shareable project and the deployment handoff; the browser supplies the execution environment.** Sharing moves the packaged project between people; deployment makes it available in DataX.now's runtime. This is not a claim that every runtime asset is embedded in the HTML or that a running session is serialized. Required assets must be downloaded on first use. Cached assets can reduce subsequent startup work, and the PWA supports local Python/R/JavaScript analysis offline once the necessary assets are available. Cloud model calls and remote connectors still need connectivity.

### Product overview

[![Watch the DataX.now overview](https://img.youtube.com/vi/HMedVMfOZrw/hqdefault.jpg)](https://www.youtube.com/watch?v=HMedVMfOZrw)

---

## Audience-Based Positioning

| Audience | Positioning | Meaning |
| ---------- | ------------- | --------- |
| Technical users | **Deploy the environment, not just the code** | Deliver a project into an integrated Python/R/JavaScript browser runtime through one HTML file |
| Buyers/business | **A working environment, not another setup guide** | Give colleagues usable analytical capability without a local language installation or hosted notebook runtime per user |
| Investors | **Agents Deployed and Shared as One HTML File.** | **Your browser is the runtime.** One-file deployment and sharing are the entry point to a creator-to-user agent platform |

Agents define the broader product ambition; enterprise analytical workflows define the initial market. Notebooks are an authoring surface, not the limit of the positioning. Cowork and Claude Code are comparison points, not DataX.now's category.

Across these audiences, three non-functional advantages lead the story:

1. **One-file deployment and sharing:** Share the packaged agent project as one HTML file; opening it is the handoff into a working browser environment, rather than asking each recipient to reconstruct the setup.
2. **Local polyglot execution:** Run Python, R, and JavaScript on the client, share state across languages, and keep analyzing offline after required assets are cached.
3. **Build and use in one workspace:** Let specialists define agents with code and colleagues invoke them without code.

---

## The Problem: An Agent That Works for Its Creator Is Not Yet Deployed

**The neglected deliverable is the environment.** Code and model instructions alone do not give a colleague the runtimes, libraries, file layout, tools, and execution context needed to do the work. DataX.now's initial customer hypothesis is that this handoff imposes material setup and support costs on specialist-to-colleague workflows.

1. **Local setup becomes recipient work.** A notebook or repository still leaves someone installing compatible runtimes and libraries, arranging supporting files, and diagnosing differences. Every new recipient can become another onboarding and support task.
2. **Hosted execution becomes a platform obligation.** Remote notebooks and sandboxes solve real setup problems, but introduce provisioning, capacity, access, updates, and ongoing compute operations. Customer-controlled hosting remains a valid alternative, not necessarily third-party data exposure.
3. **A separate application becomes another development project.** Turning a specialist's working analysis into a colleague-facing tool can require a new interface and deployment path before the underlying work is reused.
4. **Language silos multiply the handoff.** Separate Python, R, and JavaScript environments fragment execution context and require manual file or value transfers.
5. **Sensitive data adds review, not a shortcut around it.** Execution location and data paths matter; security, source access, model endpoints, and governance still need approval even when computation is local.

Coding agents and general agent platforms can create and execute workflows; hosted notebooks can provide managed environments. The question is not whether these products work, but **how much effort it takes to deliver a usable environment to the next colleague**. DataX.now must win that comparison for supported workloads.

- **Setup and delivery pain is a product hypothesis to measure**, not a survey-proven ranking of enterprise agent barriers. The supplied research supports broader concerns about security, integration, governance, and trust; it does not quantify environment-setup costs.
- A working environment needs live computational state across analysis steps; exporting a project does not preserve live variables, processes, or credentials.
- Success means less recipient setup and specialist support, not simply producing an HTML file. Unsupported packages, network dependencies, and enterprise controls remain real boundaries.

---

## The Product: One-File Deployment and Sharing for Browser Agents

**Build → Export one HTML file → Share → Open → Work.** DataX.now combines environment delivery, project sharing, a no-code agent work surface, and technical authoring, with enterprise analysis as its first use case:

| Capability | Description | Why It Matters for Agents |
| ------------ | ------------- | -------------------------- |
| **One-file deployment and sharing** | JupyterLite Briefcase packages notebooks and supporting files into one shareable HTML file; opening it imports the project into DataX.now with its folder structure intact | Creators share a packaged project; recipients enter an integrated browser runtime rather than reconstructing a local language stack |
| **Local-first execution** | WASM in browser or native local runtime executes code and eligible working data on the client | Reduces hosted-compute dependence and remote data-transfer exposure |
| **Installable, offline-capable** | After an offline download, the installed browser app runs Python, R, and JavaScript analysis without a network connection | Demonstrates that computation is genuinely local and keeps work going through network loss; model calls and remote connectors still need connectivity |
| **Persistent session** | Variables, outputs, context persist across cells | Enables true reasoning loops and iterative investigation |
| **Polyglot execution** | Python, R, JS/TypeScript environments with namespace sharing | Reuse supported values across languages without manual file exports; conversion and copying depend on type and runtime path |
| **Build-and-use workflow** | Specialists define agents with code; colleagues use them through a no-code interface | Removes a separate application-development and deployment cycle |
| **Composable model workflows** | Coordinate providers for judging, fallback, routing, or racing | Optimizes a task across quality, speed, cost, and resilience |
| **Notebook-native interaction** | Rich displays, Markdown routing, interactive widgets | Work is understandable and reviewable by accountable humans |

The underlying xeus-x architecture is a real routing kernel with dedicated Python, R, and JavaScript sub-kernels, coordinated shared state, staged optional-runtime startup, and browser-worker integration. This is deep runtime infrastructure, not an LLM wrapper around a notebook.

### Product walkthroughs

These clips demonstrate the agent-authoring, polyglot, local-execution, and interactive-workflow capabilities described above.

#### Agent authoring and model workflows

##### AI-Assisted Code Implementation in DataX.now

[![Watch AI-assisted code implementation](https://img.youtube.com/vi/ElgF6LLJTIQ/hqdefault.jpg)](https://www.youtube.com/watch?v=ElgF6LLJTIQ)

##### AI-Assisted Code Fixing in DataX.now

[![Watch AI-assisted code fixing](https://img.youtube.com/vi/ii7A-Nx7YbI/hqdefault.jpg)](https://www.youtube.com/watch?v=ii7A-Nx7YbI)

##### Using the OpenAI Python SDK in DataX.now

[![Watch the OpenAI Python SDK demo](https://img.youtube.com/vi/1EiOYrQTl8g/hqdefault.jpg)](https://www.youtube.com/watch?v=1EiOYrQTl8g)

#### Polyglot and local workflows

##### Python, R, and JavaScript in One DataX.now Session

[![Watch the Python, R, and JavaScript session demo](https://img.youtube.com/vi/JTSUgZ0Brkk/hqdefault.jpg)](https://www.youtube.com/watch?v=JTSUgZ0Brkk)

##### Python and JavaScript in One DataX.now Session

[![Watch the Python and JavaScript session demo](https://img.youtube.com/vi/7VX6mvNlMZo/hqdefault.jpg)](https://www.youtube.com/watch?v=7VX6mvNlMZo)

##### User-Approved Local File Access in DataX.now

[![Watch user-approved local file access](https://img.youtube.com/vi/0xnJgbqJZnc/hqdefault.jpg)](https://www.youtube.com/watch?v=0xnJgbqJZnc)

##### Offline Analysis with Cached Browser Assets | DataX.now

[![Watch offline analysis with cached browser assets](https://img.youtube.com/vi/lR9rQtYblc0/hqdefault.jpg)](https://www.youtube.com/watch?v=lR9rQtYblc0)

#### Interactive work and collaboration

##### Interactive UI for Data Workflows in DataX.now

[![Watch interactive UI workflows](https://img.youtube.com/vi/H6QtneFiyqo/hqdefault.jpg)](https://www.youtube.com/watch?v=H6QtneFiyqo)

##### 3D Gaussian Splatting with Spark.js in DataX.now

[![Watch 3D Gaussian Splatting with Spark.js](https://img.youtube.com/vi/ElL-AcFQY3s/hqdefault.jpg)](https://www.youtube.com/watch?v=ElL-AcFQY3s)

##### AI and People Collaborate in DataX.now

[![Watch AI and people collaborate](https://img.youtube.com/vi/h20ayRs65uI/hqdefault.jpg)](https://www.youtube.com/watch?v=h20ayRs65uI)

### What the Shared HTML File Delivers

The HTML file is the handoff into a working environment, not simply a source-code attachment or a rendered report. It carries the project; DataX.now supplies the integrated browser runtime. Import does not automatically execute notebook cells. The deployment does not embed every runtime binary, guarantee arbitrary package compatibility, or restore a live process snapshot.

No account is required for the public DataX.now workspace, though model providers and enterprise sources may require credentials. First use needs access to required runtime assets and any uncached dependencies; later runs can reuse cached assets. The PWA retains supported local execution offline once the necessary assets are cached, but cloud models, remote data, and external-file downloads require connectivity.

The economic claim is **no hosted notebook-compute service to provision for each recipient**, not zero operating cost. Static hosting, asset delivery, model usage, support, and enterprise integrations still have costs. Measure first-use and cached startup separately; caching is not a promise that every workload starts instantly.

### Illustrative First Workflow

A financial-services analyst defines a recurring variance-analysis agent using approved calculations and domain instructions, then exports and shares its project as one HTML file. A colleague opens the file, imports the project into DataX.now, supplies an authorized dataset, and uses the agent to produce calculations, tables, and charts. The analyst reviews exceptions and updates the reusable workflow.

This is a **proposed pilot scenario, not a customer deployment**. Compare it with the team's current notebook handoff or separate application: measure recipient setup steps, specialist support time, time to first successful colleague-run analysis, first-use versus cached startup, repeat use, and correctness against an agreed baseline. Begin with bounded, read-only analysis; do not imply production approval for regulated decisions.

### Client-Side Boundary

DataX.now relates to enterprise servers in much the same way a browser relates to websites. DataX.now owns client execution and interaction. Enterprise servers and data platforms remain responsible for authentication, authorization, source-system data access control, governance, and system-of-record policies. DataX.now can integrate with those systems but does not replace their controls.

DataX.now still needs to enforce the client controls relevant to its deployment, including model-context handling, package behavior, connector permissions, and local data lifecycle. Browser delivery does not bypass procurement or security review. Browser memory, package compatibility, device policy, and workload size constrain eligible computation; large, scheduled, GPU-heavy, or centrally governed jobs may remain on enterprise compute.

---

## Competitive Positioning

DataX.now competes for the enterprise data-agent work surface while remaining complementary to enterprise servers:

| Layer | Representative Products | Primary Job | Where DataX.now Fits |
| ------- | ------------------------ | ------------- | --------------------- |
| Horizontal Agent Workspace | Claude Cowork | General knowledge work through a no-code agent surface | Specializes the work surface for stateful, polyglot data analysis |
| Coding Agent | Claude Code, Cursor | Build software and compose technical workflows | Brings low-code creation and model composition into the data workspace |
| Enterprise Server | Data platforms, databases, identity systems | Govern identity, data, and access | Consumes authorized interfaces; does not replace server controls |
| Hosted Notebook/Sandbox | Cloud notebooks, remote sandboxes | Run code on remote infrastructure | Moves eligible interactive execution to the client |
| **Browser Agent Environment** | **DataX.now** | **Build, deploy, share, and use agents through one-file delivery into an integrated runtime** | **Reduces the environment handoff from specialist to colleague** |

A coding agent might generate a query, model prediction, or transformation. The enterprise server determines which data a user may access. DataX.now provides the client environment where authorized data can be analyzed, intermediate results persist, and rich visualizations are displayed.

### Comparison point: Claude Cowork

This clip illustrates the horizontal agent-workspace category; it is a comparison point, not a DataX.now product demo.

[![Watch the Claude Cowork comparison](https://img.youtube.com/vi/g82WQf6qNfU/hqdefault.jpg)](https://www.youtube.com/watch?v=g82WQf6qNfU)

---

## FAQ

### What is the product category?

It is a **browser-native platform for building, deploying, sharing, and using agents**. The investor positioning is **Agents Deployed and Shared as One HTML File. Your browser is the runtime.** For creators, it makes the project shareable and delivers it into a runtime, not just as code; for recipients, it provides a working environment rather than another setup guide. Enterprise analysis defines the initial market, not the limit of the agent category.

### Is the whole runtime inside the HTML file?

No. The HTML is the deployment handoff into DataX.now's browser runtime. It carries the project and imports notebooks and supporting files with folder structure preserved. Required runtime assets and supported dependencies must be available or downloaded; cached assets enable supported offline local execution. It is not a standalone runtime binary or a snapshot of live variables, processes, or credentials, and importing does not automatically execute code.

### Why can't Claude Cowork, Claude Code, or a cloud notebook add this?

They can reproduce individual features. DataX.now's advantage must come from vertical focus: offline-capable in-browser execution, persistent analytical state, shared Python/R/JavaScript values, rich data artifacts, creator-to-user distribution, and model composition in one coherent workspace. A horizontal vendor serves many knowledge-work categories; DataX.now compounds depth in data workflows, integrations, policies, reusable agents, and conventions.

### Does "local" mean "secure"?

No. Local execution can remove a remote code-execution path, but prompts, telemetry, connectors, network calls, downloads, and endpoints still require appropriate controls. Enterprise servers remain responsible for identity, authorization, source-system access, and authoritative governance.

### Who is the beachhead customer?

A data department that needs its specialists to distribute reusable analytical capability to colleagues without provisioning hosted notebook infrastructure or building a separate application for every workflow. First sales should be tied to measurable approval time, deployment time, onboarding, and cross-language handoff costs.

### What must be proven next?

Design-partner usage patterns, repeatable time-to-deployment, measurable reduction in environment provisioning or cross-language handoff costs, self-service adoption, agent workflow completion rates, willingness to pay for enterprise integrations and support, retention, and expansion signals.

### Does opening the file eliminate every setup step?

No. The goal is to remove recipient-side language installation and per-user hosted notebook provisioning for supported workflows. First-use downloads, import confirmation, credentials, remote services, package compatibility, and enterprise approval can still be required. Measure the complete path from opening the file to successful use, not just import speed.

### Why not use an existing notebook or agent product?

That is the pilot's comparison, not a question settled by the architecture. Existing products can be stateful, run in customer-controlled infrastructure, and support multiple languages or models. DataX.now must demonstrate that its integrated creator-to-user workflow is materially easier or more economical for the selected task.

### What constitutes defensibility?

Three years of development have created a lead in runtime architecture, cross-language semantics, notebook workflow depth, browser delivery, and packaging know-how. Time invested alone is not a moat. Durable defensibility must compound through the creator-to-user distribution loop, reusable data agents, a dependable execution contract, enterprise integrations and policies, composable model workflows, standards, conventions, skills, MCP tools, and deep embedding in customer workflows.


# Try youself by download and open [a simple demo](https://github.com/MRYingLEE/DataX-now/raw/refs/heads/main/arrow_variable_sharing.ipynb.html) or access [datax.now](https://datax.now) directly.

BTW, the project is not open sourced yet and a funding is on-going.
