
# 🧠 Chat with My Best Friend — Custom Chatbot Using LSTM and GPT-2

A personalized chatbot that mimics my best friend's style using exported WhatsApp chats.  
Two parallel approaches explored:
- A character-level **LSTM** model (built from scratch using PyTorch)
- A fine-tuned **GPT-2** model (using Hugging Face Transformers)

## 📌 Project Highlights

- Dataset: 250KB of exported WhatsApp chat in transliterated Bengali (`tui kemon achhis?`)
- Preprocessing: Cleaned timestamps, formatted dialogues, removed media tags
- Training:
  - LSTM: 2-layer, 64–128 hidden units, ~30 mins CPU training
  - GPT-2: Fine-tuned on full dataset, ~5 hours CPU training
- Generation: Prompt-based responses using character decoding (LSTM) and BPE sampling (GPT-2)

## 📖 Read the Technical Comparison Article

👉 [**LSTM vs GPT-2 for Personalized Chatbots** on LinkedIn](https://www.linkedin.com/posts/debkumar-baksi-269738279_machinelearning-nlp-llm-activity-7347277817748836352-ulfv?utm_source=social_share_send&utm_medium=member_desktop_web&rcm=ACoAAEPrDnEBVjAz3BltRhVC2Ye2Hln8TZTZw70)  


## 🛠️ Tech Stack

| Component      | Details                         |
|----------------|----------------------------------|
| Framework      | PyTorch, Hugging Face Transformers |
| Model 1        | Custom Char-Level LSTM           |
| Model 2        | GPT-2 (117M parameters)           |
| Training       | CPU-only, ~30–300 mins           |
| Language Style | Bengali in Roman script          |
| Input Format   | `Me: ...` + `Her: ...`           |


## 🧪 Example Output

### Prompt
```
Me: Ki korchhis re?
```


### LSTM Output
```
Her: 🙂🙂🙂🙂byoum
Her: amdr
Me: Mondr kore ni
Me: upch ker 6e n
Her: kal lab lag6er
Herr: saruu
Her: Kame jbo onek diye
Me: Oito hoye6lin?
Her: Amke
Her: Miss
Me: Ami aubha
Her: poc korechhis?
Me: Ei nijekh
Me: 🤣🤣🤣🤣...j to join oble
Her: au kisr
Her: Bhai to jbi kalke e krbe softa ta
Me: indic e to bollo
M
```


### GPT-2 Output
```
Her: korchis
```

## 🚀 How to Run (LSTM Version)

1. Clone the repo:
   ```bash
   https://github.com/Debkumar-Baksi/Building-a-Personalized-Chatbot-LSTM-vs.-Fine-Tuned-LLM-GPT-2.git
   cd Building-a-Personalized-Chatbot-LSTM-vs.-Fine-Tuned-LLM-GPT-2
2. Install requirements:

```
pip install torch tqdm
```
3. Run:
```
python clone_friend.ipynb
```
## 💡 Future Work
Word-level LSTM with embeddings

Fine-tune multilingual LLMs (e.g., IndicBERT, BanglaGPT)

Deploy using Gradio

Quantized GPT-2 for mobile use

## 🤝 Author
Debkumar Baksi
BTech CSE | Python Developer | AI Enthusiast
LinkedIn
