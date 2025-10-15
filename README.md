# Yuktha-Langgraph--MAT496  
# MODULE 1  

**video** 1- The video describes how traditional language model workflows, known as chains, are dependable but tend to be too fixed in structure. LangGraph was developed to add more flexibility, giving developers the ability to set the stable parts of a process while allowing the language model to make dynamic decisions. This makes it easier to create AI agents that are both intelligent and adaptable.  

**video** 2- Learnt how to create simple graphs in LangGraph, which consists defining states, nodes, conditional edges, constructing graph, visualizing it and graph invocation.  
Changes made: Added "My Examples" section towards the end where I implemented my own graph example.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/simple_graph%20(1).ipynb  

**video** 3- Learnt how to setup and run LangGraph Studio on device and in the studio and learnt how to use the UI to input a graph state, see the thread for the dataflow of the graph  
Changes made: I chose to use Groq as the client, so I had to install some extra dependencies during the setup. After setting up the environment, I created a .env file to store my Groq and Langsmith API keys. I also updated the code in router.py and agent.py (found in the /studio folder) by replacing ChatOpenAI() with ChatGroq() so the tools would work correctly with the Groq client.  

**video 4**- Learnt how to use chat messages as our graph state, chat models as graph nodes, binding tools to the model and executing tool calls in graph nodes.  
Changes made: Used Groq's "openai/gpt-oss-120b" model instead of OpenAI, implemented my own tool calling example at the end  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/chain.ipynb

**video 5**- Learnt about the concept of a router agent, where the chat model decides whether to respond directly or call a tool based on the user's input. Focused on how the LLM manages control flow - choosing between tool execution and generating a natural language reply.  
Changes made: Used Groq’s "openai/gpt-oss-120b" model. At the end, implemented my own graph and included screenshots from LangGraph Studio to show the flow visualization.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/router.ipynb  

**video 6** - I learned about agentic architecture, where the system can return a ToolMessage to the LLM, allowing it to either make another tool call or generate a direct response. I also explored how LangSmith provides detailed traceability of the entire conversation flow.  
Changes made: used Groq’s "openai/gpt-oss-120b" model, created a custom agent example, and included screenshots of the LangSmith traces    
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/agent.ipynb  
