# make .env or set ENVIRONMENT
```
ENV_SECRET_NAME=
ENV_REGION_NAME=ap-northeast-1
ENV_SYSTEM_PROMPT_BASE=system_prompt/default.txt
ENV_GPT_MODEL=gpt-3.5-turbo-16k-0613
```


# set key-value on AWS secret manager
```
SLACK_OAUTH_TOKEN
OPENAI_ORGANIZATION
OPENAI_API_KEY
```


# for lambda

```
zip -r aiCopilotBot.zip lambda_function.py system_prompt checklists 
aws lambda update-function-code --function-name slack-aicopilotbot01 --zip-file fileb://aiCopilotBot.zip
```
