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

**video 7** - Learned how agents can retain past data using memory through persistence, where a checkpointer is used to automatically save the graph's state after each step.  
Changes made: Used Groq’s "openai/gpt-oss-120b" model, built a custom agent with memory example, and included screenshots of the LangGraph Studio implementation  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/agent_memory.ipynb  

**video 8** - Learned how to deploy the Graph models both locally to LangGraph Studio and to LangGraph Cloud, enabling easy testing and sharing of the implemented workflows.  
Code for local deployment: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/Module%201/deployment.ipynb  
(Deployment on LangGraph Cloud is a paid feature)  

# MODULE 2  

video 1- Learnt how to define state schemas in LangGraph using three different methods: TypedDict, dataclass, and Pydantic. Each method provides a way to structure the data used in the graph's state. Learnt how these schemas help manage and update the state as the graph runs. I also noticed that Pydantic stands out because it offers built-in runtime validation, which the other two don’t provide by default.  
Changes made: Added own examples towards the end of the source code.
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/MODULE%202/state_schema%20(1).ipynb  

video 2- Learnt how LangGraph manages state updates, branching,usage and working of reducers and specially custom reducers like operator.add and custom functions to handle concurrent updates and data types like lists and messages. This allows for robust state management in graphs with branching logic.  
Changes made: Added 'own examples' section towards the end of the source code for the concepts covered.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/MODULE%202/state_reducers%20(1).ipynb  

video 3- Learnt how to use private state in LangGraph to manage intermediate data that is not needed in the final output. We also saw how a single overall schema includes all state information in both input and output. Finally, we explored using explicit input and output schemas to filter data entering and leaving the graph.  
Changes made: Added own examples towards the end of the source code.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/MODULE%202/multiple_schemas.ipynb  

video 4- Learnt how to manage message history in LangGraph using several techniques. These include reducing the number of messages, filtering to keep only certain messages, and trimming based on token limits. I understand how important it is to manage the conversation history properly to make chatbots more efficient and context-aware. By controlling what part of the conversation is sent to the language model, we can improve performance and save resources.   
Changes made: Added own examples at the end of the source code to implement my understanding of the concepts.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/MODULE%202/trim_filter_messages.ipynb   

video 5- Learnt how to build a chatbot using LangGraph that keeps conversations short by summarizing previous messages. It also showed me how to give the chatbot memory by using LangGraph's built-in persistence feature with thread IDs. This helps the bot remember past interactions even if the conversation gets long.  
Changes made: Added own examples at the end of the source code to implement my understanding of the concepts.  
Tweaked code: https://github.com/Y-kz918/Yuktha-Langgraph-MAT496/blob/main/MODULE%202/chatbot_summarization.ipynb  

video 6- 


