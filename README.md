# LUFFY Development Repository

> 🚧 **Development Branch** - This is the main development repository
⚠️ **Note**: This development version has incomplete implementations. Many features are marked as TODO and need to be completed before production use.

```bash
# Clone the repository
git clone <repository-url>
cd LUFFY

# Install dependencies
pip install -r luffy/requirements.txt

# Note: Some functionality is incomplete - check TODO list below for details
```

## 📁 Repository Structure

```
LUFFY/
├── luffy/                 # Core framework
│   ├── deepscaler/        # Scaling utilities (⚠️ API integration needed)
│   ├── verl/              # RL training components (⚠️ Some features incomplete)
│   └── ...
├── data/                  # Training data and scripts
├── eval_scripts/          # Evaluation utilities
├── exp_scripts/           # Experiment scripts
└── README.md              # This file
```

## ⚠️ Development Notes

- This is a **development version** with incomplete implementations
- Many functions contain TODO markers indicating pending work
- ✅ OpenAI API integration completed (placeholder implementation replaced with full client + retry logic)
- Gemini API integration still needs completion
- FSDP and distributed training features need completion
- ✅ Data processing batch dimension operations completed (fold/unfold batch dim fully implemented)


### 🔴 High Priority TODOs

- ✅ **API Integration**: OpenAI API implementation completed (with exponential backoff retry logic)
  * Remaining: Gemini API implementation, logging improvements, batch processing optimizations
- **Reward System**: Parallel processing and validation for reward computation  
- **FSDP Training**: Model loading and distributed training setup
- ✅ **Data Processing**: Batch dimension operations (fold_batch_dim/unfold_batch_dim) completed
  * Remaining: Additional optimization improvements for batch handling