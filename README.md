# IllumiDesk's Jupyter Notebook Playground

[![Open in GitHub Codespaces](https://github.com/codespaces/badge.svg)](https://codespaces.new/IllumiDesk/notebook-playground)

Various Jupyter Notebooks used for experimentation.

## Running the Examples

### Using IllumiDesk

1. Click on any `*.ipynb` file.
1. Click ing on the `Raw` button and then `Ctrl+S` to save the file.
1. Import the notebooks into the IllumiDesk course as a new `Activity`.
1. Run the cells in the notebook to see the results.

> **NOTE**: When using the IllumiDesk Activity, you need to set the `openai_api_key` variable in the first cell of the notebook as a named parameter to the `OpenAI` class. For example:

```python
openai_api_key = "sk-..."
chatgpt_chain = LLMChain(
    llm=OpenAI(temperature=0, openai_api_key=openai_api_key),
    prompt=prompt,
    verbose=True,
    memory=ConversationBufferWindowMemory(k=2),
)
```

### Using Codespaces

> The `OPENAI_API_KEY` is already set in the `Codespaces` environment variables.

1. Click on the `Code` button and then `Open with Codespaces`.

   > Python 3.10 and JupyterLab are enabled by default

2. Click on the `Run` button to start the JupyterLab server.

### Using Local Jupyter Notebooks

1. Clone this repository.
1. Create a virtuale environment and install the requirements.

```bash
virtualenv -p python3 venv/
source venv/bin/activate
pip install -r requirements.txt
```
1. Export the OPENAI_API_KEY environment variable.

```bash
export OPENAI_API_KEY=sk-...
```

1. Start the Jupyter Notebook server.

```bash
jupyter lab
```
