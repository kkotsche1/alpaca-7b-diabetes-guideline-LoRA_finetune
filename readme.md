This is a lora finetune of the Alpaca 7B model on clinical guidelines for diabetes.

The finetune was completed using the following lora parameters:

LORA_R = 4 </br>
LORA_ALPHA = 16</br>
LORA_DROPOUT = 0.05</br>

config = LoraConfig(</br>
r=LORA_R,</br>
lora_alpha=LORA_ALPHA,</br>
target_modules=["q_proj", "v_proj"],</br>
lora_dropout=LORA_DROPOUT,</br>
bias="none",</br>
task_type="CAUSAL_LM",</br>
)</br>

Training was done over 2 epochs on free form text obtained from the AWMF clinical guidelines for diabetes.

Disclaimer: As this is a finetune of an Alpaca model, these weights should be used for non-commercial and research purposes only. Please refer to the Alpaca license for more information.
