# Medic_bot

<div align = "left" >

**Prerequisite**: Gradio requires [Python 3.8 or higher](https://www.python.org/downloads/)
```
pip install python 3.8
```

We recommend installing Gradio using `pip`, which is included by default in Python. Run this in your terminal or command prompt:

```
pip install gradio
```
### Sharing Your Demo

What good is a beautiful demo if you can't share it? Gradio lets you easily share a machine learning demo without having to worry about the hassle of hosting on a web server. Simply set `share=True` in `launch()`, and a publicly accessible URL will be created for your demo. Let's revisit our example demo,  but change the last line as follows:

```python
import gradio as gr

with gr.Blocks() as demo:
   global messages
   health_condition = gr.Dropdown(["BP","FEVER","TYROIDE","SUGAR"],label = "health_condition")
   severity_condition = gr.Dropdown(["minor","moderate","major","extreme"],label = "severity_condition")
   chatbot = gr.Chatbot()
   msg = gr.Textbox()
   clear = gr.Button("Clear")
    
demo.launch(share=True)  # Share your demo with just 1 extra parameter 🚀
```

When you run this code, a public URL will be generated for your demo in a matter of seconds, something like:

👉 &nbsp; `https://a23dsf231adb.gradio.live`

Now, anyone around the world can try your Gradio demo from their browser, while the machine learning model and all computation continues to run locally on your computer.

To learn more about sharing your demo, read our dedicated guide on [sharing your Gradio application](https://www.gradio.app/guides/sharing-your-app).


### An Overview of Gradio

So far, we've been discussing the `Interface` class, which is a high-level class that lets to build demos quickly with Gradio. But what else does Gradio do?

#### Chatbots with `gr.ChatInterface`
<img src="https://github.com/Dhinesh-Kumar8/Medic_bot/blob/main/gif/demo(1).gif" style="padding-bottom: 10px">
<br></br>
Gradio includes another high-level class, `gr.ChatInterface`, which is specifically designed to create Chatbot UIs. Similar to `Interface`, you supply a function and Gradio creates a fully working Chatbot UI. If you're interested in creating a chatbot, you can jump straight [our dedicated guide on `gr.ChatInterface`](https://www.gradio.app/guides/creating-a-chatbot-fast).
<br></br>
<img src="https://github.com/Dhinesh-Kumar8/Medic_bot/blob/main/gif/demo(2).gif" style="padding-bottom: 10px">
