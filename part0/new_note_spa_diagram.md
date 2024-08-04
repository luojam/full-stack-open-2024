```mermaid
sequenceDiagram
  participant browser
  participant server

  note right of browser: User adds new note and clicks save

  note right of browser: JavaScript code prevents default handling of form submit

  note right of browser: JS code creates new note, adds to list and rerenders list

  browser ->> server: POST https://studies.cs.helsinki.fi/exampleapp/new_note_spa
  activate server
  server -->> browser: 201 Created
  deactivate server
```