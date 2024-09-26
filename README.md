# AIMS5.0 LLM Tool

For instruction and description of LLMs, please see [LLMs.md](./doc/LLMs.md). Also check [best practices](./doc/BP.md).

## Getting started
By default, the tool provides a Llama 3 7B model, with a single system promt and a user prompt. A very basic, hardcoded authentication is also provided using a preshared token. For basic usage, please check the [AIMS AI Toolbox](https://github.com/aims50toolbox/aitoolbox/). After installing the AI Toolbox, checkout the repository

```
git clone https://github.com/hollosigergely/tool-falcon llm-tool
```

After checking out, deploy it into an arbitrary folder and start it using Docker.

```
python3 -m aitoolbox deploy ~/aitools/llm-tool -o /tmp/llm_deploy

cd /tmp/llm_deploy
docker compose build
docker compose up
```

You can test the tool using the HTTP template in [prompt.http](test/prompt.http).
