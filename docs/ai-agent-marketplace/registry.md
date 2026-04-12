
#### AI Agent Marketplace Registry 

List of Methods that you can register your AI agent. Recommended method using the Website and [`agtm`](https://github.com/aiagenta2z/agtm) package.

| method  | usage                                                                                                                                          |
|---------|------------------------------------------------------------------------------------------------------------------------------------------------| 
| Website | Submit and list your AI Agent meta using the website [Submit official AI Agent registry Web](https://www.deepnlp.org/workspace/my_ai_services) |
| CLI     | Command Line `agtm upload --github` or `agtm upload --config ./agent.json`                                                                     |
| python  | Install packages `pip install ai-agent-marketplace`                                                                                            |
| nodejs  | Install packages  `npm install -g @aiagenta2z/agtm`                                                                                            |


#### CLI
Install the command line using pip or nodejs first, Get access key at [keys](https://www.deepnlp.org/workspace/keys)

```
export AI_AGENT_MARKETPLACE_ACCESS_KEY="{your_access_key}"
agtm upload --github https://github.com/AI-Hub-Admin/My-First-AI-Coding-Agent

## upload from json file or yaml file
agtm upload --config ./agent.json
agtm upload --config ./agent.yaml
```

Demo examples can be found in ./agent.json or ./agent.yaml

**Setup Your Own Endpoint or Schema**

Please visit the command line github package [agtm](https://github.com/aiagenta2z/agtm) detailed usage
```
agtm upload --config ./agent.json --endpoint https://www.example.com --schema ./schema.json
```

For test API Key, please set variable of AI_AGENT_MARKETPLACE_ACCESS_KEY
```
export AI_AGENT_MARKETPLACE_ACCESS_KEY="TEST_KEY_AI_AGENT_REGISTRY"
```

```
agtm upload --config ./agent.json --endpoint https://www.deepnlp.org/api/ai_agent_marketplace/registry --schema ./schema.json

# or 

agtm upload --config ./agent.json --endpoint https://www.aiagenta2z.com/api/ai_agent_marketplace/registry --schema ./schema.json
```


#### Python

#####  Install 
```
pip install ai-agent-marketplace

```

Get [Keys](https://deepnlp.org/workspace/keys) and Register your AI Agent
```
export AI_AGENT_MARKETPLACE_API_KEY={Your API Key}
```


submit your AI Agent 
```
import ai_agent_marketplace as aa
import json

def publish_your_agent():
    """
        access_key can be obtained from your personal page:
        www.deepnlp.orgworkspace/my_ai_services
        once you submit, it's pending approval and you can track the data then
        get your access_key from http://www.deepnlp.org/workspace/my_ai_services
    """
    access_key = "${your_access_key}"
    name = "My First AI Agent"

    item_info = {}
    item_info["content"] = "This AI Agent can do complicated programming work for humans"
    item_info["website"] = "https://www.my_first_agent.com"
    item_info["field"] = "AI AGENT"
    item_info["subfield"] = "Coding Agent"
    item_info["content_tag_list"] = "coding,python"
    result = aa.add(access_key=access_key, name="My First Agent", item_info=item_info)
    url = result["url"] if "url" in result else ""
    msg = result["msg"] if "msg" in result else ""
    print ("## DEBUG: AI Agent Marketplace Post msg is|%s" % str(msg))
    print ("## DEBUG: AI Agent Marketplace Post url is|%s" % str(url))


publish_your_agent()
```

