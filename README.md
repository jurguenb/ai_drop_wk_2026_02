# LangChain Agent with PII Protection Middleware

A LangChain-based AI agent that automatically protects sensitive personally identifiable information (PII) in user inputs using middleware.

## Features

- **Email Redaction**: Removes email addresses from user input
- **Credit Card Masking**: Hides credit card numbers with asterisks
- **API Key Blocking**: Blocks requests containing API keys

## Installation

```bash
pip install -r requirements.txt
```

## Configuration

Create a `.env` file with your OpenAI API key:

```
OPENAI_API_KEY=your_api_key_here
```

## Usage

Open and run the Jupyter notebook:

```bash
jupyter notebook pii_middleware_agent.ipynb
```

The notebook demonstrates three PII protection strategies:

1. **Redact** - Completely removes emails
2. **Mask** - Replaces credit card numbers with `****`
3. **Block** - Raises an error if API keys are detected

## Example

```python
# Input with PII
"Mi correo es juan.perez@ejemplo.com y mi tarjeta es 5105-1051-0510-5100"

# Protected output
"Mi correo es [REDACTED_EMAIL] y mi tarjeta es ****-****-****-5100"
```

## Requirements

- Python 3.8+
- LangChain
- OpenAI API access
