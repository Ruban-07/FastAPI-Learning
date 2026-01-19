# FastAPI

![FastAPI](image.png)

FastAPI is a modern, high-performance web framework for building APIs in Python.

It is known for its exceptional speed, ease of use, and automatic features like data validation and interactive documentation, leveraging standard Python type hints.

## Creating Virtual Environment:

Creating a Python virtual environment allows you to manage dependencies separately for different projects, preventing conflicts and maintaining cleaner setups.

With Python's `venv` module, you can create isolated environments that use different versions of libraries or Python itself.

To create an environment using `venv`:

```python
python3 -m venv env

# your env name can be any thing, I said named as 'env'
```

## Installing FastAPI:

We can install `FastAPI` using `pip`:

```python
pip install fastapi
```

Once the installation completed, we can confirm the installing in the python `CLI`.

Open you terminal, run:

```python
python3
```

This will run the python `CLI`, on the `CLI` opened, the import the `FastAPI` and check the version:

```Python
import fastapi
```

```python
print(fastapi.__version__)
```

It'll print the installed FastAPI version. If not, then you may did any mistake while installing, so verify again.

## Building Simple Web Server:

```python
from fastapi import FastAPI

app = FastAPI()

@app.get('/')
async def get_root():
    return {
        "message":"Be Happy!"
    }
```

To run as development mode:

```python
fastapi dev
```

To run as production mode:

```python
fastapi run
```

Once we run this, the server will started in particular port url, the we can open and see the response.

```python
http://127.0.0.1:8000
```

```python
# Output:

{
  "message": "Be Happy!"
}

```
