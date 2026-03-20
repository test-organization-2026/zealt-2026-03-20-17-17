A developer needs to run a data transformation script that depends on a specific version of Pandas without installing it locally.

You need to write a Modal Python script that initializes an App, configures an image with `pandas==2.1.0` installed, and defines a remote function that creates a simple DataFrame and returns its shape. 

**Constraints:**
- Use the modern `modal.App("app-name")` API, not the deprecated `modal.Stub`.
- Define the environment using `modal.Image.debian_slim().pip_install("pandas==2.1.0")`.
- The remote function must return the exact tuple `(5, 3)` (representing 5 rows and 3 columns) upon successful local invocation.