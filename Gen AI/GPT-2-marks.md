
# UNIT 1 – Introduction to Generative AI

---

## 1. What are generative models?
**Answer:**  
Generative models learn the underlying probability distribution of data so they can generate new, similar samples.  
They model **P(X)** or **P(X|Z)** and capture structure in training data.  
Examples include GANs, VAEs, Diffusion Models, and Normalizing Flows.  
They are widely used in image synthesis, speech generation, drug discovery, and simulation tasks.

---

## 2. Define discriminative models.
**Answer:**  
Discriminative models learn the mapping from input data to output labels, modeling **P(Y|X)**.  
They classify or predict outcomes but do not generate new samples.  
Examples include Logistic Regression, SVM, Random Forest, and CNN classifiers.  
They are typically more efficient for supervised learning tasks.

---

## 3. What is the difference between generative and discriminative models?
**Answer:**  
Generative models learn full data distributions and create new samples, while discriminative models learn boundaries between classes.  
Generative → “How data is formed.”  
Discriminative → “Which class does this belong to?”  
Generative models support unsupervised tasks; discriminative models excel in classification.

---

## 4. What are Bayesian Networks?
**Answer:**  
Bayesian Networks are probabilistic graphical models using directed acyclic graphs to represent dependencies.  
Nodes represent variables; edges show conditional relationships.  
They support probabilistic inference, causal reasoning, and uncertainty modeling.

---

## 5. Define Diffusion Models.
**Answer:**  
Diffusion models generate data by reversing a noise-adding process.  
Training: gradually add Gaussian noise.  
Generation: start from noise and denoise step-by-step.  
Used in modern text-to-image systems like **Stable Diffusion**, **DALL·E 2**, and **Midjourney**.

---

## 6. What is a GAN?
**Answer:**  
A Generative Adversarial Network consists of a **Generator** and a **Discriminator** competing in training.  
Generator creates fake data; discriminator identifies fakes.  
This adversarial learning process produces highly realistic synthetic images.

---

## 7. What are Variational Autoencoders (VAEs)?
**Answer:**  
VAEs are probabilistic autoencoders that learn latent distributions instead of direct encodings.  
Loss = Reconstruction Loss + KL Divergence.  
They support controlled sampling and smooth latent interpolation.

---

## 8. Define Restricted Boltzmann Machines.
**Answer:**  
RBMs are energy-based generative models with visible and hidden layers.  
Training uses Contrastive Divergence.  
Historically important for pretraining deep networks, later replaced by more powerful generative models.

---

## 9. What are PixelRNNs?
**Answer:**  
PixelRNNs are autoregressive models that generate images pixel-by-pixel.  
Each pixel is conditioned on previously generated pixels.  
They provide high likelihood accuracy but are slow for high-resolution image generation.

---

## 10. Define Markov Chains.
**Answer:**  
Markov Chains are stochastic processes where future states depend only on the current state (memoryless property).  
Used in text generation, simulations, and sequential modeling.

---

## 11. What are Normalizing Flows?
**Answer:**  
Normalizing Flows transform simple distributions (Gaussian) into complex ones using invertible functions.  
Allow exact log-likelihood computation and efficient sampling.  
Used in density estimation and advanced generative modeling.

---

## 12. What is image transformation?
**Answer:**  
Image transformation refers to preprocessing and augmentations like resizing, cropping, flipping, color jitter, and normalization.  
Improves dataset diversity and model generalization.

---

## 13. Define Deep Neural Networks.
**Answer:**  
DNNs contain multiple layers of neurons capable of learning complex hierarchical representations.  
They solve tasks in vision, NLP, speech, robotics, and reinforcement learning.

---

## 14. What is a perceptron?
**Answer:**  
The perceptron is the basic unit of neural networks:  
Weighted sum → Activation → Output.  
Used for linearly separable classification tasks.

---

## 15. Define backpropagation.
**Answer:**  
Backpropagation computes gradients of loss with respect to weights using the chain rule.  
Used to update weights during training.  
Backbone of all modern deep learning.

---

## 16. What is a CNN?
**Answer:**  
Convolutional Neural Networks use convolutional filters to detect spatial patterns in images.  
Layers learn edges → textures → shapes → objects.

---

## 17. What is an RNN?
**Answer:**  
Recurrent Neural Networks maintain temporal states to process sequences.  
Variants like LSTM/GRU solve long-term dependency issues.

---

## 18. Define Gradient Descent.
**Answer:**  
Gradient Descent updates model parameters by moving opposite to the gradient of loss.  
Used for optimization in machine learning.

---

## 19. What is Stochastic Gradient Descent?
**Answer:**  
SGD updates weights using a single sample at a time.  
Provides noisy but fast convergence and helps escape local minima.

---

## 20. What is Mini-batch Gradient Descent?
**Answer:**  
Uses small batches of data to compute gradients.  
Balances efficiency and stability.  
Most commonly used optimization strategy.

---

# UNIT 2 – Image Encodings & TensorFlow Networks

---

## 1. Define image encoding.
**Answer:**  
Image encoding compresses an image into a numerical vector capturing essential features.  
CNNs extract edges, textures, and semantic features into a compact latent space.

---

## 2. What is dimensionality reduction?
**Answer:**  
Dimensionality reduction reduces feature count while retaining information.  
Techniques: **PCA, t-SNE, UMAP, Autoencoders**.  
Used for visualization, compression, and noise reduction.

---

## 3. What is the variational objective?
**Answer:**  
VAE objective = Reconstruction Loss + KL Divergence.  
KL divergence shapes latent space into a continuous Gaussian, enabling controlled sampling.

