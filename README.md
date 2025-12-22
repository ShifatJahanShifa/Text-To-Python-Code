Folder Structure:   

Text-To-Python-Code/     
│       
├── data/   
│   ├── raw/       
│   │   └── codesearchnet_python.jsonl   # optional (cached or downloaded)       
│   │      
│   ├── processed/      
│   │   ├── train.pt     
│   │   ├── val.pt     
│   │   ├── test.pt      
│   │   └── vocab.pkl     
│      
├── models/        
│   ├── __init__.py       
│   │       
│   ├── encoder.py        # RNN / LSTM / BiLSTM encoders        
│   ├── decoder.py        # RNN / LSTM decoders         
│   ├── attention.py      # Bahdanau attention                
│   ├── seq2seq.py        # Full Seq2Seq wrappers      
│        
├── training/         
│   ├── train.py          # Training loop (shared)       
│   ├── evaluate.py       # BLEU, accuracy, exact match         
│   └── utils.py          # teacher forcing, masks, helpers      
│         
├── experiments/         
│   ├── rnn_baseline/        
│   │   ├── config.yaml        
│   │   ├── loss.png          
│   │   └── model.pt       
│   │      
│   ├── lstm/          
│   │   ├── config.yaml         
│   │   ├── loss.png         
│   │   └── model.pt       
│   │         
│   └── attention/         
│       ├── config.yaml          
│       ├── loss.png           
│       ├── model.pt         
│       └── attention_weights/          
│           ├── ex1.npy         
│           ├── ex2.npy          
│           └── ex3.npy            
│       
├── visualization/        
│   ├── plot_loss.py        
│   ├── plot_attention.py           
│   └── attention_heatmaps/            
│       ├── ex1.png           
│       ├── ex2.png             
│       └── ex3.png            
│        
├── scripts/        
│   ├── download_data.py           
│   ├── preprocess.py           
│   └── build_vocab.py         
│           
├── report/    
│   ├── figures/        
│   │   ├── loss_curves.png         
│   │   ├── bleu_scores.png         
│   │   └── attention_example.png          
│   │          
│   └── report.pdf          
│           
├── README.md            
├── requirements.txt             
└── main.py          
