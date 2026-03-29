# Reviewer sEtD

## [W1 & Q3 & Q4]:Supplementary Discussion on Mip-Splatting and Multi-Resolution Training Inputs

Model Size, Memory Cost and Rendering Quality Comparison between Mip-Splatting and Ours


| Scene      | Method         | GS (M) ↓ | Size (GB) ↓ | Mem (GB) ↓ | PSNR ↑ | SSIM ↑ | LPIPS ↓ |
|------------|---------------|----------|-------------|------------|--------|--------|---------|
| Building   | Mip-Splatting | 19.67    | 4.62        | >60        | 20.65  | 0.684  | 0.345   |
|            | Ours          | 6.39     | 1.28        | 12.09      | 22.84  | 0.804  | 0.210   |
| Rubble     | Mip-Splatting | 17.21    | 4.04        | >60        | 24.04  | 0.724  | 0.323   |
|            | Ours          | 5.89     | 1.27        | 11.45      | 25.85  | 0.801  | 0.210   |
| Residence  | Mip-Splatting | 20.03    | 4.70        | >60        | 20.98  | 0.747  | 0.272   |
|            | Ours          | 5.26     | 1.29        | 9.31       | 22.51  | 0.825  | 0.205   |
| Sci-Art    | Mip-Splatting | 6.11     | 1.43        | >40        | 21.74  | 0.806  | 0.257   |
|            | Ours          | 1.98     | 0.45        | 10.82      | 22.62  | 0.815  | 0.208   |
