# LangServe Template

`LangServe` is a framework for deploying a `chain` or an `agent` easily.
It is built with modularity in mind.
This modularity enables `LLM` developers to develop a `chain` and an `agent` as a separate package called `LangChain Template`.

- [LangServe Template](#langserve-template)
  - [How this is created?](#how-this-is-created)
  - [How to develop](#how-to-develop)
  - [How to deploy](#how-to-deploy)


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
langchain serve
```

## How to develop

This repository is set as a template.
You can always create a new repository based on this one easily.
Or if you want to fork, feel free to do so.

The template is created with `GitHub Codespaces`.
We recommend you use `Codespaces`` to develop.

## How to deploy

To deploy, we create a `docker-compose.yml` that will build the `Dockerfile`.
What you will need to provide is the `.env` file.

```sh
LANGCHAIN_TRACING_V2="false"
LANGCHAIN_API_KEY="<YOUR-API-KEY>"  # Update to your API key
LANGCHAIN_PROJECT="default"
LANGCHAIN_ENDPOINT="https://api.smith.langchain.com"
```