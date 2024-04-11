This project demonstrates how to fine tune a pre-trained LLM model on custom data

We will fine tune the Phi-2 LLM model by Microsoft.

There are two ways to fine tune a LLM model
1) Full fine tuning (also called Instruction Fine Tuning)
   This updates all the model weights and requires substantial time and compute power. It could also result in "catastrophic failure" if we are not careful

2) PEFT (Performance Efficient Fine Tuning)
     This is a modular approach wherein we don't touch the weight of the original model
     We use LoRA (Low Rank Adaptation) technique or the more optimized version called QLoRA (Quantized LoRA) to train two matrices, the dot product of which approximates the original pre-trained weight matrix.
     The two sub-matrices is called "LoRA adapter".
     At inference time the LoRA adapter along with the original pre-trained model weights is used to reach the inference.
