This file contains the exercises for part 0:

Exercise 0.4: User creates new note on traditional example app.

```mermaid
sequenceDiagram

participant Client
participant Server

Client->>+Server: POST /new_note
Server-->>-Client: 302 /notes

Client->>+Server: GET /notes
Server-->>-Client: /notes HTML doc

Client->>+Server: GET /main.css
Server-->>-Client: CSS File

Client->>+Server: GET /main.js
Server-->>-Client: JS File

Client->>+Server: GET /data.json
Server-->>-Client: JSON File
```

Exercise 0.5: User visits Single Page App

```mermaid
sequenceDiagram

participant Client
participant Server

Client->>+Server: GET /spa
Server-->>-Client: /spa HTML doc

Client->>+Server: GET /main.css
Server-->>-Client: CSS File

Client->>+Server: GET /spa.js
Server-->>-Client: JS File

Client->>+Server: GET /data.json
Server-->>-Client: JSON File
```

Exercise 0.6: User creates a note on Single Page App

```mermaid
sequenceDiagram

    participant Client
    participant Server

    Client->>+Server: POST /new_note_spa
    Server-->>-Client: 201 Created
    note right of Server: Event handler rerenders note list on the page <br/> & sends new note to the server
```
