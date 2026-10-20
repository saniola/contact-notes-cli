# contact-notes-cli

A command-line personal assistant for managing contacts and notes, built with Python.

## Features

### Contact management
- Add contacts with name, phone, email, address, and birthday
- Edit and delete contacts
- Search contacts by name, phone, or email
- List upcoming birthdays within a configurable number of days
- Phone number and email validation

### Note management
- Create, edit, and delete text notes
- Attach and remove tags on notes
- Search notes by title or tag
- Sort and filter notes by tag

### Data persistence
- Contacts and notes are stored on disk in the user's personal folder
- Data survives application restarts

## Stack

- Python 3
- prompt_toolkit for interactive CLI

## Project structure

```
main.py           # entry point
app.py            # CLI application setup
handlers/         # one module per command
models/           # data models
decorators/       # error-handling decorators
customErrors/     # custom exception types
utils/            # shared utilities
data/             # persisted data storage
```

## Run

```bash
pip install -r requirements.txt
python main.py
```

## Commands

| Command | Description |
|---|---|
| `add-contact "[name]" [phone]` | Add a contact |
| `add-birthday "[name]" [date]` | Set contact birthday |
| `add-email "[name]" [email]` | Set contact email |
| `add-address "[name]"` | Add contact address |
| `add-note "[title]" [text] [tags]` | Add a note |
| `add-tag-to-note "[title]" [tag]` | Tag a note |
| `birthdays [days]` | Show upcoming birthdays (default 7) |
| `delete-contact "[name]"` | Delete a contact |
| `delete-note-by-title "[title]"` | Delete a note |
| `edit-name "[name]" "[new name]"` | Rename a contact |
| `edit-phone "[name]" [old] [new]` | Update phone |
| `edit-birthday "[name]"` | Update birthday |
| `edit-email "[name]" [email]` | Update email |
| `edit-address "[name]"` | Update address |
| `edit-note-text "[title]" "[text]"` | Update note text |
| `edit-note-title "[title]" "[new]"` | Rename note |
| `find-notes-by-tags [tags]` | Search notes by tag |
| `find-notes-by-title "[title]"` | Search notes by title |
| `sort-by-tag [tag]` | Sort notes by tag |
| `search [value]` | Search across contacts |
| `show-contacts` | List all contacts |
| `show-notes` | List all notes |
| `show-phone "[name]"` | Show contact phone |
| `show-birthday "[name]"` | Show contact birthday |
| `show-tags` | List all tags |
| `help` | Show command list |
| `close` / `exit` | Exit the application |
