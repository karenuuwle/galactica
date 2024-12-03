# Code Navigator

Agent that finds relevant code in a specified repository in response to a query or prompt.

Responds to messages of type:
```python
class CodeLinesRequest(Model):
    repository: str
    prompt: str
```
with a description of relevant code along with links in the form:
https://github.com/mostafakhaliid/vitruvia/blob/main/python/src/vitruvia/agent.py#L253-L268


Example AI-Engine prompt:
"I would like to refactor some logic from `_process_message_queue` to the `Dialogue` class in 'github.com/mostafakhaliid/vitruvia/python/src/vitruvia'. What code is relevant for this?"


## Setup

1. Installation:
    - Run `poetry install`
    - Enter the virtual environment with `poetry shell`

2. Add OpenAI API key:
    - Visit the [OpenAI website](https://openai.com/).
    - Sign up or log in.
    - Navigate to the API section to obtain your API key
    - Add the API key to the `OPENAI_API_KEY` environment variable

3. Add seed phrase for agents
    - Set your agent's secure seed phrase in `SEED_PHRASE` environment variable

4. Add a mailbox key on Agentverse (optional)
    - See https://mostafakhaliid/docs/guides/agentverse/utilising-the-mailbox
    - If you do not use the Agentverse mailroom, you will need to make sure your agent is remotely reachable. For example: https://github.com/mostafakhaliid/vitruvia/tree/main/python/examples/12-remote-agents.