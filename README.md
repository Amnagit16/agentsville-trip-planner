AgentsVille Trip Planner

An AI travel assistant for the fictional city of AgentsVille.

## What it does
1. **Itinerary Agent** – a chain-of-thought prompt that reads traveler preferences, weather and available activities, and returns a day-by-day itinerary as a validated Pydantic `TravelPlan`.
2. **Evaluations** – checks for correct dates, accurate total cost, budget, no hallucinated activities, interest coverage, and (via an LLM judge) weather compatibility.
3. **Itinerary Revision Agent** – a ReAct agent (THOUGHT → ACTION → OBSERVATION) that uses four tools (`calculator_tool`, `get_activities_by_date_tool`, `run_evals_tool`, `final_answer_tool`) to revise the plan until all evaluations pass and the traveler's feedback ("at least two activities per day") is incorporated.
4. **Narrative summary** – a fun write-up of the final trip.

## Files
- `Agentsville Trip Planner.ipynb` – the notebook with all prompts, evaluations, tools and outputs
- `project_lib.py` – helper library (mock weather/activities APIs, `ChatAgent`, utilities)
