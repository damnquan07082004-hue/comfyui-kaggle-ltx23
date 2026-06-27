# ComfyUI-Kaggle + LTX 2.3 GGUF 🚀

Kaggle notebooks for running **ComfyUI** with **LTX 2.3 GGUF** (Unsloth Dynamic 2.0) — multi-scenario video generation on free GPU!

## 📓 Notebooks

| Notebook | Description | Kaggle Link |
|----------|-------------|-------------|
| **ComfyUI + LTX 2.3 GGUF** | LTX 2.3 Text/Image→Video, IC-LoRA face consistency, 11 official workflows | [Open in Kaggle](https://www.kaggle.com/code/quan0708/comfyui-ltx-2-3-gguf-multi-scenario) |
| **ComfyUI (March 2025)** | Original — SDXL, FLUX, general purpose | [Open in Kaggle](https://www.kaggle.com/code/pogscafe/comfyui-kaggle-march-2025) |
| **ComfyUI (November 2023)** | Original — older version | [Open in Kaggle](https://www.kaggle.com/pogscafe/comfyui-kaggle) |

## ✨ What can LTX 2.3 GGUF do?

| Type | Workflow | Description |
|------|----------|-------------|
| **Text→Video** | T2V Single Stage | Pure text prompt to video |
| **Image→Video** | I2V Single Stage | Product image → motion video |
| **Face Reference** | ICLoRA HDR | Keep character face consistent |
| **Person + Product** | ICLoRA Ingredients | Multi-reference image input |
| **Person Holding Product** | ICLoRA Union Control | Person + product reference |
| **Lip Sync** | ICLoRA Lipdub | Video + audio → lip sync |
| **Video→Video** | V2V ICLoRA | Transform existing video |
| **Inpaint/Outpaint** | ICLoRA Inpaint/Outpaint | Fix/extend video |

## 🚀 Quick Start

1. Open the [Kaggle notebook](https://www.kaggle.com/code/quan0708/comfyui-ltx-2-3-gguf-multi-scenario)
2. Click **Copy & Edit** → **Settings** → **Accelerator: GPU T4 x2** (or P100)
3. Enable **Internet** → **Run All**
4. Wait ~20-30 min for model downloads (one-time per session)
5. Click the tunnel URL → Open ComfyUI
6. Load workflow from `/kaggle/working/workflows/`
7. Queue Prompt!

## 🌐 Tunnel Options

| Method | Setup | URL Changes? | Best For |
|--------|-------|-------------|----------|
| **Pinggy** (default) | Zero config | Every hour | Quick testing |
| **Cloudflare Tunnel** | Domain + API token | **Never** 🏆 | Production / Auto API |

### Cloudflare Tunnel Setup (one-time)

```bash
# Install locally first
cloudflared tunnel create comfyui-ltx23
cloudflared tunnel route dns comfyui-ltx23 your-subdomain.yourdomain.com

# Upload credentials.json to Kaggle Dataset
# Or use CF_TUNNEL_TOKEN in notebook config
```

## 📁 Included Workflows (18 files)

- **3 Isi-dev GGUF workflows** — Basic I2V/T2V + Audio
- **11 Lightricks Official workflows** — All IC-LoRA variants
- **4 Original sample workflows** — SD/FLUX

## 🧠 Model

Uses **Unsloth LTX-2.3-GGUF Dynamic 2.0**:
- **Q3_K_M** (~10.6 GB) — Recommended for P100/T4 16GB
- **Q2_K** (~7.94 GB) — For low VRAM with headroom
- **Q4_K_M** (~14.2 GB) — For T4 x2 with GPU split

Text encoder: **Gemma 3 12B** (GGUF quantized)

## 📺 Video Tutorial

Check out [AIQUEST's tutorial (62K views)](https://youtu.be/dq-0jeyJA8I) on YouTube

## 🙏 Credits

- **wandaweb** — [ComfyUI-Kaggle](https://github.com/wandaweb/ComfyUI-Kaggle) (base notebook)
- **Isi-dev** — [Google-Colab-Notebooks](https://github.com/Isi-dev/Google-Colab_Notebooks) (LTX 2.3 branch)
- **Lightricks** — [ComfyUI-LTXVideo](https://github.com/Lightricks/ComfyUI-LTXVideo) (official nodes + workflows)
- **Unsloth** — [LTX-2.3-GGUF](https://huggingface.co/unsloth/LTX-2.3-GGUF) (Dynamic 2.0 quantization)
- **Kijai** — [LTX2.3_comfy](https://huggingface.co/Kijai/LTX2.3_comfy) (model splitting)

## 📜 License

MIT — same as original ComfyUI-Kaggle
