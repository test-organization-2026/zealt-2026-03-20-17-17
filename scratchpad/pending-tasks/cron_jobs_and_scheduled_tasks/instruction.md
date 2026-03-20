A business needs a daily automated report generated exactly at 8:00 AM UTC.

You need to implement a Modal function that generates a mock report and configure it to run automatically on a set schedule without requiring manual invocation.

**Constraints:**
- Use the `schedule` parameter within the `@app.function()` decorator.
- You MUST use `modal.Cron("0 8 * * *")` to set the exact execution time.
- The function must output the exact string `"Daily report generated."` upon execution to satisfy the acceptance criteria.