A compatibility wrapper for software that imports the ``flash_attn`` Python
namespace on unsupported GPUs. It delegates attention to PyTorch scaled dot
product attention; it is not a fused FlashAttention kernel.

Do not install this distribution alongside ``flash-attn`` or
``flash-attn-legacy``. They provide the same ``flash_attn`` module paths, so the
last package installed can overwrite files from the other implementation.

NOTE This needs more work by someone who know GPU Programming
