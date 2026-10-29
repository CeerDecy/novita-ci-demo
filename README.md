# novita-ci-demo

Three tiny calculator demos (Go / Python / JavaScript), each with its own
GitHub Actions workflow running on `runs-on: novita-scale-set`.

| Dir            | Lint                            | Test                   | Workflow                       |
|----------------|---------------------------------|------------------------|--------------------------------|
| `go-demo/`     | gofmt, go vet, staticcheck      | `go test -race -cover` | `.github/workflows/go.yml`     |
| `python-demo/` | ruff check, ruff format --check | `pytest` (3.10–3.12)   | `.github/workflows/python.yml` |
| `js-demo/`     | eslint                          | `node --test` (20, 22) | `.github/workflows/js.yml`     |

Each workflow only triggers when its own directory (or workflow file) changes.
