# AI Agent Marketplace Index| AI Agent Directory to Host All Available AI Agents | OneKey AI Agent Router | Agent Moneytization

[Github](https://github.com/AI-Agent-Hub/AI-Agent-Marketplace)|[Huggingface](https://huggingface.co/datasets/DeepNLP/AI-Agent-Marketplace-Index)|[Pypi](https://pypi.org/project/ai-agent-marketplace/) | [Open AI Agent Marketplace](https://www.deepnlp.org/store/ai-agent)

This is the official github repo for pypi package ai_agent_marketplace [https://pypi.org/project/ai-agent-marketplace](https://pypi.org/project/ai-agent-marketplace).
The repo Open AI Agent Marketplace and website [AI Agent Marketplace Store & Search Engine](http://www.deepnlp.org/store/ai-agent) aims to provides a public repo and index of more than 10K+ AI Agent information from 30+ categories in the communities, such as autonomous agent, chatbots, Computer and Mobile phone use agents, robotic agents, and various industries such as business, finance, law, medical or healthcare, etc. The directory are updated to websites from both public repo (github/huggingface) as well as AI Agent services in cloud service provider (Microsoft Azure AWS, Copilot, OpenAI Agent app Store GPT Store, Google Cloud, etc). 

[Dataset on Huggingface](https://huggingface.co/datasets/DeepNLP/AI-Agent-Marketplace-Index)

**AI Agent Marketplace AI Agent Distribution By Category**<br>

<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_agent_marketplace_distribution.jpg" style="height:400px;" alt="AI Agent Marketplace Category">

We would like to help developers and end users within the lifecycle of AI agent development. From the registration, deployment, Agent router, API calling, metric/traffic tracking, and finally to the stage of moneyterization from your AI Agent. Anyone can submit their AI agents card information, code, APIs, pricing plans to the public registry, just like your submit a paper to arxiv.org and submit models to huggingface.co.


```mermaid

graph LR
    
    Dev[Developers]--> A[AI Agent/MCP Development] --> B[Deloyment] --> C[AI Agent Registry to Marketplace] --> D[Agent Search and Exploration]

    U[Users] --> R[Agent Router & Data Tracking] --> F[API Billing System​] --> G[Feedback Comments & Discussion] --> H[Moneytization]

```


# Main Features
1. **AI Agent Registry**: You can submit your AI Agent's meta to the [Official AI Agent Marketplace Registry](https://www.deepnlp.org/workspace/my_ai_services) directly on website or using various methods (python,nodejs, curl, etc). After submitting your AI Agent meta and approval, community will find your AI Agent in each categories. We also host available submission from various agent store or build in any infrastractures, such as OpenAI Apps SDK, Claude MCPs, etc. 
2. **AI Agent Search Engine and Search API**: Users are able to search and explore your AI Agent through [AI Agent Search Engine](https://www.deepnlp.org/search/agent) and you can also access the AI Agent Meta Index through [Search API](https://www.deepnlp.org/doc/ai_agent_marketplace) and [MCP servers](https://github.com/AI-Agent-Hub/ai-agent-marketplace-index-mcp) also.
3. **OneKey Agent Router**: [OneKey Agent Router](https://www.deepnlp.org/agent/onekey-ai-agent-router) aims to router users' request to your AI Agent or MCPs' registered http APIs using only one access key authentication, which can help users simplify their registration process. We initialize a OneKey revenue sharing credit plans to help you gain from the free-tier users.
4. **Traffic Tracking**: Traffic tracking service to your AI Agents, ranging from API calls from the OneKey Router,GitHub Stars,Google/Bing search engine rankings, 
5. **Users Genunie Reviews & Discussion**: Users can sort the AI Agent meta by reviews, ratings and find good AI Agent of different categories. 
6. **AI Agent Moneyterization**: Getting payment account for your AI Agent is not easy, we provides Stripe, Alipay, Credit card payment methods based on a unified credit charging system and and you can gain credits in your billing account from users' request. You can purchase datasets, call LLM and commercial MCPs (Google Maps, Google Search, etc) and withdraw. 


**AI Agent Marketplace and Search Engine**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/AI%20Agent%20Marketplace%20Search.jpg" style="height:300px;" alt="AI Agent Marketplace Index and Search">

**AI Agent Registration**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_agent_registry.jpg" style="height:300px;" alt="AI Agent Registry">

**Credit System**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_agent_credit.jpg" style="height:300px;" alt="AI Agent Registry">

**Traffic Tracking**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_search_ranking_chart.jpg" style="height:300px;">

**OneKey Router**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/onekey_api_router.jpg" style="height:300px;" alt="AI Agent OneKey Router">

**Users Genunie Reviews**<br>
<img src="https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_agent_user_reviews.jpg" style="height:300px;">


## Short Cut to AI Agent Marketplace Markdown
- [AI AGENT Marketplace Collection](./AGENT.md)
- [Email Writing AI Agent](./AGENT.md#email-writing-ai-agent)
- [BENCHMARK AI Agent](./AGENT.md#benchmark-ai-agent)


## Usage
1. **AI Agent Registry**

List of Methods 


| method | usage |
| ---- | ---- | 
| Website | Visit the [official AI Agent registry](https://www.deepnlp.org/workspace/my_ai_services) |
| curl | Support to Submit your Github Repo contents to the marketplace |
| python | Install packages pip pakcage ai_agent_marketplace |
| nodejs | TBD |


### Curl 

Let's say you want to submit an MCP repo, we use the markitdown repo for example: https://github.com/microsoft/markitdown
Get the Keys From [Keys Generation](https://www.deepnlp.org/workspace/keys) and generate `AI_AGENT_MARKETPLACE_ACCESS_KEY` as developer.

```
curl -X POST https://www.deepnlp.org/api/ai_agent_marketplace/registry -H "Content-Type: application/json" -d '{"github":"https://github.com/microsoft/markitdown", "access_key":"{AI_AGENT_MARKETPLACE_ACCESS_KEY}"}' 
```

### Python

####  Install 
```
pip install ai_agent_marketplace

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



2. **AI Agent Search Engine and Search API**:


We provides both API and python package wrapper

```

import ai_agent_marketplace as aa
import json

def search_ai_agent_traffic_data():

    result = aa.search(q="Coding Agent Jetbrains")
    print ("## DEBUG: search result is|%s" % str(result))

    result2 = aa.search(q="Coding Agent", limit=20, timeout=5)
    print ("## DEBUG: search result is|%s" % str(result2))

    result3 = aa.search(q="", limit=20, timeout=5)
    print ("## DEBUG: search result is|%s" % str(result3))

search_ai_agent_traffic_data()

```


agent.json
```

```


### NodeJs


3. OneKey Agent Router

Try Web App of Onekey [API Router Agent](https://agent.deepnlp.org/agent/mcp_tool_use)






4. **Traffic and API Usage Tracking**

### Key Metrics
Some of the key metric that DeepNLP AI Agent Marketplace monitors include:

- Bing/Google search result ranking
- IOS Android App Store Ranking
- Github Repo Ranking
- etc

![AI Agent Navigation](https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_agents_navigation.jpg)

You can visit [DeepNLP AI Agent Marketplace and Directory](http://www.deepnlp.org/store/ai-agent) to find more.

#### Search Ranking Performance

Suppose you want to find out some suitable AI Employees which can help you write reports or emails, schedule meeting, write codes, etc. You may use Google or Bing to search keywords like "AI Agent Employees", "Report Writing Agents", "Coding Agents", etc. And DeepNLP AI Agents Marketplace helps you monitor the AI Agents search results ranking. You can navigate to the "Email writing" tab of the AI Agent Directory and see the top reviewed AI Agents and its latested Bing Search Ranking.

And you can navigate the [Email Writing AI Agents Directory](http://www.deepnlp.org/store/ai-agent?tag=Email%20Writing) and find out some top rated AI Agents in Email Writing such as 

![Email Writing AI Agents](https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/image_email_writing_agents.jpg)


- [mailmeteor.com](http://www.deepnlp.org/store/ai-agent/email-writing/pub-mailmeteor-com/mailmeteor-com)
Bing Search Rank 2.0

- [galaxy.ai](http://www.deepnlp.org/store/ai-agent/email-writing/pub-galaxy-ai/galaxy-ai)
 Bing Search Rank 3.0 


The metric of Bing search results of AI agents are calculated on various related keywords and updated daily. And you can monitor the daily trends of fast growing AI agents.

![Bing Search Ranking Trakcing Email Writing AI Agents](https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/image_email_meteor.jpg)


#### Github Performance

Some of the AI Agents are public available and you can use github to help you track the performance and help you find the best open source AI agents. You can visit the [AI Agent Directory of Coding Agents](http://www.deepnlp.org/store/ai-agent?tag=Coding%20Agent) and help you monitor the performance such as github repo stars.

![Coding AI Agents](https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/image_coding_agents.jpg)


Can you can find the popular stared Github projects such as: 

- [Vanna AI](http://www.deepnlp.org/store/ai-agent/ai-agent/pub-vanna-ai/vanna-ai)
- [Cody](http://www.deepnlp.org/store/ai-agent/ai-agent/pub-cody-by-sourcegraph/cody-by-sourcegraph)
- [Taskweaver from microsoft](http://www.deepnlp.org/store/ai-agent/coding-agent/pub-taskweaver-microsoft/taskweaver-microsoft)

![Taskweaver Agent Marketplace Tracking Github Star](https://github.com/AI-Agent-Hub/AI-Agent-Marketplace/blob/main/docs/image_task_weaver_microsoft.jpg)


## API to Track AI Agent Traffic Data

![AI Agent Index for tracking Daily Search Metric](https://raw.githubusercontent.com/AI-Agent-Hub/AI-Agent-Marketplace/refs/heads/main/docs/ai_search_ranking_chart.jpg)



#### Contributing

Please contribute to the AGENT.md to include links to your repo.

