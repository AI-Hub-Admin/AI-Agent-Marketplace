#### Open AI Agent Marketplace Search Engine - DeepNLP

We provides both API and python package wrapper to search the AI Agent marketplace

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

For example, we use the AI Agent MCP server [Google Maps MCP Servers](https://www.deepnlp.org/store/mcp-server/map/pub-google-maps/google-maps) as example. 

The unique_id should follow the same /{owerid}/{item-id} format

```
{
  "unique_id": "google-maps/google-maps",
  "content_name": "Google Maps MCPs",
  "content": "Google Maps MCPs provides Location Service to support various APIs..."  
  "category": "Map",
  "field": "MCP SERVER",
  "subfield": "Map",
  "website": "maps.google.com",
  "content_tag_list": "official,maps,location",
  "github": "https://github.com/modelcontextprotocol/servers/tree/main/src/google-maps"
}
```

### NodeJs
See the document for node CLI wrapper at [NPM Agtm package](https://github.com/aiagenta2z/agtm)


