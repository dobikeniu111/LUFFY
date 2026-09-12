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


### 📝 Complete TODO List

#### 🔴 High Priority TODOs (Ordered by file path ascending, line numbers increasing)

##### eval_scripts/oat_math_grader.py
- ⚠️ HACK: ing. (line 1023)
- ⚠️ HACK: ing. (line 1048)
- ⚠️ HACK: ing. (line 1075)

##### luffy/deepscaler/utils.py
- ⏳ TODO: Add logging for API calls and errors (line 45)
- ⏳ TODO: Support batch processing for multiple prompts (line 46)
- ⏳ TODO: Add timeout configuration for API calls (line 47)
- ⏳ TODO: Implement Vertex AI initialization and authentication (line 107)
- ⏳ TODO: Configure safety settings for content generation (line 108)
- ⏳ TODO: Set up GenerativeModel with proper system instructions (line 109)
- ⏳ TODO: Implement retry logic with exponential backoff (line 110)
- ⏳ TODO: Add comprehensive error handling for API access issues (line 111)
- ⏳ TODO: Handle rate limiting and quota management (line 112)
- ⏳ TODO: Implement response validation and text extraction (line 113)
- ⏳ TODO: Add support for different generation configurations (line 114)

##### luffy/test.py
- ⏳ TODO: add smaller page sizes when https://github.com/Dao-AILab/flash-attention/pull/824 is merged (line 1590)

##### luffy/verl/verl/protocol.py
- ✅ fold_batch_dim/unfold_batch_dim implemented (lines 112+)
- ⏳ TODO: Optimize memory usage during tensor reshaping (line 114)
- ⏳ TODO: Add support for different tensor types and shapes (line 115)
- ⏳ TODO: Optimize tensor view operations for performance (line 136)
- ⏳ TODO: Add error handling for invalid batch dimensions (line 137)
- ⏳ TODO: (zhangchi.usc1992) add consistency check (line 169)
- ⏳ TODO: we can actually lift this restriction if needed (line 265)
- ⏳ TODO: (zhangchi.usc1992) whether to copy (line 351)

##### luffy/verl/verl/trainer/fsdp_sft_trainer.py
- ⏳ TODO: (zhangchi.usc1992) (line 16)
- ⏳ TODO: add checkpoint manager (line 77)
- ⏳ TODO: (zhangchi.usc1992): (line 140)
- ⏳ TODO: Implement model loading with proper initialization context (line 159)
- ⏳ TODO: Add support for different model types and configurations (line 160)
- ⏳ TODO: Implement memory-efficient model loading for large models (line 161)
- ⏳ TODO: Add model validation and compatibility checks (line 162)
- ⏳ TODO: Complete model loading implementation (line 165)
- ⏳ TODO: Add support for custom model architectures (line 166)
- ⏳ TODO: Implement proper dtype and attention configuration (line 167)
- ⏳ TODO: Implement gradient checkpointing configuration (line 170)
- ⏳ TODO: Add memory usage optimization strategies (line 171)
- ⏳ TODO: Configure mixed precision training settings (line 172)
- ⏳ TODO: Implement FSDP sharding and wrapping policies (line 173)
- ⏳ TODO: Add CPU offloading configuration for memory optimization (line 174)
- ⏳ TODO: Set up distributed training parameters properly (line 175)
- ⏳ TODO: Initialize FSDP wrapped model (line 178)
- ⏳ TODO: add a unified tracking (line 301)
- ⏳ TODO: (zhangchi.usc1992) add back checkpoint manager. Currently, it blocks when uploading to hdfs. So very slow. (line 318)

##### luffy/verl/verl/trainer/main_ppo.py
- ⏳ TODO: Implement reward computation for different data sources (line 50)
- ⏳ TODO: Add support for parallel processing of reward computation (line 53)
- ⏳ TODO: Implement proper sequence decoding and validation (line 54)
- ⏳ TODO: Add thread-safe logging and debugging functionality (line 55)
- ⏳ TODO: Optimize memory usage for large batch processing (line 56)
- ⏳ TODO: Extract and validate prompt and response sequences (line 62)
- ⏳ TODO: Decode sequences to text format (line 63)
- ⏳ TODO: Apply appropriate reward function based on data source (line 64)
- ⏳ TODO: Handle edge cases and error conditions (line 65)
- ⏳ TODO: Implement batch-wise reward computation (line 70)
- ⏳ TODO: Add proper error handling and validation (line 71)

#### ✅ Already Completed Items
- ✅ **OpenAI API Integration**: Full client initialization with exponential backoff retry logic (luffy/deepscaler/utils.py)
- ✅ **Batch Dimension Operations**: fold_batch_dim/unfold_batch_dim fully implemented (luffy/verl/verl/protocol.py)