# Spring 2023 - Deep Learning - New York University (NYU)
# NeRF: Neural Radiance Fields - A deep dive into the variations and applications

## Authors

- Aneek Roy (Net ID: ar8002, NYU ID: N18324528)
- Jash Rathod (Net ID: jsr10000, NYU ID: N13876910)

## Project Abstract
In this project, we explore different variations of the Neural Radiance Fields (NeRF) technique for generating new views of intricate scenes using sparse inputs. We compare the performance of various NeRF implementations and investigate their strengths and weaknesses. Our focus is on understanding NeRF variations such as PixelNeRF, RegNeRF, and SNeRG, and their applications in constrained resource environments, sparse coding, real-time performance, and representation from one or few images. We visually compare these variations with prior works in neural rendering and view synthesis.

## Architectures

In this section, we provide an overview of the architectures used in our experiments. The following images depict the architectures of each variation:

### NeRF Architecture
![NeRF Architecture](NeRF_arch.png)

### PixelNeRF Architecture
![PixelNeRF Architecture](pixelNeRF.png)

### RegNeRF Architecture
![RegNeRF Architecture](RegNeRF_arch.png)

### SNeRG Architecture
![SNeRG Architecture](SNeRF.png)

These images provide a visual representation of the network structures for each architecture. They help in understanding the design and components of the NeRF variations we explored in our experiments.

## Experiments and Results

Our objective was to compare different implementations of NeRF and evaluate their performance. We conducted experiments using custom environments and objects, such as library rooms and a 3D-printed Yoda toy. We utilized existing NeRF implementations available on GitHub repositories and obtained the following results:

### NeRF
We used NerfStudio for NeRF implementation. The output was a 3D render viewed on PolyCam. The fine-tuned hyperparameters for this implementation were Polygon Size (5 mm) and Smoothing (10%).

![NeRF output](NeRF_out.png)

### PixelNeRF and RegNeRF
PixelNeRF and RegNeRF address sparsity in inputs. We fed four images to each model and obtained 3D renders of library rooms in the NYU Dibner Library.

PixelNeRF Output:
![PixelNeRF output](dibner_1.png)

RegNeRF Output:
![RegNeRF output](dibner_2.png)

### SNeRG
SNeRG was implemented on screenshots from a video of a smaller subsection of a room. The rendered views were detailed at the center but had artifacts at the outer fringes.

Entire View:
![SNeRG Entire View](SneRG_imp.png)

Focus on the Center:
![SNeRG Center](SNeRG_foc.png)

We also plotted the Peak Signal to Noise Ratio (PSNR) against the number of input views for each architecture. Higher PSNR values indicate better performance.

![PSNR Results](graph_results.png)

We summarize our best results in terms of PSNR in the following table:

| Architecture | Best PSNR |
|--------------|-----------|
| NeRF         | 24.324    |
| PixelNeRF    | 23.173    |
| RegNeRF      | 25.190    |
| SNeRG        | 23.981    |

## Conclusion

Through this project, we have gained a comprehensive understanding of NeRF variations and their applications. We have compared the performance of different NeRF implementations and identified their strengths and weaknesses. Our work provides insights into addressing challenges such as sparse inputs, real-time performance, and representation from limited images. Further experiments and research will contribute to overcoming these challenges and improving the capabilities of NeRF.

Please refer to the full report ([report.pdf](report.pdf)) for a detailed analysis and discussion of the results.

## References

- NeRF - (https://www.matthewtancik.com/nerf)
- Pixel-NeRF - (https://alexyu.net/pixelnerf/)
- regNeRF - (https://m-niemeyer.github.io/regnerf/)
- sNeRG - (https://phog.github.io/snerg/)
