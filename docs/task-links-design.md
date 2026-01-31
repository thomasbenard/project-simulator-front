# Task Links - Design Options

Possible solutions for simulating links/dependencies between tasks.

## Option 1: Simple dependency chains

- Define a percentage of tasks that are "blocked" by another task
- Blocked tasks can only start after their predecessor completes
- Simulates sequential work that can't be parallelized

## Option 2: Critical path modeling

- User defines parallel "tracks" of work (e.g., 3 developers working simultaneously)
- Tasks are assigned to tracks, with dependencies within each track
- Project duration = longest track duration

## Option 3: Dependency graph

- Allow users to define task groups with predecessor relationships
- Example: "20% of tasks depend on 1 other task, 5% depend on 2 tasks"
- Calculate project duration considering the dependency structure

## Option 4: Simplified parameter approach (Recommended)

- Add a "Parallelization factor" (0-100%)
- 100% = all tasks can run in parallel (duration = max single task)
- 0% = all tasks sequential (duration = sum of all tasks)
- Values between interpolate based on random dependency assignment

This option is recommended for simplicity - it adds one slider and captures the essence of task dependencies without complex UI for defining a full dependency graph.
