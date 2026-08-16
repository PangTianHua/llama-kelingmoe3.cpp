# llama-kelingmoe3.cpp

> 在 [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp) 上跑 [Ling-3.0-tiny](https://huggingface.co/inclusionAI/Ling-3.0-tiny) 的预编译包 fork。

## 关于本仓库

本仓库是 [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp) 的 fork，跟进 [aetherbird/llama.cpp](https://github.com/aetherbird/llama.cpp) 的 `bailingmoe3-support` 分支（提供 **BailingMoE3** 架构支持），并发布对应的 Windows + CUDA 12.4 预编译包。

**目的**：想尽早用 llama.cpp 跑 [Ling-3.0-tiny](https://huggingface.co/inclusionAI/Ling-3.0-tiny)，所以自己做了一份预编译包开源出来。

## 预编译包

最新发布：[Releases](../../releases) 页面。

| 项 | 值 |
|---|---|
| 文件名 | `llama-bailingmoe3-cuda12.4-bin-win-x64.zip` |
| 大小 | ~80 MB |
| SHA256 | `1d9f9e47e9a9d0aa001bbcd038e7fa68d3ec0c7a7682aee326af618f2873d91b` |
| 平台 | Windows 10 / 11 x64 |
| 编译器 | MSVC 19.40 + CUDA 12.4 |
| GPU | NVIDIA GPU（CUDA 12.4 driver）|
| 最低 VRAM | 6 GB（推荐跑 Ling-3.0-tiny Q4_K_M）|
| 包含 | `llama-server.exe` + `llama-cli.exe` + `llama-bench.exe` + CUDA 12.4 runtime DLLs |

## 快速开始

1. **下载预编译包**：[Releases](../../releases) 页面
2. **下载模型**：从 [Mike0021/Ling-3.0-tiny-GGUF](https://huggingface.co/Mike0021/Ling-3.0-tiny-GGUF) 或 [unsloth/Ling-3.0-tiny-GGUF](https://huggingface.co/unsloth/Ling-3.0-tiny-GGUF) 拿 Q4_K_M 版本
3. **启动**：

```sh
llama-server -m path/to/Ling-3.0-tiny-Q4_K_M.gguf -ngl 99
```

## 致谢

- [ggml-org/llama.cpp](https://github.com/ggml-org/llama.cpp) —— 上游
- [aetherbird/llama.cpp](https://github.com/aetherbird/llama.cpp) —— BailingMoE3 架构支持
- [inclusionAI](https://huggingface.co/inclusionAI) —— Ling 模型作者

## License

MIT
