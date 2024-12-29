
## testing environment
```
pip install -r requirements.txt
```

Before running the code, you should download the weight(https://pan.baidu.com/s/1X258SeUnEfmB4wvGwV1nQg 

) file. And put this file in logs/. 
Extracted code:wqcy


## Modify model config

Enter models/wide_resnet/wide_resnet50.py
```
    test=dict(
        ckpt = 'your weight path',
        metrics = ['accuracy', 'precision', 'recall', 'f1_score', 'confusion'],
        metric_options = dict(
            topk = (1,5),
            thrs = None,
            average_mode='none'
```


## Running this code
```
python tools/single_test.py "your img path" "your model path"
```


