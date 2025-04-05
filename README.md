**What is Cross Entropy?**
Cross-entropy measures the difference between two probability distributions:

The true distribution (what should happen — your labels)

The predicted distribution (what the model thinks will happen)

It answers:

"How surprised is the model by the actual result?"

Less surprise = lower cross-entropy = better predictions In the context of NLP / summarization: For every token the model generates (e.g., a word or subword), it predicts a probability distribution over the entire vocabulary.

Example: Vocabulary = [dog, cat, bird, food]

Actual next word: "cat" → [0, 1, 0, 0] (true one-hot distribution)

Model predicts: [0.2, 0.5, 0.2, 0.1]

Cross-entropy measures how far [0.2, 0.5, 0.2, 0.1] is from [0, 1, 0, 0].


**Why convert data into a PyTorch Dataset?**
Because PyTorch models (and Hugging Face's Trainer) expect data to come from a Dataset or DataLoader during training.

**What is T5 (Text-to-Text Transfer Transformer)**
t%is a language model developed by Google that treats every NLP task as a text-to-text problem. 
It uses a Transformer-based encoder-decoder architecture, similar to models like BART and PEGASUS. 
T5 is pretrained on a large corpus (C4) using a masked span prediction objective. 
It can be used for tasks like summarization, translation, classification, and question answering with just text prompts. 
T5 comes in multiple sizes (t5-small, t5-base, t5-large, etc.), making it flexible for both speed and accuracy.
