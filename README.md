

````markdown
# 🎥 NeRF Training & Rendering in Google Colab

This project provides a simple pipeline to **train and render Neural Radiance Fields (NeRF)** models directly in **Google Colab**. Users can choose from preset datasets or upload their own images, videos, Polycam, or Record3D captures.  

## 🚀 Features
- Easy setup with automatic installation of dependencies  
- Support for preset datasets (`poster`, `dozer`, `desolation`)  
- Upload and process your own images, videos, Polycam, or Record3D data  
- Train NeRF models using **Nerfstudio (nerfacto pipeline)**  
- Render spiral (orbit) videos of trained models  

## 🛠️ Requirements
- Google Colab (recommended)  
- Python 3.9+  
- Dependencies: `nerfstudio`, `torch`, `numpy`, `pandas`  

## 📂 Workflow
1. Install dependencies  
2. Select or upload dataset  
3. Process data for NeRF training  
4. Train NeRF model (`nerfacto`)  
5. Render a spiral video of the scene  

## ▶️ Example Usage
In Colab:
```python
# Install dependencies
!pip install nerfstudio torch==2.5.1 torchvision==0.20.1 numpy pandas

# Run training
!ns-train nerfacto --max-num-iterations 4000 \
   nerfstudio-data --data data/nerfstudio/poster --downscale-factor 4

# Render spiral video
!ns-render spiral --load-config /content/outputs/.../config.yml \
   --output-path /content/renders/output.mp4
````

## 📸 Output

* `config.yml` → trained NeRF configuration
* `/content/renders/output.mp4` → final rendered spiral video

## 🙌 Acknowledgements

* [Nerfstudio](https://docs.nerf.studio/) for the core pipeline
* Google Colab for cloud-based training
* Torch & Numpy for ML backend

```

```
