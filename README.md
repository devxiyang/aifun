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
