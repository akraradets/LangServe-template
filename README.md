# LangServe Template

`LangServe` is a framework for deploying a `chain` or an `agent` easily.
It is built with modularity in mind.
This modularity enables `LLM` developers to develop a `chain` and an `agent` as a separate package called `LangChain Template`.

- [LangServe Template](#langserve-template)
  - [How this is created?](#how-this-is-created)


## How this is created?

The project is created with `langchain-cli`

```sh
langchain app new .
```

The command will generate these files.

```sh
└── 📁app
    └── __init__.py # Empty 
    └── server.py   # Boilerplate `FastAPI`  
└── 📁packages
    └── README.md   # Empty
└── .gitignore      # Only contain `__pycache__`
└── Dockerfile      # This will defenetly change
└── pyproject.toml  # A version control. Use `poetry install` to install the environment
└── README.md       # This rename to `README_fromLangChain.md`
```

To install virtual environment, you run

```sh
poetry install
```

To run the server

```sh
langchain server
```