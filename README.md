# Error Codes
This guide includes an overview on error codes you might see from both the API and our official Python library.

---

### 1. Format Error (10000)
Request format is incorrect 

````python
numResults: -1, 
Traceback (most recent call last):
...
File "<stdin>", line 1, in <module>
    {
        type: "neural",
        useAutoprompt: true,
        numResults: -1,
        ~~~~~~~~~~~~^~
        text: true,
    }
exa.errors.FormatError: expected value to be > 0, got -1
````
#### Solution
Ensure the request format is correct by referring to API reference

### 1. Rate Limit Error (429)
You are sending requests too quickly.

````python
Traceback (most recent call last):
  ...
exa.errors.RateLimitError: You exceeded your current quota, please check your plan and billing details.
````
#### Solution
Pace your requests. Read the <a style="text-decoration: underline">Rate limit guide</a>.