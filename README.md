# Compress MobileNet V1 and V2 using tools from NNI
We give an end-to-end demo of compressing MobileNetV2 for finegrained classification using NNI Pruners. Although MobileNetV2 is already a highly optimized architecture, we show that we can further reduce its size by over 50% with more than 96% performance retained using iterative pruning and knowledge distillation. To similate a real usage scenario, we use the Stanford Dogs dataset as the target task. Please find the results, insights, and detailed explanations in the jupyter notebook `Compressing MobileNetV2 with NNI Pruners.ipynb`. 

![results](final_performance.png)

### Preparation
```
pip install -r requirements.txt
chmod u+x prepare_data.sh
./prepare_data.sh
```

### Pretraining
```
python3 pretrain.py
```

### Experiment with pruning
```
python3 pruning_experiments.py [arguments]
```
