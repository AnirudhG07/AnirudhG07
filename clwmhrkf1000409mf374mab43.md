---
title: "Terminal GPT and AI"
seoTitle: "Terminal GPT and AI Overview"
seoDescription: "Use AI tools in Terminal like Terminal GPT, aichat, Amazon Q, and Warp Terminal Emulator to boost developer productivity with advanced terminal features."
datePublished: Sat May 25 2024 19:16:16 GMT+0000 (Coordinated Universal Time)
cuid: clwmhrkf1000409mf374mab43
slug: terminal-gpt-and-ai
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716654436764/0201e538-b077-4a00-b20a-af2c93b5fda8.png
tags: ai, terminal, terminal-ai, terminal-gpt, ai-in-terminal

---

In today's advancing world, the hot topic going on is "AI". Everyday, we use ChatGPT, Gemini, Llama, Github Copilot, etc. for our everyday purposes. For code writers, they may feel Github Copilot, OpenAI's gpt-3.5-turbo, gpt-4 are life saviours. These models give you code suggestions, solutions to any problem, code autocompletion(in case of Github Copilot), etc. which speeds up your work, hence increasing your productivity.

But as a developer, going to the web for asking AI seems time taking which might be annoying, especially for Vim/NeoVim users who don't want to wait for even VS code to open(no offence, kidding). Woudn't it be great to have an inbuit AI chat bot which can do the following-

* Writes the shell command based on your prompt
    
* The usual ChatGPT, Gemini, etc. functionality in chat
    
* Creating Images within the Terminal for your prompt
    
* and all this for Free, or atleast your API key
    

Well good news as there are various tools today for your Terminal to upgrade!

# Terminal Tools

## 1\. Terminal GPT (tgpt)

