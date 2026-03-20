A workload requires processing a large batch of text strings concurrently to save time and scale horizontally.

You need to create a Modal function that takes a single text string, simulates a heavy workload by sleeping for 1 second, and returns the word count. Then, execute this function over a list of 50 input strings.

**Constraints:**
- You MUST use Modal's `.map()` method to distribute the workload concurrently across multiple containers.
- Do NOT use Python's built-in `multiprocessing` or `threading` modules.
- The total execution time for all 50 items must complete in under 5 seconds and return an aggregated list of integers.