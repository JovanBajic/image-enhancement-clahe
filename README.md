# Image Enhancement and CLAHE

Python notebook exploring contrast enhancement, image sharpening, and a custom implementation of contrast-limited adaptive histogram equalization (CLAHE).

## What the notebook covers

- **HDR contrast enhancement:** converts a 16-bit image for display, comparing percentile contrast stretching, CLAHE, logarithmic transforms, and gamma correction.
- **Color image sharpening:** processes the luminance component using a Laplacian filter and high-frequency emphasis, comparing detail enhancement and noise amplification.
- **Custom CLAHE (`dosCLAHE`):** tile histograms, histogram clipping and redistribution, cumulative distributions, and bilinear interpolation between neighboring tiles.
- **Experiments:** compares tile counts and clipping limits, discusses halo artifacts, and measures execution time against scikit-image's implementation.

## Getting started

Requires Python 3, JupyterLab, NumPy, SciPy, Matplotlib, and scikit-image.

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install jupyterlab numpy scipy matplotlib scikit-image
jupyter lab
```

Open [domaci1_20_662.ipynb](domaci1_20_662.ipynb) and run the cells in order from the repository directory.

## Input data

The original assignment images are **not included in this repository**. To rerun the experiments, supply the following files at the paths expected by the notebook:

- `sekvence/street.tif`
- `sekvence/miner.jpg`
- `sekvence/train.jpg`

The notebook contains saved figures and outputs that can be viewed without rerunning it. The notebook text and comments are primarily in Serbian.

## Project context

Academic image-processing coursework (DOS), with implementations, parameter experiments, visual comparisons, and discussion. This repository preserves the original notebook; it is not a packaged library. Dependencies are not version-pinned, and compatibility with current releases has not been verified. Full execution requires the missing input images.

## Output notes

The original code saves `sekvence/street_out.jpg` and `sekvence/miner_sharp.jpg.jpg`. The export cells use the gamma-enhanced and high-frequency-emphasis images, respectively, although the accompanying discussion selects logarithmic enhancement and Laplacian sharpening.
