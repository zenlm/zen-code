# Zen Code 4B

General-purpose code generation model. Part of the Zen Eco family.

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## Overview

Zen Code 4B is a compact code generation model optimized for fast inference. Supports multiple programming languages with strong performance on code completion, generation, and explanation tasks.

| Property | Value |
|----------|-------|
| Parameters | 4B |
| Context | 32K |
| License | Apache 2.0 |

## Usage

```python
from transformers import AutoModelForCausalLM, AutoTokenizer

model = AutoModelForCausalLM.from_pretrained("zenlm/zen-code")
tokenizer = AutoTokenizer.from_pretrained("zenlm/zen-code")
```

## Related

- [zen-eco](https://huggingface.co/zenlm/zen-eco) — Base 4B model
- [zen-coder](https://huggingface.co/zenlm/zen-coder) — 24B code model
- [Zen LM](https://github.com/zenlm) — Full model family

Apache 2.0 · [Zen LM](https://zenlm.org) · [Hanzo AI](https://hanzo.ai)
