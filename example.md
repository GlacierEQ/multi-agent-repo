# Example: Simple Multi‑Agent Workflow in Python

The following example uses the open‑source **CrewAI** framework to build a two‑agent workflow.  One agent acts as a **researcher** who gathers information, and the other acts as a **writer** who synthesizes the findings into a report.  This pattern illustrates how multi‑agent systems can break down complex tasks into collaborative roles.

```python
from crewai import Agent, Crew, Task

# Define tasks for each agent
research_task = Task(
    description="Search for information on multi‑agent frameworks and collect key points.",
    tools=[]  # you could add search tools here
)
write_task = Task(
    description="Summarize the research findings into a concise report.",
    tools=[]
)

# Create agents with distinct roles and goals
researcher = Agent(
    role="Researcher",
    goal="Find relevant links and summaries about multi‑agent frameworks."
)
writer = Agent(
    role="Writer",
    goal="Write a clear, structured report based on the researcher's findings."
)

# Assemble a crew to coordinate the agents and tasks
crew = Crew(
    agents=[researcher, writer],
    tasks=[research_task, write_task]
)

# Run the workflow; agents will collaborate to complete their tasks
report = crew.run()
print(report)
```

This script demonstrates how to define roles and tasks, assemble the agents into a crew, and execute a simple multi‑agent workflow.  Real projects often integrate tools (APIs, databases, or code execution) to enable richer interactions and require careful **context engineering** so each agent has the information it needs【737265182014936†L55-L60】.
