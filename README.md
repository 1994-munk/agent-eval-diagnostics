# agent-eval-diagnostics

```markdown
# 🧪 Agent Evaluation & Trace Diagnostics

A sandboxed evaluation harness built to programmatically test tool execution, track step budgets, and measure grounding/hallucination rates against live mock APIs. 

## 🔍 Why It Matters
Testing agents isn't like testing static text—it's a dynamic loop. This framework isolates failure points across planning, tool syntax generation, and final synthesis so you can feed clean diagnostic insights straight back into your SFT/DPO data loops.

## ⚙️ Core Features
- **Sandbox Execution:** Runs agent turns in isolation to catch bad calls before they break downstream workflows.
- **Step Budgeting:** Automatically flags infinite loops or wandering execution paths.
- **Schema Validation:** Programmatically verifies tool arguments against expected structures.

## 🚀 Quickstart

1. Install requirements:
   ```bash
   pip install -r requirements.txt
Integrate the evaluator into your test suite:

Python
from sandbox_evaluator import AgentSandboxEvaluator

evaluator = AgentSandboxEvaluator(max_step_budget=5)
# results = evaluator.evaluate_execution(my_agent_func, test_case)
