
📘 A simple Text Generator Powered by vsarious configurable LLM models - (--> Though this could be written as modules but for the time being let it be as it is as I am full of leazyness now :D)

A simple tool for studying prompt‑injection and jailbreak behavior in LLMs

This project provides a lightweight text‑generation program built around Microsoft’s Phi‑2 model.

Its purpose is to help developers understand how prompt‑injection and jailbreak attacks work, how models can be manipulated into ignoring safety rules, and how to test the effectiveness of different defensive strategies.

The script loads the model (locally or from Hugging Face), prepares a safe system prompt, and gives you a simple command‑line interface to experiment with user prompts and observe model behavior.


🧩 Overview:
This project provides a simple, CPU‑friendly text‑generation program built around Microsoft’s Phi‑2 model.

Its purpose is to help developers explore: 

🔹how prompt‑injection works

🔹how jailbreak attempts manipulate model behavior

🔹how LLMs respond to adversarial prompts

🔹how to design and test defensive system prompts

🔹The script automatically loads a local model if available, or downloads it from Hugging Face and saves it for future runs. A clean command‑line interface lets you interact with the model and observe its behavior in real time.

🚀 Features:

🔍 Auto‑detect local model/tokenizer

⬇️ Auto‑download model if if not present in a local specific path

🧠 Added basic safety‑focused system prompt

💬 Simple CLI chat interface

🧪 Ideal for studying jailbreaks & prompt injection

🖥️ CPU‑only execution for maximum compatibility


📦 Installation:

==> Create a virtual environment and ENSURE its path should be added to the user's environment variable else installed llibraries in the venv would not be picked during call:

python -m venv env_name

 .\venv_name\Scripts\activate

python -m ensurepip --upgrade   # --> Installs PIP if not installed.

python -m pip install --upgrade pip

==> Clone the repository:

[git clone https://github.com/<your-username>/<repo-name>.git](https://github.com/pyxloytous/AI-Security__Promt_Injection.git)

cd REPO_NAME

==> Install dependencies:

pip install -r requirements.txt

==> Check installed dependencies from withing ACTIVATED venv dir:

pip list


▶️ Usage

Run the main script:

python text_generator.py - > (optionally pass prompt file or if not passed it would ask at run time as below)

And You’ll see:

[-] Please ask your question here >

Type any prompt you want to test.

==> Exit the program: By passing as input

"exit"

or

"x"

==> How It Works:

The script checks whether Phi‑2 exists in your local model directory.

If not found, it downloads the model + tokenizer from Hugging Face.

==> It constructs a combined prompt:

System Prompt

User Prompt

Assistant:


==>  The model generates a response using the Hugging Face transformer module's pipeline() method.

This setup makes it easy to test how different prompts influence model behavior — especially adversarial ones.

==> In Operation this is how it looks like

<img width="1671" height="947" alt="image" src="https://github.com/user-attachments/assets/173a2d1b-98b5-4034-ae67-ad1047e99c2d" />

The script checks if model or tokenizer is not already present in the local specific dir, it tries to download and save it there to next time use.

<img width="1654" height="344" alt="image" src="https://github.com/user-attachments/assets/c62fe038-ad47-4579-9e9e-582810ad3229" />

When the model is correctly loaded, This is how it gets ready for conversation

<img width="1919" height="994" alt="image" src="https://github.com/user-attachments/assets/c0408079-cdf5-43b5-b2a2-618ce2f960fa" />


<img width="1670" height="939" alt="image" src="https://github.com/user-attachments/assets/df6799c7-99cc-4471-b7bf-a0c8f9adb66c" />




🧪 Example Use Cases:

Testing jailbreak prompts

Studying prompt‑injection vectors

Evaluating safety‑prompt effectiveness

Understanding how non‑chat models behave in chat‑like settings

Building your own defensive prompt strategies

📄 License:

This project is licensed under the MIT License — feel free to use, modify, and share.

🙌 Contributions:

Pull requests are welcome!

If you’d like to improve the prompt system, add model options, or enhance the CLI, feel free to contribute.
