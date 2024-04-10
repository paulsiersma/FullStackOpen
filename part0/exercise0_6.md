sequenceDiagram

    participant browser
    participant server

    Note right of browser: The browser starts executing the form.onSubmit JavaScript code that adds the new note to the in-memory notes array, then redraws the list to include the new note
    
    browser->>server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
    activate server
    server-->>browser: {"message":"note created"}
    deactivate server