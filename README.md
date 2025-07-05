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

👉 [**LSTM vs GPT-2 for Personalized Chatbots** on LinkedIn](https://www.linkedin.com/in/debkumar-baksi)  
(*Replace the link with the actual article URL when published*)

## 🛠️ Tech Stack

| Component      | Details                         |
|----------------|----------------------------------|
| Framework      | PyTorch, Hugging Face Transformers |
| Model 1        | Custom Char-Level LSTM           |
| Model 2        | GPT-2 (117M parameters)           |
| Training       | CPU-only, ~30–300 mins           |
| Language Style | Bengali in Roman script          |
| Input Format   | `Me: ...` + `Her: ...`           |

## 📂 Project Structure

├── data/
│ └── whatsapp_chat.txt # Raw exported chat
│ └── new_chat_data.txt # Cleaned & formatted
├── lstm_model.py # Char-level LSTM model
├── train_lstm.py # LSTM training script
├── generate_lstm.py # LSTM-based generator
├── gpt2_finetune.py # GPT-2 fine-tuning script
├── chat_lstm_model.pth # Saved LSTM weights
├── README.md


## 🧪 Example Output

### Prompt
```
Me: tumi porcho?
Her:
```


### LSTM Output
```
Her: ki krbo
Her: ki krbo
Her: ki krbo
```


### GPT-2 Output
```
Her: ha porchi. Tui bol ki korchish?
```

## 🚀 How to Run (LSTM Version)

1. Clone the repo:
   ```bash
   git clone https://github.com/yourusername/chat-with-best-friend.git
   cd chat-with-best-friend
2. Install requirements:

```
pip install torch tqdm
```
3. Train:
```
python train_lstm.py
```
4. Generate:
```
python generate_lstm.py
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