---

## 4. Define Inverse Autoregressive Flow.
**Answer:**  
IAF enhances VAEs by applying invertible flow transformations to latent variables.  
Improves posterior flexibility and sample quality.

---

## 5. What is TensorFlow 2 used for?
**Answer:**  
TF2 is used to build, train, and deploy deep learning models with Keras API support, eager execution, GPU acceleration, and production tools.

---

## 6. What is CIFAR-10?
**Answer:**  
Dataset of 60,000 images across 10 classes (32x32).  
Common benchmark for image classification.

---

## 7. What is CIFAR-100?
**Answer:**  
Similar to CIFAR-10 but with 100 fine-grained classes.  
More challenging due to higher class density.

---

## 8. What is the KL divergence term in VAEs?
**Answer:**  
KL divergence regularizes latent distribution toward Normal(0,1).  
Ensures smooth latent space and prevents overfitting.

---

## 9. What is a latent vector?
**Answer:**  
Low-dimensional vector encoding essential features of input data.  
Used in VAEs, GANs, autoencoders, CLIP, and diffusion models.

---

## 10. What is the purpose of model compilation in TF2?
**Answer:**  
Specifies loss, optimizer, and metrics before training.  
Builds computational graph for gradient updates.

---

# UNIT 3 – GANs

---

## 1. Define a GAN.
**Answer:**  
GAN = Generator + Discriminator trained adversarially.  
Generator creates data; discriminator validates real vs fake.

---

## 2. What is a Conditional GAN?
**Answer:**  
GAN conditioned on labels or additional information.  
Allows controlled generation like “Generate digit 7” or “Generate a red shoe.”

---

## 3. What is DCGAN?
**Answer:**  
Deep Convolutional GAN using CNN layers.  
Produces higher-quality images and stable training.

---

## 4. Define LAPGAN.
**Answer:**  
Laplacian Pyramid GAN generates images progressively from low → high resolution.

---

## 5. Define SRGAN.
**Answer:**  
Super-Resolution GAN converts low-resolution images into high-resolution ones using perceptual loss.

---

## 6. What is the role of a generator in GAN?
**Answer:**  
Converts noise into fake data that mimics real samples.

---

## 7. What is the role of a discriminator?
**Answer:**  
Distinguishes real data from generated data.  
Trains to identify fake examples.

---

## 8. What is mode collapse?
**Answer:**  
Generator produces limited or identical outputs regardless of input noise.  
Common GAN training issue.

---

## 9. What is MinMax Loss?
**Answer:**  
GAN objective:  
Minimize Generator Loss, Maximize Discriminator Loss.  
Defines adversarial optimization.

---

## 10. Define Deepfake.
**Answer:**  
AI-generated videos replacing faces or voices.  
Uses GANs, autoencoders, and motion transfer techniques.

---

# UNIT 4 – LLMs & Transformers

---

## 1. What is a Large Language Model (LLM)?
**Answer:**  
LLMs are transformer-based models trained on large corpora to perform text generation, reasoning, coding, translation, etc.

---

## 2. What is a Transformer?
**Answer:**  
Deep learning model using self-attention to model long-range dependencies without recurrence.

---

## 3. What are autoregressive models?
**Answer:**  
Models that generate one token at a time conditioned on previous tokens.  
Example: GPT.

---

## 4. Define encoder-decoder architecture.
**Answer:**  
Encoder processes input; decoder generates output.  
Used in translation, summarization, T5.

---

## 5. What is GPT?
**Answer:**  
Generative Pretrained Transformer using decoder-only architecture for next-token prediction.

---

## 6. What is T5?
**Answer:**  
Text-to-Text Transfer Transformer framing all NLP tasks as text → text.

---

## 7. What are multilingual models?
**Answer:**  
Models trained across many languages, enabling translation and cross-lingual understanding.

---

## 8. What are hybrid models?
**Answer:**  
Models combining autoregressive, encoder-decoder, retrieval augmentation, or MoE approaches.

---

## 9. What is self-attention?
**Answer:**  
Mechanism where tokens attend to each other to compute contextual meaning.

---

## 10. What are positional encodings?
**Answer:**  
Patterns injected into embeddings to provide sequence order information.

---

# UNIT 5 – Prompting & In-Context Learning

---

## 1. What is a prompt?
**Answer:**  
Instruction given to an LLM to guide output generation.

---

## 2. What are types of prompts?
**Answer:**  
Instruction, zero-shot, few-shot, role-based, chain-of-thought.

---

## 3. What is zero-shot prompting?
**Answer:**  
Prompt without any examples.  
Relies on model’s pretraining knowledge.

---

## 4. What is few-shot prompting?
**Answer:**  
Prompt containing examples to demonstrate the expected pattern.

---

## 5. What is in-context learning (ICL)?
**Answer:**  
Model learns from examples in the prompt without changing weights.

---

## 6. What is in-context prompting (ICP)?
**Answer:**  
Designing prompts optimized for ICL performance.

---

## 7. What is chain-of-thought prompting?
**Answer:**  
Prompt encouraging model to show step-by-step reasoning.

---

## 8. What is image prompting?
**Answer:**  
Using detailed textual prompts to control diffusion or transformer-based image models.

---

## 9. Define prompt hijacking.
**Answer:**  
Security threat where malicious prompts override system instructions.

---

## 10. What is retrieval-augmented generation?
**Answer:**  
Technique where external knowledge is added to prompts for more accurate responses.

---

