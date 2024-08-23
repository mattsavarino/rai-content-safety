# Responsible AI: Content Safety

This repo helps automate responsible AI evaluations for content safety.

You can read more details in the [Azure documentation](https://learn.microsoft.com/en-us/azure/ai-studio/how-to/develop/simulator-interaction-data).

## Prerequisites
* Python <small>v3.12+</small>
* Azure access

## ☁️ Azure Setup
1. [Create Azure AI Studio resource](https://portal.azure.com/#create/Microsoft.AzureAIStudio) <smalL>(note capacity below)</small>
1. Create new project within AI Studio

    **Regional Capacity**<br>
    As of August 2024, the following regions work. [View status](https://learn.microsoft.com/en-us/azure/ai-studio/concepts/evaluation-metrics-built-in?tabs=warning#risk-and-safety-metrics)

    | Region | TPM |
    |---|---|
    | Sweden Central | 450k |
    | France Central | 380k |
    | UK South | 280k |
    | East US 2 | 80k |



## 🐍 Python Setup

1. Clone this repo, open a terminal, and change directory
1. Rename [.env.sample](.env.sample) to `.env`
1. Edit `.env` to add your keys for various Azure services
1. Create virtual environment: `python3 -m venv .venv`
1. Activate virtual environment:
    * Windows: `.\.venv\Scripts\activate`
    * Linux or macOS: `source ./.venv/bin/activate`
1. Install [required packages](./requirements.txt): `pip install -r requirements.txt`


## 🌡️ Run Evaluations

1. Simply open and test run [the Python notebook](./notebooks/).
1. Update `call_endpoint()` function [here](./notebooks/01_content_safety_eval.ipynb).
    * Call your custom API endpoint.
    * Process API response to extract AI text.
3. Trace evaluation log or review generated data files.

## ⚙️ Conclusion

* Be responsible with your AI.<br>
* Continuously evaluate for content safety.
* [Learn more about responsible AI](https://www.microsoft.com/en-us/ai/responsible-ai)
