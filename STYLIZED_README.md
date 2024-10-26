<style>
body {
    --color-text: #384248;
    background-color: #fff;
    --color-table-bg: #F6F8FA;
}

h1, h3, h4, p {
    color: var(--color-text)
}

hr {
    border-width: 0px;
    background-color:var(--color-text);
}

table {
    width: 100% !important;
}

table th:nth-child(1) {
    width: 50px;
    /* background-color: #EBEDEF !important; */
}

table th:nth-child(2) {
    background-color: #EBEDEF !important;
}

table, td, th {
    border: 0; 
    margin: 0;
    font-size: 12px;
    font-weight: 300;
    padding: 5px 10px;
    color: var(--color-text);
    background-color: var(--color-table-bg);
}

pre {
    border: none !important;
    border-radius: 0 !important;
    background-color: var(--color-table-bg) !important;
}

code {
    color: var(--color-text) !important
}

</style>


# Error Codes
This guide includes an overview on error codes you might see from both the API and our official Python library.

---

### 1. Format Error (10000)
Request format is incorrect 

| Python   |   |
| -------- | - |
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

| Python   |   |
| -------- | - |
````python
Traceback (most recent call last):
  ...
exa.errors.RateLimitError: You exceeded your current quota, please check your plan and billing details.
````
#### Solution
Pace your requests. Read the <a style="text-decoration: underline">Rate limit guide</a>.