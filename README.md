## 🚀 视频背景&Object移除（开源模型&项目）

### Generative Video Matting (2025年8月)  
- 📄 [论文链接](https://arxiv.org/abs/2508.07905?utm_source=chatgpt.com)  
- 📝 特点：结合大规模 synthetic + pseudo-标注数据预训练；视频 diffusion 增强泛化能力；边缘细节和时间连贯性好  
- 🔧 可用性：论文提供了数据和生成管道，但暂未完全轻量开源  

### MatAnyone (CVPR 2025)  
- 📄 [论文链接](https://openaccess.thecvf.com/content/CVPR2025/papers/Yang_MatAnyone_Stable_Video_Matting_with_Consistent_Memory_Propagation_CVPR_2025_paper.pdf?utm_source=chatgpt.com)  
- 📝 特点：“Stable Video Matting with Consistent Memory Propagation”，边界细节 + 帧间一致性强  
- 🔧 可用性：[GitHub 开源代码](https://github.com/pq-yang/MatAnyone?utm_source=chatgpt.com)  

### OmnimatteZero (2025年3月)  
- 📄 [论文链接](https://arxiv.org/abs/2503.18033?utm_source=chatgpt.com)  
- 📝 特点：零训练（zero-shot）版 Omnimatte；基于预训练视频 diffusion，实时分离对象层和背景层，支持阴影/反射等  
- 🔧 可用性：开源，有论文和代码  

### VRMDiff (Video Referring Matting Diffusion, 2025年3月)  
- 📄 [论文链接](https://arxiv.org/abs/2503.10678?utm_source=chatgpt.com)  
- 📝 特点：通过文本提示 / caption 指定对象，生成 alpha matte；可区分实例；适合交互式抠图  
- 🔧 可用性：开源，有数据集 + 代码  

### PTQ4VM (Post-Training Quantization for Video Matting, 2025年6月)  
- 📄 [论文链接](https://arxiv.org/abs/2506.10840?utm_source=chatgpt.com)  
- 📝 特点：针对资源受限设备的后训练量化；保持高精度和时间一致性，同时降低推理成本  
- 🔧 可用性：开源研究，可在现有模型上应用

### 🔧 开源项目 /实用工具
除了论文模型外，这里有几个实际可以拿来试的视频 / 背景移除 / matting 工具 / repo：  

- [MatAnyone GitHub 项目](https://github.com/pq-yang/MatAnyone?utm_source=chatgpt.com)  
- [Real-Time High-Resolution Background Matting (BackgroundMattingV2)](https://github.com/PeterL1n/BackgroundMattingV2?utm_source=chatgpt.com)：支持 4K@30fps 或 HD@60fps，如果有较好的 GPU，可用于高分辨率视频背景去除。  
- [BackgroundRemover by nadermx](https://github.com/nadermx/backgroundremover?utm_source=chatgpt.com)：比较轻量 / CLI 风格的工具，可以用于 image + video background removal。


## 🖼️ 图片背景移除（开源模型&项目）

### U²‑Net (2020)
📄 [论文 / GitHub](https://github.com/xuebinqin/U-2-Net)  
📝 特点：Nested U 结构 + Residual U‑Blocks，多尺度特征；轻量版 U2Netp；适合通用前景/背景分割任务  
🔧 可用性：完全开源；支持 CPU / GPU 推理；工具集成如 rembg  
⚡ 推理性能：全尺寸 ~176MB，320×320 图像 ~30FPS；轻量版 ~4.7MB，约40FPS；中等分辨率效果佳  

---

### MODNet (2020)
📄 [论文 / GitHub](https://github.com/ZHKKKe/MODNet)  
📝 特点：轻量网络 + 多尺度特征融合 + e-ASPP + SOC 子目标一致性；trimap-free；适合人像背景移除  
🔧 可用性：开源；实时视频/静态图像推理  
⚡ 推理性能：1080Ti 下静态图像 ~67FPS；高分辨率需降采样；精度好于轻量显著性模型  

---

### BiRefNet (2024)
📄 [论文 / GitHub](https://github.com/ZhengPeng7/BiRefNet)  
📝 特点：双向参考机制，高分辨率输入支持；边缘细节和复杂背景处理效果好  
🔧 可用性：开源；提供多版本（轻量 / 高精度 / HR）  
⚡ 推理性能：HR 可处理 2048×2048 图像；显存需求高；精度优秀  

---

### InSPyReNet (2022)
📄 [论文 / GitHub](https://github.com/plemeri/InSPyReNet)  
可运行项目 [github](https://github.com/plemeri/transparent-background)
📝 特点：图像金字塔 + 多尺度处理，高分辨率显著性分割；边缘与复杂背景效果好  
🔧 可用性：MIT 许可开源；工具集成支持批量图像处理  
⚡ 推理性能：速度略慢于 U²‑Net；高分辨率效果佳；精度高于 U²‑Net  

---

### rembg (2020)
📄 [GitHub](https://github.com/danielgatis/rembg)  
📝 特点：工具包 + 多个模型集成（U²‑Net 系列）；支持各种输入输出格式  
🔧 可用性：易用，生态成熟；可切换不同模型权衡速度与精度  
⚡ 推理性能：速度取决 backend；轻量版快速，全版消耗高；精度与所用模型相关  

---

### ToonOut (BiRefNet fine-tuned) (2024)
📄 [论文](https://arxiv.org/abs/2509.06839)  

📝 特点：基于 BiRefNet 微调，优化卡通 / 动漫风格；半透明/边缘处理效果好  
🔧 可用性：开源权重 + 数据集提供  
⚡ 推理性能：硬件依赖较高；Pixel Accuracy 可达 ~99%+；支持中高分辨率动漫图像  
