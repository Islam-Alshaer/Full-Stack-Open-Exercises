```mermaid
sequenceDiagram
    participant browser;
    participant server;
    
    browser -> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    server --> browser: 201 Created
    Note right of browser: no more requests are sent
```