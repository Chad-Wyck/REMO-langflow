# REMO-langflow
GPT-4 and the [REMO memory system](https://github.com/daveshap/REMO_Framework) are combined to create a highly intelligent chatbot with a long-term memory. This provides an easy way to interface with it using [LangFlow](https://github.com/logspace-ai/langflow).

This is not a complete or ideal implementation. Feel free to improve upon it or use it to better understand the tech it uses.

## How to use
- Launch REMO
- Launch langflow and import the json from this repo
- Put in your OpenAI key in the ChatOpenAI node on the left
- Chat...

It will save the information you give it (`add_message`), but you need to tell it to "organize memories" (`maintain_tree`) to put those new memories in the place where the retrieval function (`search`) can find them. Ideally this would be automatically triggered, but for the purposes of testing, I've not done this. You can trigger a rebuild of its memory tree `rebuild_tree` by saying "rebuild tree". 


![image](https://user-images.githubusercontent.com/123516285/232272096-23763e8a-9f44-446a-80c9-ea4a696bb0b5.png)

## Implemented
- Saving memories
- Finding memories
- Organizing memories (must be called for new memories to be retrievable)
- Rebuilding memory tree (Useful to trigger when it returns incomplete or incorrect information)
