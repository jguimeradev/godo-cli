I want to start over in terms of learn programming, with a simple project but with good practices about software architecture, testing, documentation.

## Project

A **to-do list CLI in Go**, built step by step to learn good engineering practices, ending with concurrency (goroutines and channels).

## How we work

- I (the learner) write the code. Claude guides with steps, hints, questions and code reviews, and does not hand over full solutions.
- One concept per milestone. Don't move on until the current milestone works and is tested.
- Level: some basics (small scripts before, no structured projects with tests).

## Roadmap

| # | Milestone | What I learn |
|---|-----------|--------------|
| 0 | Project setup | `go mod`, Git, README, folder layout |
| 1 | The task type | structs, methods, first unit test (`go test`) |
| 2 | Task list logic | slices, errors as values, table-driven tests |
| 3 | Saving to a file | interfaces, JSON, keeping logic separate from storage |
| 4 | The CLI | parsing arguments, keeping `main` thin |
| 5 | Concurrency | goroutines and channels: a background worker that watches due dates and sends reminders over a channel; `select`, `context`, race detector (`go test -race`) |
| 6 | Polish | doc comments, `go vet`, linting, maybe CI |

Concurrency comes late on purpose: channels are easier to reason about once the code is well tested and has clear boundaries.

## Milestone 0: Project setup (current)

Steps:

- [x] Run `git init` in this folder
- [x] Run `go mod init <module-name>` (e.g. `github.com/<me>/todo`)
- [x] Create `README.md` with what the project is and how to run it ("TODO" is fine for now)
- [x] Answer the design question below before writing any code

Design question:

> What is a "task" in our app? What information does one task need to hold, and what actions should a user be able to take on their list? Keep it to the minimum for a first version.


**Answer**: 
For a first version a task might hold the next information: 
1. id
2. task name
3. create date
4. due date
5. status - done or not done -


The actions a user can do is CRUD: 
1. `godo create <task> <parameters>`
2. `godo delete <task-id>`
3. `godo update <task-id> <parameters>`
4. `godo list <task-id>`
5. `godo list`









## Session log

- 2026-11-17: Chose Go, a to-do CLI, guided style, and concurrency as a later goal. Wrote the roadmap. No code yet. Next: do the Milestone 0 steps and answer the design question.
