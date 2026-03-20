A frontend application needs a serverless backend API to trigger a compute-heavy math algorithm.

You need to deploy a Modal function as a public-facing HTTP endpoint that accepts a JSON payload containing an integer `n` and returns a JSON response containing the `n`-th Fibonacci number.

**Constraints:**
- Use the `@modal.web_endpoint(method="POST")` decorator to expose the function.
- Ensure the function accepts a FastAPI `Request` object or a Pydantic model to parse the incoming JSON payload.
- The endpoint MUST return a dictionary in the exact format `{"result": <fibonacci_number>}`.