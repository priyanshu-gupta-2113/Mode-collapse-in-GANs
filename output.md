Generates 2D points arranged in a ring-like pattern.

The points are clustered into 8 groups (like a circle divided into 8 sections).

Each cluster follows a Gaussian (normal) distribution.
![image](https://github.com/user-attachments/assets/c49c7b19-cc42-4def-9d11-4612a8e6ae6e)


why I did not use any real dataset:


1-Controlled Environment for Mode Collapse Analysis

    We generated our own data (e.g., 8 Gaussian modes in a circle) because it allows us to clearly visualize and study mode collapse.

    Real-world datasets are more complex, making it harder to isolate and analyze mode collapse behavior.

2-Easy to Define Ground Truth

    Since we know the exact number of modes (8 clusters) in our generated data, we can directly measure how many modes the GAN captures.

    In a real dataset, we don’t always know the true number of clusters, making evaluation harder.

3-Simplified Metric Calculation

    KL divergence and mode coverage are easier to compute when we have a predefined distribution.

    If we used a real dataset, we would need additional clustering methods to estimate real modes.

4-Avoid Bias from Real-World Datasets

    Some real datasets might be imbalanced (e.g., some modes appearing more frequently than others).

    By generating our own data, we ensure that each mode has an equal chance, making it a fair test for mode collapse.

5-Standard Approach in Research

    Many research papers on mode collapse in GANs use synthetic datasets (like Gaussian mixtures or ring structures) because they provide a clean way to study behavior.

![image](https://github.com/user-attachments/assets/0704bb2e-4096-4525-903a-45361b7aa532)


![image](https://github.com/user-attachments/assets/527b9b64-c7f2-453e-acf8-f001f10794fb)



![image](https://github.com/user-attachments/assets/9d957e6e-c919-43c7-9994-f363b30f58bf)



![image](https://github.com/user-attachments/assets/4e818097-8736-4eb9-aa8c-443311bbd9a7)



![image](https://github.com/user-attachments/assets/1f5e7793-c3ae-4e8a-955d-7dca8cea8b5f)



![image](https://github.com/user-attachments/assets/c913f50a-d741-4a7d-bf21-a2f36013ae4a)










    
