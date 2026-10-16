<div align="center">

<img src="assets/ghifarion/repo-banner.svg" alt="MCAP TO MP4 · GOOGLE DRIVE — Convert supported recordings in a guided Colab workflow." width="100%">

</div>

# MCAP to MP4 — Google Drive Notebook

A Google Colab notebook for converting MCAP recordings stored in Google Drive into MP4 files, processing recordings one at a time.

## What it does

- Mounts Google Drive in Colab.
- Copies each input recording to the Colab runtime for processing.
- Processes files sequentially to help limit peak memory use.
- Copies generated MP4 files back to Drive and removes temporary local files.
- Detects the supported recording formats described in the notebook:
  - `ego_*.mcap` recordings with two cameras and protobuf data.
  - ROS 2 recordings containing `/head/camera/image_compressed` with H.265 video.
- Installs support for zstd and lz4 compressed MCAP chunks when needed.

## Run it

1. Open [`mcap_drive.ipynb`](./mcap_drive.ipynb).
2. Select **Open in Colab**.
3. Read the notebook instructions and run the cells in order.
4. When prompted, authorize Google Drive access and check the configured input/output folders before running the conversion.

**Important:** Run this notebook only on recordings and Drive folders you are authorized to access. Confirm the input and output paths before processing a large batch.

## Requirements

- A Google account with access to Google Colab.
- Google Drive access to the source recordings and destination folder.
- Sufficient Colab runtime resources for the recordings being processed.

## Notebook

[Open the notebook in GitHub](./mcap_drive.ipynb) · [Open directly in Google Colab](https://colab.research.google.com/github/progstay17/mCAP-to-mp4-drive-converter/blob/main/mcap_drive.ipynb)

---

This repository currently provides the notebook workflow; it is separate from the desktop/CLI converter project.
