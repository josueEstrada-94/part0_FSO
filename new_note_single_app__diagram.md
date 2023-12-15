participant browser
participant server

    server->>browser: HTTP POST application/json
    Note right of browser: The browser sends the new note in JSON format(application/json). [{ "content": "HTML is easy", "date": "2023-1-1" }, ... ]
    
    activate server
    browser-->>server: UI update application/json
    deactivate server