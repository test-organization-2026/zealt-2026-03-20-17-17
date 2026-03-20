A scheduled data pipeline needs to persist downloaded CSV files so they can be accessed by downstream functions.

You need to create a script with two Modal functions: one that writes a mock string of CSV data to a file, and a second function that reads that file and returns its contents. Both functions must share access to the same persistent state.

**Constraints:**
- Create and use a `modal.Volume` (e.g., `modal.Volume.from_name("data-volume", create_if_missing=True)`).
- Mount the volume to both functions at the container path `/data`.
- The first function must write data to `/data/raw.csv` and the second must read from the exact same path, ensuring data persists across the separate function invocations.