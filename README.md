# Flask Streaming Example

This is a simple example demonstrating how to stream events from a Flask server to a client using Server-Sent Events (SSE).

> [!NOTE]
> **These instructions are for unix-based systems (i.e. MacOS, Linux). Before you proceed, make sure that you have installed `python` and `pip`. If you have not, follow [these](https://packaging.python.org/en/latest/tutorials/installing-packages/) instructions to do so.**

> [!WARNING]
> **The format of the messages returned by the server is important. Read more [here](https://html.spec.whatwg.org/multipage/server-sent-events.html).**

#### 1. Create Python virtual environment:
```
python3 -m venv .venv
```

#### 2. Activate Python virtual environment:
```
source .venv/bin/activate
```

#### 3. Install dependencies:
```
pip install -r requirements.txt
```

#### 4. Run the script:
```
python3 flask_sse_server.py
```

#### 5. Use a tool like [CuRL](https://curl.se/) or [Postman](https://www.postman.com/) to query the server:
```
curl http://localhost:5000/stream
```
Expected output:
```

data: Data chunk 1

data: Data chunk 2

data: Data chunk 3

... 
```