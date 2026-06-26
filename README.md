# Virtual Dress Try-On

A Kaggle-ready virtual dress try-on notebook using CatVTON. The notebook takes a target person image and a reference dress image, then generates a realistic dress try-on result.

## Files

- `tryondress.ipynb` - main notebook for running the virtual dress try-on workflow.

## What It Does

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

## How To Run

1. Open `tryondress.ipynb` in Kaggle.
2. Enable GPU acceleration.
3. Run Cell 1 once to install the environment.
4. After the kernel restarts, run all cells.
5. Download the final result from the output link in the last cell.

## Notes

- The notebook is designed for Kaggle Python 3.12 with GPU.
- If Kaggle shows dependency warnings during setup but the install finishes successfully, continue to the next cells.
- If imports fail, delete `/kaggle/working/.catvton_env_ready_v6` and rerun Cell 1.
