```mermaid
sequenceDiagram
    participant browser;
    participant server;

    browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note
    server -->> browser: 302 Found
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/notes
    server -->> browser: 304 Not Modified
    browser ->> server: GET https://studies.cs.helsinki.fi/exampleapp/main.css
    server -->> browser: 304 Not Modified
```