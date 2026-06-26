# AI Try-On And Video Notebooks

Kaggle-ready notebooks for virtual dress try-on and portrait video generation.

## Files

- `tryondress.ipynb` - virtual dress try-on workflow using CatVTON.
- `ai-video.ipynb` - portrait video generation workflow using SadTalker.

## Virtual Dress Try-On

- Sets up the CatVTON environment on Kaggle.
- Loads a target person image and a reference dress image.
- Uses full-dress mode with `CLOTH_TYPE = "overall"`.
- Generates the final output image.

## Kaggle Input Paths

The notebook is currently configured to use:

```text
/kaggle/input/datasets/ganapathyg/trynewdata/Dwa.jpeg
/kaggle/input/datasets/ganapathyg/trynewdata/dress.jpg
```

Update these paths in Cell 3 if your Kaggle dataset uses different filenames or folders.

## Output

The generated try-on image is saved to:

```text
/kaggle/working/virtual_dress_outputs/virtual_dress_result.png
```

## AI Portrait Video

`ai-video.ipynb` is configured as a Kaggle workflow that:

- Checks the Kaggle runtime and GPU.
- Finds uploaded image, prompt text, and optional audio files in `/kaggle/input`.
- Sets up SadTalker dependencies and checkpoints.
- Generates a portrait video.

The final video is saved to:

```text
/kaggle/working/portrait_video_zipless/outputs/output.mp4
```

## How To Run

1. Open the notebook you want to use in Kaggle.
2. Enable GPU acceleration.
3. Attach the required Kaggle input dataset files.
4. Run the setup cells.
5. Run the generation cells.
6. Download the final result from the output link in the last cell.

## Notes

- The notebooks are designed for Kaggle Python 3.12 with GPU.
- If Kaggle shows dependency warnings during setup but the install finishes successfully, continue to the next cells.
- For CatVTON import issues, delete `/kaggle/working/.catvton_env_ready_v6` and rerun Cell 1 in `tryondress.ipynb`.
