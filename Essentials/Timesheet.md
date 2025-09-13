
# 📓 Developer’s Journal – snakhy2s - Shrikar Nakhye

---

## **Initial Commit** (04.06.25, 19:35:54)
- **Commit**: `212cc50`
- **Summary**: Set up the foundation of the project.
- **Details**:
  - Added `.gitignore` (comprehensive Python + IDE ignores).
  - Created a basic `README.md` with project title *Shadow_Casting_Object_Segmentation*.
- **Reflection**:
  This was the project bootstrap stage: preparing the repo with clean version control practices and a placeholder readme.

---

## **Conda Environment Cleanup** (04.09.25, 10:03:04)
- **Commit**: `20b562e`
- **Summary**: Made the Conda environment file agnostic to local paths.
- **Details**:
  - Removed hardcoded prefixes (`/Users/<user>/anaconda3/envs/dlrv`).
  - Stripped platform-specific build hashes from dependencies.
- **Reflection**:
  Ensured the environment YAML is portable across different machines—an important step for collaborators and reproducibility.

---

## **First UNet Training Pipeline** (13.09.25, 00:01:21)
- **Commit**: `fe7cfc9`
- **Summary**: Introduced UNet training logic with evaluation.
- **Details**:
  - Implemented `train_unet.py`: data loader, UNet model (ResNet34 encoder), training loop.
  - Added IoU calculation for validation.
  - Introduced logging, GPU memory tracking, and metrics plotting.
  - Extended `.gitignore` to include `.DS_Store`.
- **Reflection**:
  This was the first functional training setup. The model could train and report validation IoU. Still very raw, but the base loop worked.

---

## **Adding Inference and Polishing Training** (13.09.25, 00:23:27)
- **Commit**: `74c792a`
- **Summary**: Expanded functionality with inference, modularity, and better documentation.
- **Details**:
  - **`inference_unet.py`**:
    - Loads trained model and runs inference on new images.
    - Outputs prediction mask alongside original image visualization.
  - **`train_unet.py` Updates**:
    - Added `argparse` for configurable paths, epochs, and batch size.
    - Simplified logging (no longer separate log files).
    - Cleaned unused features (GPU memory log, inference timing).
  - **New `unet.py`**:
    - A more detailed training script with logging to file, GPU monitoring, inference speed measurement, and plotting of metrics.
  - **README Overhaul**:
    - Rebranded project as **🌍 PrithviVision**.
    - Documented goals (shadow-casting object segmentation in aerial imagery).
    - Added inference usage instructions.
    - Highlighted model variety (U-Net, YOLO, Mask R-CNN).
- **Reflection**:
  A major milestone. The project now supports both **training and inference**, is parameterized for flexibility, and has a clear identity with improved documentation.

---

# 🚀 Key Evolution

1. **From Idea → Identity**
   - Started as *Shadow_Casting_Object_Segmentation*.
   - Rebranded to **PrithviVision**, aligning with broader goals in aerial image understanding.

2. **From Training Only → Full Workflow**
   - Early commits only supported training.
   - Later commits introduced **inference, visualization, and modular scripts**.

3. **From Local Hack → Portable Research Project**
   - Cleaned environment setup.
   - Enhanced documentation, logging, and reproducibility.

---

# 📌 Next Steps (Future Roadmap)
- Add **Mask R-CNN training pipeline** (already hinted in README).
- Integrate **YOLO training/inference** with the curated dataset.
- Add experiment tracking (e.g., Weights & Biases).

---
