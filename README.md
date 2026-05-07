# Parking Intelligence v1

This repo includes:
- Phase-1: Vehicle detection and filtered detection exports
- Phase-2: Manual calibration, homography estimation, BEV generation, and tile-based scale calibration
- Phase-3: BEV scene annotation, BEV masks, transformed detections, occupied/free-space masks
- OpenCV image augmentation utility

## Input Folder Structure

Use this input root:

`sukshi_parking/`
- `similar_cctv_view/`
- `Front_view/`
- `Side_view/`

All phases recursively load images from all subfolders under `sukshi_parking/`.

## Setup

```bash
pip install -r requirements.txt
```

## OpenCV Augmentation Run

```bash
python src/augment_images.py
```

## Phase-1 Run

```bash
python src/main.py --images-dir sukshi_parking --output-dir outputs --model yolo26x.pt --conf-threshold 0.25
```

## Phase-2 Run

```bash
python src/main_phase2.py --images-dir sukshi_parking --output-dir outputs
```

## Phase-3 Run

```bash
python src/main_phase3.py --images-dir sukshi_parking --output-dir outputs --dilation-px 6
```

Optional Phase-3 reuse of existing annotation JSON:

```bash
python src/main_phase3.py --images-dir sukshi_parking --output-dir outputs --reuse-existing-scene --reuse-existing-scale
```
