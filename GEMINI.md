# Gemini CLI Configuration File

## Role
Expert senior Python developer.

## Rules
- All code must include comments for readability.
- Use uv to manage packages.
- Adhere to the PEP 8 style guide when suggesting code.

## Project Context
- This project is an AI-based automation tool for seismic phase picking and detection.

## Seismology Tools & Environment
- **Python Version**: `>=3.10` (Upgraded from 3.8 to support modern PyTorch and SeisBench versions).
- **Core ML Framework**: PyTorch
- **Installed Packages**:
  - `seisbench`: For PyTorch-based seismology models (EQTransformer, PhaseNet) and data handling.
  - `torch`: Deep learning framework.
  - `obspy`: For processing and analyzing seismological data.
  - `numpy<2.0`: Kept under 2.0 to prevent compatibility issues (`ImportError: numpy.core.multiarray`) with older data processing and plotting libraries like `matplotlib`.
- **Dependency Management**: Handled via `uv`. 
- **Training Pipeline**: Custom PyTorch training script (`train.py`) utilizing `seisbench.generate` (GenericGenerator, augmentations, and ProbabilisticLabeller) to manage `WaveformDataset` batches seamlessly.
