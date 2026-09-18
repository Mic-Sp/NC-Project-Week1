# Vivi's Dream

A technical showcase website documenting the journey of remastering the iconic full-motion videos (FMVs) of Final Fantasy IX for modern displays.

## About the Project

Vivi's Dream was born from a desire to bring the breathtaking cinematics of FFIX out of the standard-definition era (240p) without sacrificing their original soul. This repository contains the source code for the project's showcase web page, which details the workflows, experiments, and technical pipelines used to revitalize these classic cutscenes.

### Highlights Documented
*   **The First Attempt:** An initial automated super-resolution pipeline using a custom-tuned Real-ESRGAN model and FFmpeg.
*   **The Direction Forward:** A next-generation generative reconstruction pipeline leveraging FLUX.1 [dev] within ComfyUI, ControlNet, and custom LoRAs to achieve true high-fidelity results without the artifacts of traditional upscalers.

## Technologies Discussed
*   **Generative AI & Upscaling:** FLUX.1 [dev], ComfyUI, Real-ESRGAN, PyTorch, ControlNet
*   **Video Processing:** FFmpeg
*   **Web Frontend:** HTML5, CSS3

## Getting Started

To view the showcase locally, simply clone this repository and open `index.html` in your web browser. No complex build tools or dependencies are required.
