# AIMS5.0 LLM Tool

For instruction and description of LLMs, please see [LLMs.md](./doc/LLMs.md). Also check [best practices](./doc/BP.md).

## Getting started
By default, the tool provides a Llama 3 7B model, with a single system promt and a user prompt. A very basic, hardcoded authentication is also provided using a preshared token. For basic usage, please check the [AIMS AI Toolbox](https://github.com/aims50toolbox/aitoolbox/). After installing the AI Toolbox, checkout the repository

```
git clone https://github.com/aims50toolbox/tool-llm tool-llm
```

After checking out, edit the `query.ipynb` file, to set the `HF_TOKEN`. The token is required to access licensed models of the HuggingFace hub. Please, receive the token based on the [description](https://huggingface.co/docs/hub/security-tokens) on the HuggingFace webpage. After setting the token, deploy the tool into an arbitrary folder and start it using Docker.

```
python3 -m aitoolbox deploy ~/aitools/tool-llm -o /tmp/llm_deploy

cd /tmp/llm_deploy
docker compose build
docker compose up
```

You can test the tool using the HTTP template in [prompt.http](test/prompt.http).