This is an amazing cross platform Terminal AI tool (Visit: [https://github.com/aandrew-me/tgpt](https://github.com/aandrew-me/tgpt)) which solves all of the above requirements. It is super fast, easy to use, very interactive, provides keyboard keybindings for copying text and code(don't have to use mouse, how cool is that!) and it let's you use not only gpt and llama2, but many more models configured.

You can enter into a regular interactive mode using-

```bash
tgpt -i
```

This will create an interactive mode where you can ask your doubts and get solutions, including codes. Although you won't be able to prompt your code here.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716647865670/e032ff7f-d3bb-4aa5-9181-8ac13e8ac4af.png align="center")

But this has another functionality which let's you have multi line functionality and prompt codes to specify which part you are facing problems in.

```bash
tgpt -m
```

This let's you copy code with b, and copy the whole reponse with c, no mouse needed at all! ( A plus point for non-mouse developers)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716648220475/c6dc7979-5325-4358-b3c7-848e91e68764.png align="center")

You can create images with `tgpt -img "make a human sketch"`. Get shell scripts to run for your prompt using-

```bash
tgpt -s "echo hi in blue colour"    
# response:
# echo -e "\033[34mhi\033[0m"
# Execute shell command? [y/n]:
```

The default AI model set is Phind AI, but you can always chat with other models with suitable provider name, model and API key. Some of the models used are-

1. openai - Needs API key to work and supports various models. Recognizes the OPENAI\_API\_KEY and OPENAI\_MODEL environment variables.
    
2. opengpts - Uses gpt-3.5-turbo.
    
3. phind - Uses Phind Model. Great for developers.
    
4. llama2 - Llama 2 is an open source large language model (LLM) developed by Meta AI. Uses llama2-70b by default. Supports other models too.
    
5. groq - Requires a free API Key. Supports LLaMA2-70b & Mixtral-8x7b.
    
    and many more...
    

Thus having Terminal GPT in hand can increase your workflow super fast while staying in your dev environment.

### Pros

* Various AI models can be used here for chat
    
* translate to shell codes and creates images
    
* No mouse needed usually
    

### Cons

* No inbuilt terminal shortcuts, although you can create a customised aliases
    
* Internet needed for accessing AI models
    

## 2\. Aichat

`aichat` is a CLI chat and copilot tool that connects to over 20 well-known AI LLM models and platforms.

It supports a variety of models including GPT-3.5 / GPT-4, Gemini models: (Gemini-1.0 / Gemini-1.5), Claude: Claude-3, Mistral, Cohere, Perplexity, Groq and more.

Moreover, it also includes `context-aware conversations`, `image analysis`, being an code assistant for pair programming, shell integration + shell auto-completion.

aichat has many commands and a REPL for chatting with LLM models and is worth a look if you're searching for an AI copilot tool suited for the terminal.

```bash
All-in-one AI CLI Tool

Usage: aichat [OPTIONS] [TEXT]...

Arguments:
  [TEXT]...  Input text

Options:
  -m, --model <MODEL>        Select a LLM model
      --prompt <PROMPT>      Use the system prompt
  -r, --role <ROLE>          Select a role
  -s, --session [<SESSION>]  Start or join a session
      --save-session         Forces the session to be saved
      --serve [<ADDRESS>]    Serve the LLM API and WebAPP
  -e, --execute              Execute commands in natural language
  -c, --code                 Output code only
  -f, --file <FILE>          Include files with the message
  -H, --no-highlight         Turn off syntax highlighting
  -S, --no-stream            Turns off stream mode
  -w, --wrap <WRAP>          Control text wrapping (no, auto, <max-width>)
      --light-theme          Use light theme
      --dry-run              Display the message without sending it
      --info                 Display information
      --list-models          List all available models
      --list-roles           List all available roles
      --list-sessions        List all available sessions
  -h, --help                 Print help
  -V, --version              Print version
```

This is really powerful tool with all types of AI configurations for you. This is a must for any developer hoping to use AI in there.

Visit: [https://github.com/sigoden/aichat](https://github.com/sigoden/aichat) for official documentation

### Pros

* Lot's of AI model configurations with aichat
    
* shell integrations and shell auto-completeltions present
    
* Image analysis also available
    
* You can set different roles for AI to behave, which is very unique and useful
    

### Cons

* Doesn't provide keyboard shortcuts of copying codes
    
* Internet is needed for accessing models
    

## 3\. Ollama

For running Ollama, there are various tools featured which are really easy to use.

* Ollama: [https://ollama.com/](https://ollama.com/)
    
* oterm: [https://terminaltrove.com/oterm/](https://terminaltrove.com/oterm/)
    
* osh: [https://github.com/charyan/osh](https://github.com/charyan/osh)
    

**Ollama** is a CLI aimed at simplifying the deployment and management of software applications. It offers a straightforward interface for tasks such as configuration, deployment, and monitoring, making it accessible for both beginners and experienced developers.

To run llama2 and ollama, you can use TerminalGPT or even create your own tool.

## 4\. ChatGPT Tui's

There are various TUI's made for accessing ChatGPT and openai gpt's. These are-

* elia: [https://github.com/darrenburns/elia](https://github.com/darrenburns/elia)
    
* cligpt: [https://github.com/paij0se/cligpt](https://github.com/paij0se/cligpt)
    
* gpterm: [https://github.com/MakisChristou/gpterm](https://github.com/MakisChristou/gpterm)
    
* Ai: [https://github.com/nitefood/ai-bash-gpt](https://github.com/nitefood/ai-bash-gpt)
    
* chatgpt: [https://github.com/mglantz/chatgpt](https://github.com/mglantz/chatgpt)
    
* Chatblade: [https://github.com/npiv/chatblade](https://github.com/npiv/chatblade)
    
    and more...
    

These Tools are specific for gpt's and for ChatGPT lovers, these tools are great options to pick from.

# Softwares for Terminal

## 1\. Amazon Q

Another amazing tool for terminal is Amazon Q. This is MacOS only software which unlike tgpt, provides more functionalities than just generating shell codes like giving you autocompletion plugin and keybindings for inbuilt features.

Great thing about this software is the use of aliases for calling the AI within the shell. The general command without using the special aliases goes like -

```bash
q translate "your-prompt" # for shell codes
q chat # for opening chat
# and more commands
```

But like Warp, this provides a comment based shell code translator.

```bash
# echo hi in blue
```

This is automatically converted to `q translate "echo hi in blue"` and provides more options like -

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716649702732/4e811282-cb51-4945-b37f-fa74dd820e04.png align="center")

Another good thing about Amazon Q you can mention git and environment settings easily in chat mode to get appropriate responses, unlike web server models where you will have to explain the whole package.

### Pros

* In built convenient aliases for calling Amazon Q
    
* Gives you autocomplete feature within shell and more
    
* Can be used without internet connection
    

### Cons

* You cannot copy code directly without selecting it
    
* Does not provide other AI model functionalities
    

Honestly I would say having tgpt and Amazon Q are both great! Both have great features and both will improve AI functionalities of your terminal to the next level!

## 2\. Warp Terminal Emulator

Warp is a powerful tool designed to enhance productivity and efficiency in software development. It integrates advanced AI capabilities to provide developers with intelligent features such as code completion, bug detection, and performance optimization suggestions.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657832678/8462ddcf-10cf-4547-bf78-424d962181c2.png align="center")

By leveraging machine learning algorithms, Warp can understand the context of your code better than traditional tools, offering more accurate and relevant suggestions. This not only speeds up the development process but also helps in maintaining high-quality code standards. It is just the ideal AI based Terminal Emulator you need.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1716657909105/048f6c32-f4fe-48b9-82f3-c736947e6773.png align="center")

### Pros

* Inbuilt AI chat and shell code translator with just push of a button
    
* Really good looking with modern themes
    
* Great features for blocks and splitting panes
    
* Good combination of keybindings for fast workpace
    
* Autocompletion and suggestions
    

### Cons

* Zsh keybindings (like fzf) might mess up, although it provides its own inbuilt functionality for that, but changing it according to you might be a pain.
    

Although for those who are new to vim, tmux, window tiling managers, etc. (you know...), Warp is best for them because it already provides most of these functionalities inbuilt but in it's own way, which is very fast and convenient.

# Other tools

There are various more tools present for having AI in terminal. Developers have made their own TUI's for chatGPT within the terminal, which you can view in Github repositories. One can create their own terminal user interface tool for getting the outputs in the terminal of any AI model.

# Summary

In this article, we explore various AI tools designed to enhance productivity directly within the terminal, eliminating the need to switch to web-based AI solutions. Key tools discussed include Terminal GPT (tgpt), Aichat, Ollama, and several ChatGPT TUIs, each offering unique functionalities like code suggestions, shell command generation, and image creation. Additionally, we highlight Amazon Q and Warp Terminal Emulator for their advanced features like autocompletion and intelligent code assistance. These tools cater to developers seeking efficient, integrated AI solutions within their development environment.