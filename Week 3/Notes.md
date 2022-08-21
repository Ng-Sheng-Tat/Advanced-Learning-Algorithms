### Practical advice for implementing machine learning project
**Possible Solutions for large errors in predictions (Cost Function) \*after you have implemented the regularized linear regression on housing prices**
1. Get more training examples (fixes high variance)
2. Try smaller sets of features (fixes high variance)
3. Try getting additional features (fixes high bias)
4. Try adding polynomial (more degree) features (fixes high bias)
5. Try decreasing $\lambda$ (fixes high bias)
6. Try increasing $\lambda$ (fixes high variance)
- these choices fix either high bias or high variance problems

- it is important to run a *Diagnostic Test*, which undeniably takes time but the test helps you to gain insight into what might or might not working with a learning algorithm, to gain guidance into improving its performance

### Evaluating a model 
- creating a scatter plot, and see what are the possible types of equation that suit the plot of the scatter graphs

### Establishing a baseline level of performance
**What is the level of error you can reasonably hope to get to?**
1. Human level performance
2. Competing algorithms performance
3. Guess based on experience by previous researchers or programmers


### Error Analysis
<figure>
    <center>
    <img src="Error Analysis.png" alt="Error Analysis" style="width:100%">
    <figcaption>Error Analysis</figcaption>
</figure>

- they are not mutually exclusive, means trying to get insights what are the common features that lead to misclassification and 
- might applies sampling technique to 100 examples to examine
- might not be an easy task if the application is something where human is not good at like reading an email

### Adding Data
- add only insufficient or specific categories' data not every general data

**Data Augmentation**: it is a technique to modify an existing training example to create new training example
- usually for audio and images
- examples include images rotation, enlargement, contrast-adjustment, images flipping-mirroring, adding images distortions
- adding different noisy background noise into the audio clips, changing the format into an bad cellphone connection type
- distortion introduced should be representation of the type of noise/distortions in the test set
- it is usually does not help to add purely random/meaningless noise to your data

**Data Synthesis**: creating brand new data from scratch
- for Photo OCR (Photo Optical Character Recognition): you can use different font stypes in computer and screenshort and applies different contrast to make up and scale up the amount of data that you have

<figure>
    <center>
    <img src="Data Engineering.png" alt="Data Engineering" style="width:85%">
    <figcaption>Data Engineering</figcaption>
</figure>

### Transfer Leraning
- using differerent data from different tasks to help on your current application
<figure>
    <center>
    <img src="Transfer Learning.png" alt="Transfer Learning" style="width:100%">
    <figcaption>Transfer Learning</figcaption>
</figure>

- Option 1: only retrained the output layer by using Adam or gradient descent or shochastic gradient descent
- Option 2: Use the initial weight and bias value to initialize, can be used if you have reasonable large dataset

<figure>
    <center>
    <img src="Why Transfer Leraning Works.png" alt="Why Transfer Leraning Works" style="width:100%">
    <figcaption>Why Transfer Leraning Works</figcaption>
</figure>

- so the previous layers does the same purpose of thing so that can be reuse the weight and bias adjusted or trained

**Summary of Transfer Learning Step**
1. Download neural network parameters pretrained on a large dataset with same input type (e.g., images, audio, text) as your application (or train your own) *typically done by using a tremendous large amount of training data
2. Further train (fine tune) the network on your own data *typically achieved by using a smaller set of training data

### Full Cycle of a Machine Learning Project
<figure>
    <center>
    <img src="Full Cycle of a Machine Learning Project.png" alt="Full Cycle of a Machine Learning Project" style="width:100%">
    <figcaption>Full Cycle of a Machine Learning Project</figcaption>
</figure>

<figure>
    <center>
    <img src="Development.png" alt="Development" style="width:100%">
    <figcaption>Development</figcaption>
</figure>

- Machine Learning Operation ensures the proper update, deployment, and proper training of the machine learning models so that it is well maintained with its accuracy over the time, takes over the software engineers' work

### Bias, ethics, and fairness
**Bias Case**
1. Hiring tools that discriminates against women
2. Facial recognition that tends to suspect dark skinned individual as criminals
3. Biased bank loan approvals
4. Toxic effect of reinforcing negative stereotypes

**Adverse use cases**
1. Deepfakes
2. Spreading toxic/incendiary speech through optimizing for engagement
3. Generating fake content for commercial or political purposes
4. Using Machine Learning to build harmful products, commit fraud

**Ethics Guidelines**

<figure>
    <center>
    <img src="Ethics Guidelines.png" alt="Ethics Guidelines" style="width:100%">
    <figcaption>Ethics Guidelines</figcaption>
</figure>
