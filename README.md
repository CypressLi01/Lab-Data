# Reviewer: 9eC6
## [W3 & Q3]: DoG mask computation overhead and its impact on the training FPS
As shown in the figure below, we present the GPU usage of the DoG module throughout the entire training process for a single view.

<img width="557" height="419" alt="image" src="https://github.com/user-attachments/assets/f7e3b88b-ce04-4b5f-bf93-671023825291" />

As shown in the table, we also report the impact of the DoG mask on training FPS.
| Variant                   | PSNR  | Mem(G) | FPS    |
|---------------------------|-------|--------|--------|
| w/o Freq-Guided Objective | 22.15 | 10.92  | 107.23 |
| ours                      | 22.62 | 10.82  | 111.17 |


# Reviewer:  Lt69
## [Q4]: Total number of iterations
Performance of 3DGS and Ours under Different Training Iterations

| Method   | iters   | SSIM  | PSNR  | LPIPS |
|----------|---------|-------|-------|-------|
| 3DGS     | 30000   | 0.791 | 24.16 | 0.262 |
|      | 100000  | 0.793 | 24.13 | 0.258 |
| Ours     | 100000  | 0.815 | 22.62 | 0.208 |
|     | 200000  | 0.815 | 22.63 | 0.207 |


## [Q5]: Baseline
Performance Sensitivity of CityGS-X to Batch Size and GPU Number

| Batch/GPU | SSIM  | PSNR  | LPIPS |
|-----------|-------|-------|-------|
| 2/2       | 0.742 | 21.47 | 0.225 |
| 4/5       | 0.789 | 21.98 | 0.205 |


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
