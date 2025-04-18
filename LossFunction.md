1. Standard GAN Loss (Vanilla GAN Loss)

This is the original GAN loss introduced by Goodfellow et al. (2014). It is based on the binary cross-entropy loss.

1.1 Discriminator Loss (D)

The discriminator is trained to maximize the probability of correctly classifying real and fake samples.
![image](https://github.com/user-attachments/assets/964389da-2fec-44b7-b778-75519cacfb6f)

D(x) → Discriminator’s probability that real sample x is real.

D(G(z)) → Discriminator’s probability that fake sample G(z) is real.

Goal: Maximize D(x) and Minimize D(G(z)) → Make discriminator better at distinguishing real vs. fake.



1.2 Generator Loss (G)

The generator tries to fool the discriminator by generating fake samples that look real.
![image](https://github.com/user-attachments/assets/f4a3b593-4dcb-4d7d-af79-00eccef3dd27)

The generator wants the discriminator to classify fakes as real.

It maximizes D(G(z)), so fake samples appear real.

PROBLEM WITH STANDARD GAN LOSS:
Vanishing gradients problem → When the discriminator becomes too strong, log⁡(1−D(G(z)) becomes very small, making it hard for the generator to improve.



2. Non-Saturating GAN Loss (NS-GAN)

This is an improved version of the Standard GAN Loss designed to avoid vanishing gradients.


2.1 Generator Loss (G)
![image](https://github.com/user-attachments/assets/615d7186-7125-4ad4-acef-0e2a7daf6e2c)

2.2 Discriminator Loss (D)

The discriminator’s loss remains the same as in the standard GAN.

Why NS-GAN? ✅ Fixes the vanishing gradients issue

✅ Leads to more stable training

❌ Still sensitive to mode collapse (where the generator only produces one type of sample)



3. Wasserstein GAN (WGAN)

WGAN is a major improvement over Standard GANs, introduced in Arjovsky et al. (2017). It solves issues like:

    Mode collapse

    Unstable training

    Vanishing gradients

3.1 WGAN Discriminator Loss (Critic)

Unlike Standard GANs, WGAN does not classify real/fake samples using probabilities. Instead, it outputs a real-valued score.

![image](https://github.com/user-attachments/assets/e16d541e-10c7-4292-bfc9-aeb058bc5bc6)

3.2 WGAN Generator Loss

The generator wants to maximize the discriminator’s score for fake samples:

![image](https://github.com/user-attachments/assets/feafe377-120b-44e0-9a07-474a556bdc4a)

The generator pushes the critic to increase its score for fake images.

4. Wasserstein GAN with Gradient Penalty (WGAN-GP)

To fix WGAN's problem with weight clipping, WGAN-GP (Gulrajani et al., 2017) enforces the Lipschitz constraint using a gradient penalty instead of weight clipping.

4.1 Gradient Penalty Calculation

![image](https://github.com/user-attachments/assets/7554314d-c5b6-4d61-b939-67d3b94cd7d7)

4.2 WGAN-GP Discriminator Loss

![image](https://github.com/user-attachments/assets/bad3843b-dfde-4c2c-b4e9-35dda3e35664)

