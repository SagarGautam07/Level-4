# Level-4
Chatting prediction bot
# Model link- https://drive.google.com/file/d/1hyoJRZybrUHQB8NqF3xk5bTNyWYkW_2R/view?usp=drive_link

Offline Chat-Reply Recommendation System (GPT-2)

Contents
- ChatRec_Model.ipynb: End-to-end pipeline (Excel loader, preprocess, tokenize, train GPT-2 offline, generate, evaluate, save).
- Model.joblib: Serialized wrapper saved after training (placeholder until you run the notebook).
- Report.pdf: Short report of results (now includes a template to fill after running).

Quick Start (Windows, CPU)
1) Open PowerShell in this folder.
2) Create/activate a venv (optional but recommended):
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
3) Install dependencies:
   pip install transformers==4.44.2 numpy pandas scikit-learn matplotlib nltk joblib
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cpu
4) Place conversationfile.xlsx in this folder.
5) Launch Jupyter:
   python -m notebook
6) Open ChatRec_Model.ipynb and run all cells top-to-bottom.

Outputs
- gpt2_chatrec_output/: fine-tuned model and tokenizer
- Model.joblib: inference wrapper for offline generation
- Report.pdf: fill in metrics (BLEU/ROUGE/Perplexity) after running

Notes
- If you have a CUDA GPU and drivers installed, you can install a CUDA build of PyTorch from PyTorch’s site and the notebook will auto-use GPU.
- Adjust MAX_CONTEXT_TURNS and MAX_SEQ_LEN in Config for memory/performance.
- For longer training, increase NUM_EPOCHS and consider larger batches if GPU is available.

