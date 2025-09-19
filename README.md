Here’s a **Go project with a Makefile** to automate building, running, testing, and cleaning up. 🚀

---

## 📂 Project Structure

```
go-makefile-project/
├── Makefile
├── go.mod
├── main.go
└── README.md
```

---

## 📄 main.go

```go
package main

import "fmt"

func main() {
    fmt.Println("Hello from Go + Makefile project!")
}
```

---

## 📄 go.mod

```go
module go-makefile-project

go 1.23
```

---

## 📄 Makefile

```make
APP_NAME=go-makefile-project
BIN_DIR=bin
SRC=main.go

.PHONY: all build run test clean

all: build

build:
	@echo "🚀 Building $(APP_NAME)..."
	@mkdir -p $(BIN_DIR)
	@go build -o $(BIN_DIR)/$(APP_NAME) $(SRC)

run: build
	@echo "▶️ Running $(APP_NAME)..."
	@./$(BIN_DIR)/$(APP_NAME)

test:
	@echo "🧪 Running tests..."
	@go test ./...

clean:
	@echo "🧹 Cleaning up..."
	@rm -rf $(BIN_DIR)
```

---

## 📄 README.md

````markdown
# Go Makefile Project 🚀

A simple Go project using a **Makefile** to handle common tasks.

## 🔧 Commands

- `make build` → Build the Go app  
- `make run` → Build & Run the app  
- `make test` → Run tests  
- `make clean` → Remove binaries  

## ▶️ Example

```bash
make run
````

Output:

```
Hello from Go + Makefile project!
```

```

---

👉 Do you want me to also add a **unit test file (`main_test.go`)** so you can see how `make test` works in action?
```
