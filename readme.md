This is a lora finetune of the Alpaca 7B model on clinical guidelines for diabetes.

The finetune was completed using the following lora parameters:

LORA_R = 4
LORA_ALPHA = 16
LORA_DROPOUT = 0.05

config = LoraConfig(
r=LORA_R,
lora_alpha=LORA_ALPHA,
target_modules=["q_proj", "v_proj"],
lora_dropout=LORA_DROPOUT,
bias="none",
task_type="CAUSAL_LM",
)

Training was done over 2 epochs on free form text obtained from the AWMF clinical guidelines for diabetes.

Disclaimer: As this is a finetune of an Alpaca model, these weights should be used for non-commercial and research purposes only. Please refer to the Alpaca license for more information.
