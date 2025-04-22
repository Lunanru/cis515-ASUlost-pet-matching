# Lost Pet Matching System — CIS 515 Final Project

This project is a proof-of-concept system to help identify lost pets using computer vision.

It was created as part of the final project for the **CIS 515 Deep Learning course** at Arizona State University (Spring 2025).

---

## Project Overview

When pets go missing, it can be difficult to match “found pet” sightings with “lost pet” reports.  
This system allows a user to upload a photo of a lost pet and compares it against a small database of found pet images using **pretrained ResNet-50** and **cosine similarity**.

The idea is inspired by [LOSTPAW (Voinea et al., 2023)](https://arxiv.org/abs/2304.14765), which uses contrastive learning for pet re-identification.  
Our version simplifies that model to make it lightweight and demo-ready.

---

## How It Works

1. A user uploads a query image (`lost_pet.jpeg`).
2. The system extracts image features using `ResNet-50` (pretrained on ImageNet).
3. These features are compared to every image in the `pet_database/` using cosine similarity.
4. The top 3 most similar images are returned and visualized side-by-side.

---

##  Folder Structure

project_folder/  
├── pet_match_demo.ipynb      # Main notebook  
├── lost_pet.jpeg             # Query image  
└── pet_database/             # Found pet images  
  ├── petA2.jpg  
  ├── petB1.jpeg  
  └── ...


---

## Sample Output

Top 3 Matches:  
petA2.jpg → Similarity = 0.9423  
petB1.jpg → Similarity = 0.7635  
petC1.jpg → Similarity = 0.6128  

The system also visualizes the top match side-by-side with the query image.


---

## Technologies Used

- Python 3
- PyTorch
- torchvision
- scikit-learn
- PIL
- Jupyter Notebook

---

## Future Improvements

- Fine-tune model using contrastive learning (Siamese network)
- Integrate video input (e.g. campus security cameras)
- Build a real-time pet finder dashboard
- Expand to include shelters and rescue databases

---

## Author

Created by Luna Hsieh
Arizona State University  
Spring 2025 | CIS 515
