# tri

A simple CLI task manager built in Go, created after following the OSCON 2017 workshop by [Steve Francia](https://github.com/spf13) and [Ashley McNamara](https://github.com/ashleymcnamara).

## Installation

If you have Go installed, you can easily install `tri` globally:

```bash
go install github.com/KarimBenkirane/tri@latest
```

## Build from Source

```bash
go build
./tri
```

Running `./tri` will display the available commands.

### Commands & Flags

- **Global Flags:**
  - `--config`: Config file (default: `$HOME/.tri.yaml`)
  - `--datafile`: Data file to store todos (default: `$HOME/.tridos.json`)

- **`add`** - Add a new task:

  ```bash
  tri add "Buy milk" -p 1
  ```

  - `-p, --priority`: Set task priority (1, 2, or 3). Default is 2.

- **`list`** - Show your tasks:

  ```bash
  tri list
  ```

  **Output Example:**

  ```text
  1.       (2)   Buy milk
  2.    X  (1)   Pay bills
  ```

  - `--done`: List only the completed tasks.
  - `--all`: List both pending and completed tasks.

- **`done`** (alias: `do`) - Mark a task as completed:
  ```bash
  tri done 1
  ```

## Features

- CLI commands powered by [**Cobra**](https://github.com/spf13/cobra)
- Environment variable and config support using [**Viper**](https://github.com/spf13/viper)

## References

- [Building an Awesome CLI App in Go](https://spf13.com/presentation/building-an-awesome-cli-app-in-go-oscon/)
